# Data

The data files are **not included** in this repository.

## Analytic dataset

The consolidated analytic dataset (`consolidated_data_COPD.rds`) is available from the Center for Health Data Observation and Analysis (CADS), Vice-Rectorate for Research, Universidad Mayor, Santiago, Chile, upon reasonable request and in accordance with its data access protocol (https://www.umayor.cl/um/cads).

To request the data, contact cads@umayor.cl.

## Source data

The dataset was derived from the annual DRG discharge databases of the Chilean National Health Fund (FONASA) for 2019–2024, which are publicly available from the FONASA DRG dashboard: https://public.tableau.com/views/PropuestaTableroGRD/PropuestaTableroGRD

It includes all discharge episodes with a principal diagnosis of COPD (ICD-10 J44.0, J44.1, J44.8, or J44.9), with diagnoses, procedures, and an anonymised patient identifier linking episodes from the same patient. Exclusions by study period, age, sex, province, insurance, and length of stay are applied in `paper_copd_LRH.Rmd`.

## Required files

Place the following files in this folder:

| File name (exact) | Content | Source |
|---|---|---|
| `consolidated_data_COPD.rds` | COPD discharge episodes (principal diagnosis J44.0, J44.1, J44.8, or J44.9), 2019–2024 | CADS, upon request (derived from the FONASA DRG databases) |
| `Norma MINSAL 2014_definitivo.xlsx` | 2014 MINSAL length-of-stay reference standard by DRG (sheet "PC IRGRD incluidos") | Chilean Ministry of Health (MINSAL) |
| `Tablas maestras bases GRD .xlsx` | FONASA DRG master tables (sheet "Hospitales": hospital codes and names) | FONASA |
| `estimaciones-y-proyecciones-2002-2035-comunas.xlsx` | Population estimates and projections by municipality, sex, and age, 2002–2035 | Chilean National Statistics Institute (INE), www.ine.gob.cl |

File names must match exactly, including spaces.
