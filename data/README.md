# Data

The data files are **not included** in this repository. They can be obtained in two ways.

## Option A: request the consolidated dataset from CADS (recommended)

The consolidated analytic dataset (`consolidated_data_COPD.rds`) is available from the Center for Health Data Observation and Analysis (CADS), Vice-Rectorate for Research, Universidad Mayor, Santiago, Chile, upon reasonable request and in accordance with its data access protocol.

To request the data: cads@umayor.cl.

With this file, only the files marked with an asterisk (*) in the table below are additionally needed to run `paper_copd_LRH.Rmd`.

## Option B: rebuild the dataset from the public DRG databases

The annual DRG discharge databases of the Chilean National Health Fund (FONASA) are publicly available from the FONASA DRG dashboard: https://public.tableau.com/views/PropuestaTableroGRD/PropuestaTableroGRD


## Required files

The analysis requires the following files in this folder. They are not included in the repository.

| File name (as read by the code) | Content | Source |
|---|---|---|
| `consolidated_data_COPD.rds` | FONASA DRG discharge episodes with a principal diagnosis of COPD (ICD-10 J44), 2019–2024 | FONASA, https://public.tableau.com/views/PropuestaTableroGRD/PropuestaTableroGRD |
| `Norma MINSAL 2014_definitivo.xlsx` | 2014 MINSAL length-of-stay reference standard by DRG (sheet "PC IRGRD incluidos") | Chilean Ministry of Health (MINSAL) |
| `Tablas maestras bases GRD .xlsx` | FONASA DRG master tables (sheet "Hospitales": hospital codes and names) | FONASA |
| `estimaciones-y-proyecciones-2002-2035-comunas.xlsx` | Population estimates and projections by municipality, sex, and age, 2002–2035 | Chilean National Statistics Institute (INE), www.ine.gob.cl |

File names must match exactly, including spaces.
