# Incoming Calls Caller Name Fix

## Date
2026-04-29

## File Updated
- incoming_calls_from_excel_msisdn.sql

## Issue
CallerName and ReceiverName values could be missing for some incoming call records when MSISDN formats were not normalized consistently before KYC joins.

## Root Cause
Number normalization for incoming records did not fully align with the outgoing query pattern, especially for blank/whitespace values and mixed local vs country-code representations.

## Fix Applied
Aligned incoming MSISDN normalization to the same logic used in outgoing calls, for both CallerMSISDN10 and ReceiverMSISDN10:
- If value is null or blank after trim: return NULL.
- If value starts with 231 and has at least 12 digits: use 0 + last 9 digits.
- If value starts with 0 and has at least 10 digits: keep last 10 digits.
- If value is exactly 9 digits: prepend 0.
- Otherwise: fallback to last 10 digits.

## Expected Result
- Better name resolution from vwc_KYCSubscribers for incoming call records.
- Fewer null values in CallerName and ReceiverName.

## Validation
- SQL diagnostics for incoming_calls_from_excel_msisdn.sql returned no syntax errors after the update.

## Queries
-- Unique MSISDN count: 31

DECLARE @StartDate DATE = '2026-04-01';
DECLARE @EndDate DATE = '2026-04-27';

IF OBJECT_ID('tempdb..#In_TargetMSISDNs') IS NOT NULL DROP TABLE #In_TargetMSISDNs;
CREATE TABLE #In_TargetMSISDNs (
    MSISDN VARCHAR(20) NOT NULL PRIMARY KEY
);

INSERT INTO #In_TargetMSISDNs (MSISDN)
VALUES
    ('778888319'),
    ('778888312'),
    ('778888321'),
    ('778888306'),
    ('778888303'),
    ('778888307'),
    ('778888315'),
    ('778888314'),
    ('778888317'),
    ('778888308'),
    ('778888305'),
    ('775361158'),
    ('775361186'),
    ('773359258'),
    ('775361136'),
    ('775361139'),
    ('775361149'),
    ('775361184'),
    ('773171415'),
    ('775361178'),
    ('773172236'),
    ('775361157'),
    ('773171440'),
    ('773172338'),
    ('773474730'),
    ('773172276'),
    ('775361127'),
    ('773475943'),
    ('772466001'),
    ('775361169'),
    ('775361151')
;

IF OBJECT_ID('tempdb..#In_TargetMatchNumbers') IS NULL
BEGIN
    CREATE TABLE #In_TargetMatchNumbers (
        MatchMSISDN VARCHAR(20) NOT NULL PRIMARY KEY
    );
END
ELSE
BEGIN
    TRUNCATE TABLE #In_TargetMatchNumbers;
END

;WITH CandidateMatchNumbers AS (
    SELECT MSISDN AS MatchMSISDN FROM #In_TargetMSISDNs
    UNION ALL
    SELECT '0' + MSISDN FROM #In_TargetMSISDNs
    UNION ALL
    SELECT '231' + MSISDN FROM #In_TargetMSISDNs
)
INSERT INTO #In_TargetMatchNumbers (MatchMSISDN)
SELECT DISTINCT MatchMSISDN
FROM CandidateMatchNumbers
WHERE MatchMSISDN IS NOT NULL
  AND MatchMSISDN <> '';

IF OBJECT_ID('tempdb..#In_FilteredCalls') IS NOT NULL DROP TABLE #In_FilteredCalls;
CREATE TABLE #In_FilteredCalls (
    callingnumber VARCHAR(30) NULL,
    servedMSISDN VARCHAR(30) NULL,
    seizureTime DATETIME NULL,
    answerTime DATETIME NULL,
    releaseTime DATETIME NULL,
    callDuration BIGINT NULL,
    location_lac VARCHAR(30) NULL,
    location_sac VARCHAR(30) NULL,
    location_ci VARCHAR(30) NULL,
    CallerMSISDN10 VARCHAR(20) NULL,
    ReceiverMSISDN10 VARCHAR(20) NULL
);

INSERT INTO #In_FilteredCalls (
    callingnumber,
    servedMSISDN,
    seizureTime,
    answerTime,
    releaseTime,
    callDuration,
    location_lac,
    location_sac,
    location_ci,
    CallerMSISDN10,
    ReceiverMSISDN10
)
SELECT
    M.callingnumber,
    M.servedMSISDN,
    M.seizureTime,
    M.answerTime,
    M.releaseTime,
    M.callDuration,
    M.location_lac,
    M.location_sac,
    M.location_ci,
    CASE
        WHEN M.callingnumber IS NULL OR LTRIM(RTRIM(M.callingnumber)) = '' THEN NULL
        WHEN LEFT(M.callingnumber, 3) = '231' AND LEN(M.callingnumber) >= 12 THEN '0' + RIGHT(M.callingnumber, 9)
        WHEN LEFT(M.callingnumber, 1) = '0' AND LEN(M.callingnumber) >= 10 THEN RIGHT(M.callingnumber, 10)
        WHEN LEN(M.callingnumber) = 9 THEN '0' + M.callingnumber
        ELSE RIGHT(M.callingnumber, 10)
    END AS CallerMSISDN10,
    CASE
        WHEN M.servedMSISDN IS NULL OR LTRIM(RTRIM(M.servedMSISDN)) = '' THEN NULL
        WHEN LEFT(M.servedMSISDN, 3) = '231' AND LEN(M.servedMSISDN) >= 12 THEN '0' + RIGHT(M.servedMSISDN, 9)
        WHEN LEFT(M.servedMSISDN, 1) = '0' AND LEN(M.servedMSISDN) >= 10 THEN RIGHT(M.servedMSISDN, 10)
        WHEN LEN(M.servedMSISDN) = 9 THEN '0' + M.servedMSISDN
        ELSE RIGHT(M.servedMSISDN, 10)
    END AS ReceiverMSISDN10
FROM [DMP_ZTE_Repository_202604].[dbo].[MTCallRecord] M WITH (NOLOCK)
INNER JOIN #In_TargetMatchNumbers TM ON TM.MatchMSISDN = M.servedMSISDN
WHERE M.seizureTime >= @StartDate
  AND M.seizureTime < DATEADD(DAY, 1, @EndDate);

CREATE INDEX IX_In_FilteredCalls_SeizureTime ON #In_FilteredCalls (seizureTime);
CREATE INDEX IX_In_FilteredCalls_CallerMSISDN10 ON #In_FilteredCalls (CallerMSISDN10);
CREATE INDEX IX_In_FilteredCalls_ReceiverMSISDN10 ON #In_FilteredCalls (ReceiverMSISDN10);

IF OBJECT_ID('tempdb..#In_KYCNames') IS NOT NULL DROP TABLE #In_KYCNames;
CREATE TABLE #In_KYCNames (
    MSISDN10 VARCHAR(20) NOT NULL PRIMARY KEY,
    CustomerName VARCHAR(255) NULL
);

INSERT INTO #In_KYCNames (MSISDN10, CustomerName)
SELECT
    K.MSISDN10,
    MAX(COALESCE(K.[Subscriber Name], K.[Client Name])) AS CustomerName
FROM [TIMM_CRM].[dbo].[vwc_KYCSubscribers] K WITH (NOLOCK)
WHERE K.MSISDN10 IN (
    SELECT CallerMSISDN10 FROM #In_FilteredCalls
    UNION
    SELECT ReceiverMSISDN10 FROM #In_FilteredCalls
)
GROUP BY K.MSISDN10;

SELECT
    F.callingnumber AS CallerNumber,
    KC.CustomerName AS CallerName,
    F.servedMSISDN AS ReceiverNumber,
    KR.CustomerName AS ReceiverName,
    F.seizureTime AS SeizureTime,
    F.answerTime AS AnswerTime,
    F.releaseTime AS ReleaseTime,
    F.callDuration / 60.0 AS DurationMinutes,
    CELL1.sitename AS ServingSite,
    CELL.sitename AS LocationSite,
    RIGHT(F.location_lac, 1) AS LAC,
    CASE WHEN F.answerTime IS NOT NULL THEN 'Answered' ELSE 'Missed' END AS CallStatus
FROM #In_FilteredCalls F
LEFT JOIN TIMM_DMP.dbo.DMP_SwitchCellIDs CELL ON CELL.id = LEFT(F.location_sac, 4)
LEFT JOIN TIMM_DMP.dbo.DMP_SwitchCellIDs CELL1 ON CELL1.id = LEFT(F.location_ci, 4)
LEFT JOIN #In_KYCNames KC ON KC.MSISDN10 = F.CallerMSISDN10
LEFT JOIN #In_KYCNames KR ON KR.MSISDN10 = F.ReceiverMSISDN10
ORDER BY F.seizureTime DESC, F.answerTime DESC
OPTION (RECOMPILE);


## Prepared By
Bronax N. Barlue
MIS Engineer
