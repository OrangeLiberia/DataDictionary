# Outgoing Calls Caller Name Fix

## Date
2026-04-29

## File Updated
- outgoing_calls_from_excel_msisdn.sql

## Issue
CallerName values were missing for some outgoing call records because phone numbers were not normalized consistently before joining with KYC data.

## Root Cause
The query used direct right-trim logic for MSISDN values, which did not reliably map all number formats (for example:
- local 9-digit numbers,
- local numbers prefixed with 0,
- country-code format prefixed with 231)
into a single KYC join key format.

## Fix Applied
Normalized served and dialed numbers into a consistent 10-digit local format before KYC lookup:
- If value starts with 231 and has at least 12 digits: use 0 + last 9 digits.
- If value starts with 0 and has at least 10 digits: keep last 10 digits.
- If value is exactly 9 digits: prepend 0.
- Otherwise: fallback to last 10 digits.

This normalization is applied to:
- CallerMSISDN10
- DialedMSISDN10

## Expected Result
- Improved CallerName and DialedNumberName population from vwc_KYCSubscribers.
- Fewer null name values in outgoing call output.

## Validation
- SQL diagnostics for outgoing_calls_from_excel_msisdn.sql returned no syntax errors after the update.

## Queries
-- Unique MSISDN count: 31

DECLARE @StartDate DATE = '2026-01-01';
DECLARE @EndDate DATE = '2026-04-27';

CREATE TABLE #TargetMSISDNs (
    MSISDN VARCHAR(20) NOT NULL PRIMARY KEY
);

INSERT INTO #TargetMSISDNs (MSISDN)
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
('775361151');

IF OBJECT_ID('tempdb..#TargetMatchNumbers') IS NULL
BEGIN
    CREATE TABLE #TargetMatchNumbers (
        MatchMSISDN VARCHAR(20) NOT NULL PRIMARY KEY
    );
END
ELSE
BEGIN
    TRUNCATE TABLE #TargetMatchNumbers;
END

;WITH CandidateMatchNumbers AS (
        SELECT MSISDN AS MatchMSISDN FROM #TargetMSISDNs
        UNION ALL
        SELECT '0' + MSISDN FROM #TargetMSISDNs
        UNION ALL
        SELECT '231' + MSISDN FROM #TargetMSISDNs
)
INSERT INTO #TargetMatchNumbers (MatchMSISDN)
SELECT DISTINCT MatchMSISDN
FROM CandidateMatchNumbers
WHERE MatchMSISDN IS NOT NULL
    AND MatchMSISDN <> '';

IF OBJECT_ID('tempdb..#FilteredCalls') IS NOT NULL DROP TABLE #FilteredCalls;
CREATE TABLE #FilteredCalls (
    servedMSISDN VARCHAR(30) NULL,
    calledNumber VARCHAR(30) NULL,
    servedIMEI VARCHAR(30) NULL,
    seizureTime DATETIME NULL,
    answerTime DATETIME NULL,
    releaseTime DATETIME NULL,
    callDuration BIGINT NULL,
    location_lac VARCHAR(30) NULL,
    location_sac VARCHAR(30) NULL,
    location_ci VARCHAR(30) NULL,
    CallerMSISDN10 VARCHAR(20) NULL,
    DialedMSISDN10 VARCHAR(20) NULL
);

INSERT INTO #FilteredCalls (
    servedMSISDN,
    calledNumber,
    servedIMEI,
    seizureTime,
    answerTime,
    releaseTime,
    callDuration,
    location_lac,
    location_sac,
    location_ci,
    CallerMSISDN10,
    DialedMSISDN10
)


SELECT
    M.servedMSISDN,
    M.calledNumber,
    M.servedIMEI,
    M.seizureTime,
    M.answerTime,
    M.releaseTime,
    M.callDuration,
    M.location_lac,
    M.location_sac,
    M.location_ci,
    CASE
        WHEN M.servedMSISDN IS NULL OR LTRIM(RTRIM(M.servedMSISDN)) = '' THEN NULL
        WHEN LEFT(M.servedMSISDN, 3) = '231' AND LEN(M.servedMSISDN) >= 12 THEN '0' + RIGHT(M.servedMSISDN, 9)
        WHEN LEFT(M.servedMSISDN, 1) = '0' AND LEN(M.servedMSISDN) >= 10 THEN RIGHT(M.servedMSISDN, 10)
        WHEN LEN(M.servedMSISDN) = 9 THEN '0' + M.servedMSISDN
        ELSE RIGHT(M.servedMSISDN, 10)
    END AS CallerMSISDN10,
    CASE
        WHEN M.calledNumber IS NULL OR LTRIM(RTRIM(M.calledNumber)) = '' THEN NULL
        WHEN LEFT(M.calledNumber, 3) = '231' AND LEN(M.calledNumber) >= 12 THEN '0' + RIGHT(M.calledNumber, 9)
        WHEN LEFT(M.calledNumber, 1) = '0' AND LEN(M.calledNumber) >= 10 THEN RIGHT(M.calledNumber, 10)
        WHEN LEN(M.calledNumber) = 9 THEN '0' + M.calledNumber
        ELSE RIGHT(M.calledNumber, 10)
    END AS DialedMSISDN10
FROM [DMP_ZTE_Repository_202604].[dbo].[MOCallRecord] M WITH (NOLOCK)
INNER JOIN #TargetMatchNumbers TM ON TM.MatchMSISDN = M.servedMSISDN
WHERE M.seizureTime >= @StartDate
  AND M.seizureTime < DATEADD(DAY, 1, @EndDate);

CREATE INDEX IX_FilteredCalls_SeizureTime ON #FilteredCalls (seizureTime);
CREATE INDEX IX_FilteredCalls_CallerMSISDN10 ON #FilteredCalls (CallerMSISDN10);
CREATE INDEX IX_FilteredCalls_DialedMSISDN10 ON #FilteredCalls (DialedMSISDN10);

IF OBJECT_ID('tempdb..#KYCNames') IS NOT NULL DROP TABLE #KYCNames;
CREATE TABLE #KYCNames (
    MSISDN10 VARCHAR(20) NOT NULL PRIMARY KEY,
    CustomerName VARCHAR(255) NULL
);

INSERT INTO #KYCNames (MSISDN10, CustomerName)
SELECT
    K.MSISDN10,
    MAX(COALESCE(K.[Subscriber Name], K.[Client Name])) AS CustomerName
FROM [TIMM_CRM].[dbo].[vwc_KYCSubscribers] K WITH (NOLOCK)
WHERE K.MSISDN10 IN (
    SELECT CallerMSISDN10 FROM #FilteredCalls
    UNION
    SELECT DialedMSISDN10 FROM #FilteredCalls
)
GROUP BY K.MSISDN10;

SELECT
    F.servedMSISDN AS CallerNumber,
    KC.CustomerName AS CallerName,
    F.calledNumber AS DialedNumber,
    KD.CustomerName AS DialedNumberName,
    F.servedIMEI AS DeviceIMEI,
    F.seizureTime AS SeizureTime,
    F.answerTime AS AnswerTime,
    F.releaseTime AS ReleaseTime,
    F.callDuration / 60.0 AS DurationMinutes,
    CELL1.sitename AS ServingSite,
    CELL.sitename AS LocationSite,
    RIGHT(F.location_lac, 1) AS LAC,
    CASE WHEN F.answerTime IS NOT NULL THEN 'Answered' ELSE 'Unanswered' END AS CallStatus
FROM #FilteredCalls F
LEFT JOIN TIMM_DMP.dbo.DMP_SwitchCellIDs CELL ON CELL.id = LEFT(F.location_sac, 4)
LEFT JOIN TIMM_DMP.dbo.DMP_SwitchCellIDs CELL1 ON CELL1.id = LEFT(F.location_ci, 4)
LEFT JOIN #KYCNames KC ON KC.MSISDN10 = F.CallerMSISDN10
LEFT JOIN #KYCNames KD ON KD.MSISDN10 = F.DialedMSISDN10
ORDER BY F.seizureTime DESC, F.answerTime DESC
OPTION (RECOMPILE);


