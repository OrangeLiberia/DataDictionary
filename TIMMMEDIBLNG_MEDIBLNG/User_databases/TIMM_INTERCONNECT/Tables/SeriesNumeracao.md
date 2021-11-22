#### 

[Project](../../../../index.md) > [192.168.19.11\\MEDIBLNG](../../../index.md) > [User databases](../../index.md) > [TIMM_INTERCONNECT](../index.md) > [Tables](Tables.md) > dbo.SeriesNumeracao

# ![Tables](../../../../Images/Table32.png) [dbo].[SeriesNumeracao]

---

## <a name="#properties"></a>Properties

| Property | Value |
|---|---|
| Collation | Latin1_General_CI_AS |


---

## <a name="#columns"></a>Columns

| Name | Data Type | Max Length (Bytes) | Nullability | Identity |
|---|---|---|---|---|
| IdSerieNumeracao | int | 4 | NOT NULL | 1 - 1 |
| Serie | varchar(50) | 50 | NOT NULL |  |
| idFilial | int | 4 | NULL allowed |  |
| Ano | int | 4 | NULL allowed |  |
| Valor | bigint | 8 | NOT NULL |  |
| Descricao | varchar(50) | 50 | NULL allowed |  |
| TipoSerie | int | 4 | NULL allowed |  |
| Parametro1 | varchar(20) | 20 | NOT NULL |  |
| Separador1 | varchar(10) | 10 | NULL allowed |  |
| Parametro2 | varchar(20) | 20 | NOT NULL |  |
| Separador2 | varchar(10) | 10 | NULL allowed |  |
| Parametro3 | varchar(20) | 20 | NOT NULL |  |
| NumDigitos | int | 4 | NULL allowed |  |


---

###### Author:  MIS Team

###### Copyright 2021 - All Rights Reserved

###### Created: Monday, November 22, 2021 4:40:59 PM

