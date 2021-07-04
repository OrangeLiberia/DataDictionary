#### 

[Project](../../../../index.md) > [TIMMBI\\BI](../../../index.md) > [User databases](../../index.md) > [External](../index.md) > [Tables](Tables.md) > dbo.LDvsUSDReport

# ![Tables](../../../../Images/Table32.png) [dbo].[LDvsUSDReport]

---

## <a name="#properties"></a>Properties



---

## <a name="#columns"></a>Columns

| Key | Name | Data Type | Computed | Max Length (Bytes) | Nullability |
|---|---|---|---|---|---|
| [![Cluster Primary Key PK_LDvsUSDReport: IDDimDate](../../../../Images/pkcluster.png)](#indexes) | IDDimDate | int |  | 4 | NOT NULL |
|  | Month | datetime |  | 8 | NULL allowed |
|  | LDDistinctSubs | bigint |  | 8 | NULL allowed |
|  | USDDistinctSubs | bigint |  | 8 | NULL allowed |
|  | LDUSDDistinctSubs | bigint |  | 8 | NULL allowed |
|  | TotalDistinctSubs | bigint | YES | 8 | NULL allowed |
|  | LDOnNetMinutes | bigint |  | 8 | NULL allowed |
|  | USDOnNetMinutes | bigint |  | 8 | NULL allowed |
|  | TotalOnNetMinutes | bigint | YES | 8 | NULL allowed |
|  | LDOffNetMinutes | bigint |  | 8 | NULL allowed |
|  | USDOffNetMinutes | bigint |  | 8 | NULL allowed |
|  | TotalOffNetMinutes | bigint | YES | 8 | NULL allowed |
|  | LDIntlMinutes | bigint |  | 8 | NULL allowed |
|  | USDIntlMinutes | bigint |  | 8 | NULL allowed |
|  | TotalIntlMinutes | bigint | YES | 8 | NULL allowed |
|  | TotalLDMinutes | bigint | YES | 8 | NULL allowed |
|  | TotalUSDMinutes | bigint | YES | 8 | NULL allowed |
|  | TotalMinutes | bigint | YES | 8 | NULL allowed |
|  | LDNCalls | bigint |  | 8 | NULL allowed |
|  | USDNCalls | bigint |  | 8 | NULL allowed |
|  | TotalNCalls | bigint | YES | 8 | NULL allowed |
|  | LDRechargesAmount | money |  | 8 | NULL allowed |
|  | USDRechargesAmount | money |  | 8 | NULL allowed |
|  | TotalRechargesAmount | money | YES | 8 | NULL allowed |
|  | LDOnNetConsumedAmount | money |  | 8 | NULL allowed |
|  | USDOnNetConsumedAmount | money |  | 8 | NULL allowed |
|  | TotalOnNetConsumed | money | YES | 8 | NULL allowed |
|  | LDOffNetConsumedAmount | money |  | 8 | NULL allowed |
|  | USDOffNetConsumedAmount | money |  | 8 | NULL allowed |
|  | TotalOffNetConsumed | money | YES | 8 | NULL allowed |
|  | LDIntlConsumedAmount | money |  | 8 | NULL allowed |
|  | USDIntlConsumedAmount | money |  | 8 | NULL allowed |
|  | TotalIntlConsumed | money | YES | 8 | NULL allowed |
|  | TotalLDConsumedAmount | money | YES | 8 | NULL allowed |
|  | TotalUSDConsumedAmount | money | YES | 8 | NULL allowed |
|  | TotalConsumedAmount | money | YES | 8 | NULL allowed |
|  | LDvsUSDConsumptionRate | decimal(5,2) | YES | 5 | NULL allowed |
|  | LDOnNetMinuteTariff | float |  | 8 | NULL allowed |
|  | USDOnNetMinuteTariff | float |  | 8 | NULL allowed |
|  | TotalOnNetMinuteTariff | float |  | 8 | NULL allowed |
|  | LDOffNetMinuteTariff | float |  | 8 | NULL allowed |
|  | USDOffNetMinuteTariff | float |  | 8 | NULL allowed |
|  | TotalOffNetMinuteTariff | float |  | 8 | NULL allowed |
|  | LDIntlMinuteTariff | float |  | 8 | NULL allowed |
|  | USDIntlMinuteTariff | float |  | 8 | NULL allowed |
|  | TotalIntlMinuteTariff | float |  | 8 | NULL allowed |
|  | LDSMSConsumedAmount | money |  | 8 | NULL allowed |
|  | USDSMSConsumedAmount | money |  | 8 | NULL allowed |
|  | TotalSMSConsumedAmount | money | YES | 8 | NULL allowed |
|  | LD14xDistinctSubs | bigint |  | 8 | NULL allowed |
|  | USD14xDistinctSubs | bigint |  | 8 | NULL allowed |
|  | Total14xDistinctSubs | bigint |  | 8 | NULL allowed |
|  | LD14xFeesAmount | money |  | 8 | NULL allowed |
|  | USD14xFeesAmount | money |  | 8 | NULL allowed |
|  | Total14xFeesAmount | money | YES | 8 | NULL allowed |
|  | LDGPRSAmount | money |  | 8 | NULL allowed |
|  | USDGPRSAmount | money |  | 8 | NULL allowed |
|  | TotalGPRSAmount | money | YES | 8 | NULL allowed |
|  | USDtoLDMoveDistintSubs | bigint |  | 8 | NULL allowed |
|  | LDtoUSDMoveDistintSubs | bigint |  | 8 | NULL allowed |
|  | TotalMoves | bigint |  | 8 | NULL allowed |
|  | TotalMovesDistinctSubs | bigint |  | 8 | NULL allowed |


---

## <a name="#computedcolumns"></a>Computed columns

| Name | Column definition |
|---|---|
| TotalDistinctSubs | ((isnull([LDDistinctSubs],(0))+isnull([USDDistinctSubs],(0)))+isnull([LDUSDDistinctSubs],(0))) |
| TotalOnNetMinutes | (isnull([LDOnNetMinutes],(0))+isnull([USDOnNetMinutes],(0))) |
| TotalOffNetMinutes | (isnull([LDOffNetMinutes],(0))+isnull([USDOffNetMinutes],(0))) |
| TotalIntlMinutes | (isnull([LDIntlMinutes],(0))+isnull([USDIntlMinutes],(0))) |
| TotalLDMinutes | ((isnull([LDOnNetMinutes],(0))+isnull([LDOffNetMinutes],(0)))+isnull([LDIntlMinutes],(0))) |
| TotalUSDMinutes | ((isnull([USDOnNetMinutes],(0))+isnull([USDOffNetMinutes],(0)))+isnull([USDIntlMinutes],(0))) |
| TotalMinutes | (((((isnull([LDOnNetMinutes],(0))+isnull([LDOffNetMinutes],(0)))+isnull([LDIntlMinutes],(0)))+isnull([USDOnNetMinutes],(0)))+isnull([USDOffNetMinutes],(0)))+isnull([USDIntlMinutes],(0))) |
| TotalNCalls | ([LDNCalls]+[USDNCalls]) |
| TotalRechargesAmount | (isnull([LDRechargesAmount],(0))+isnull([USDRechargesAmount],(0))) |
| TotalOnNetConsumed | (isnull([LDOnNetConsumedAmount],(0))+isnull([USDOnNetConsumedAmount],(0))) |
| TotalOffNetConsumed | (isnull([LDOffNetConsumedAmount],(0))+isnull([USDOffNetConsumedAmount],(0))) |
| TotalIntlConsumed | (isnull([LDIntlConsumedAmount],(0))+isnull([USDIntlConsumedAmount],(0))) |
| TotalLDConsumedAmount | ((isnull([LDOnNetConsumedAmount],(0))+isnull([LDOffNetConsumedAmount],(0)))+isnull([LDIntlConsumedAmount],(0))) |
| TotalUSDConsumedAmount | ((isnull([USDOnNetConsumedAmount],(0))+isnull([USDOffNetConsumedAmount],(0)))+isnull([USDIntlConsumedAmount],(0))) |
| TotalConsumedAmount | (((((isnull([LDOnNetConsumedAmount],(0))+isnull([LDOffNetConsumedAmount],(0)))+isnull([LDIntlConsumedAmount],(0)))+isnull([USDOnNetConsumedAmount],(0)))+isnull([USDOffNetConsumedAmount],(0)))+isnull([USDIntlConsumedAmount],(0))) |
| LDvsUSDConsumptionRate | (CONVERT([decimal](5,2),case  when (isnull([USDOnNetConsumedAmount],(0))+isnull([USDOffNetConsumedAmount],(0)))+isnull([USDIntlConsumedAmount],(0))=(0) then (0) else ((isnull([LDOnNetConsumedAmount],(0))+isnull([LDOffNetConsumedAmount],(0)))+isnull([LDIntlConsumedAmount],(0)))/((isnull([USDOnNetConsumedAmount],(0))+isnull([USDOffNetConsumedAmount],(0)))+isnull([USDIntlConsumedAmount],(0))) end,(0))) |
| TotalSMSConsumedAmount | (isnull([LDSMSConsumedAmount],(0))+isnull([USDSMSConsumedAmount],(0))) |
| Total14xFeesAmount | (isnull([LD14xFeesAmount],(0))+isnull([USD14xFeesAmount],(0))) |
| TotalGPRSAmount | (isnull([LDGPRSAmount],(0))+isnull([USDGPRSAmount],(0))) |


---

## <a name="#indexes"></a>Indexes

| Key | Name | Key Columns | Unique |
|---|---|---|---|
| [![Cluster Primary Key PK_LDvsUSDReport: IDDimDate](../../../../Images/pkcluster.png)](#indexes) | PK_LDvsUSDReport | IDDimDate | YES |


---

###### Author:  MIS

###### Copyright 2021 - All Rights Reserved

###### Created: Sunday, July 4, 2021 9:38:37 PM

