use dw_orangemoney
drop table timm_reports.dbo.financebuybudlereport
declare @begin date = '2026-03-01'
declare @end date = DATEADD("d",-1,'2026-05-01')
SELECT	MerchMSISDN as MerchantMSISDN,Name
	INTO	#Config
	 FROM	[TIMM.CRM.ERIS].API.[dbo].BundleSystemsMapping C WITH (NOLOCK)
	WHERE	C.Status=1
	group by MerchMSISDN,Name

SELECT T.[RefDate],T.[SENDER_MSISDN],T.RECEIVER_MSISDN,T.SERVICE_TYPE,T.TRANSFER_STATUS, convert(varchar(100),null) as Name,currencytype,TRANSACTION_AMOUNT ,convert(varchar(200),null) as Parent_Name
INTO timm_reports.dbo.financebuybudlereport
FROM [DW_OrangeMoney].[dbo].[Transactions] (NOLOCK) T
	WHERE  T.TRANSFER_STATUS = 'TS'  AND T.[RefDate] BETWEEN @begin AND @end 
and (		[SERVICE_TYPE] in  ('MERCHPAY','P2P') 
and ([TRANSFER_STATUS] = 'TS'
and [RECEIVER_DOMAIN_CODE] = 'ADDON' 
and [RECEIVER_GRADE_NAME] = 'Buy Bundles LD')
		)
		--Ut|b2JDpLX6SF[3c0]15
update g
set g.Name = H.Name
from timm_reports.dbo.financebuybudlereport g 
left join #Config H
on H.MerchantMSISDN = g.RECEIVER_MSISDN

select refdate,sum(TRANSACTION_AMOUNT) as Amount ,count(*) Total,CurrencyType,name from timm_reports.dbo.financebuybudlereport
group by RefDate,name,CurrencyType
order by RefDate


select count(*) Total,sum(TRANSACTION_AMOUNT) as Amount,Name,CurrencyType ,RECEIVER_MSISDN ,convert(char(7),[RefDate],120) as Months
from timm_reports.dbo.financebuybudlereport
group by Name,CurrencyType,RECEIVER_MSISDN,convert(char(7),[RefDate],120)

---- declare @begin date = '2021-07-01'
---- declare @end date = DATEADD("d",-1,'2021-08-01')
SELECT UA.MSISDN,UA.PARENT_USER_MSISDN,PARENT_LAST_NAME + ' '+PARENT_FIRST_NAME as PARENT_NAME,RefDate
INTO #TempUA
FROM [DW_OrangeMoney].[dbo].[ChannelUsers] (NOLOCK) UA
WHERE [RefDate] BETWEEN @begin AND @end
AND UA.USER_DOMAIN_CODE IN ('DISTRIBUTI','DISTIB') -- AND UA.Mobile_Group_Role ='GrpMobIS'
AND UA.STATUS = 'Y'
group by UA.MSISDN,UA.PARENT_USER_MSISDN,PARENT_LAST_NAME + ' '+PARENT_FIRST_NAME,RefDate


UPDATE t 
SET T.PARENT_NAME = e.PARENT_NAME
FROM   timm_reports.dbo.financebuybudlereport T 
INNER JOIN  (
SELECT UA.MSISDN,UA.PARENT_USER_MSISDN,PARENT_LAST_NAME + ' '+PARENT_FIRST_NAME as PARENT_NAME,RefDate
FROM [DW_OrangeMoney].[dbo].[ChannelUsers] (NOLOCK) UA
WHERE [RefDate] BETWEEN @begin AND @end
AND UA.USER_DOMAIN_CODE IN ('DISTRIBUTI','DISTIB') -- AND UA.Mobile_Group_Role ='GrpMobIS'
AND UA.STATUS = 'Y'
group by UA.MSISDN,UA.PARENT_USER_MSISDN,PARENT_LAST_NAME + ' '+PARENT_FIRST_NAME,RefDate
)e 
ON t.RefDate = E.REFDATE AND T.SENDER_MSISDN = E.MSISDN

SELECT currencytype, COUNT(*) AS Activations,sum(TRANSACTION_AMOUNT) as Amount,Parent_Name,SENDER_MSISDN,convert(varchar(7),refdate,120) as MonthRef,Name as Bundle
into #bbldata 
FROM timm_reports.dbo.financebuybudlereport
group by Parent_Name,convert(varchar(7),refdate,120),SENDER_MSISDN,Parent_Name,name,currencytype
order by MonthRef
insert into TIMM_Reports.dbo.bundlemonthly
select * from #bbldata
where Parent_Name is not null

select top 3 * from TIMM_Reports.dbo.bundlemonthly
where MonthRef ='2026-04'
