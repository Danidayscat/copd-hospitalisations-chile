# In-hospital mortality and geographical variation in COPD hospitalisations in Chile, 2019–2024

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23923781.svg)](https://doi.org/10.5281/zenodo.23923781)

Analysis code for the article:

> Díaz-Catalán D, Valentino G, Vidal-Vargas N, Yarza Saez MB, Peñailillo L, Vásquez-Muñoz M. In-hospital mortality and geographical variation in COPD hospitalisations in Chile, 2019–2024: a nationwide retrospective cohort study. Submitted to *The Lancet Regional Health – Americas*.

## Overview

This repository contains a single R Markdown file (`paper_copd_LRH.Rmd`) that reproduces all analyses, tables, figures, and appendix material of the article, in their order of appearance. The study used patient-level discharge data from the diagnosis-related group (DRG) database of Chile's National Health Fund (FONASA) to analyse 30 286 COPD hospitalisation episodes from 23 201 patients aged 40 years or older admitted to public hospitals between 2019 and 2024.

The code implements:

- cohort selection with sequential exclusions and a study flow diagram;
- Charlson and Elixhauser comorbidity indices (Quan ICD-10 coding algorithms; van Walraven weights);
- multivariable logistic regression for in-hospital death with patient-clustered robust standard errors;
- analysis of in-hospital mortality by FONASA income tier;
- Aalen–Johansen cumulative incidence of in-hospital death, with discharge alive as a competing event (Gray's test);
- quantile regression of length of stay with jittering and patient-clustered bootstrap;
- national and provincial hospitalisation rates per 100 000 person-years, with exact Poisson CIs and maps.

## Data

The data are **not included** in this repository. The consolidated analytic dataset can be requested from CADS, Universidad Mayor; it was derived from the annual DRG discharge databases, which are publicly available from FONASA. See [`data/README.md`](data/README.md) for details and the required files.

Variable names and category labels from the source databases are in Spanish (for example, `SEXO == "MUJER"` or `TIPOALTA == "FALLECIDO"`) and are kept unchanged in the code; all comments, outputs, tables, and figures are in English.

## Requirements

- R (version 4.5.3 was used)
- RStudio or Quarto/knitr to render R Markdown
- The R packages listed in the `packages` chunk, which are installed automatically if missing. The full session information is printed at the end of the rendered report.

## How to run

1. Clone or download this repository.
2. Place the required data files in the `data/` folder (see `data/README.md`).
3. Open `copd-hospitalisations-chile.Rproj` in RStudio.
4. Open `paper_copd_LRH.Rmd` and click **Knit** (or run `rmarkdown::render("paper_copd_LRH.Rmd")`).

The quantile regression bootstrap (chunk `los_quantreg`) is cached and may take several minutes the first time.

## Outputs

| Folder | Files |
|---|---|
| `figures/` | `Figure_1.png` (flow diagram), `Figure_2_cif.png`, `Figure_3_map.png`, `Figure_S1_cif_tier.png` |
| `tables/` | `Tables_main.docx` (Tables 1–3), `Appendix_tables.docx` (Tables S1–S7) |

Rendering also produces an HTML report with all intermediate checks.

## Citation

If you use this code, please cite the article and this repository (see [`CITATION.cff`](CITATION.cff) or the Zenodo record: https://doi.org/10.5281/zenodo.23923781).

## Funding

Chilean National Agency for Research and Development (ANID), FONDECYT grant 1260589.

## License

Code released under the MIT License (see [`LICENSE`](LICENSE)).

## Contact

Daniela Díaz-Catalán — daniela.diazca@umayor.cl
Prof Luis Peñailillo (corresponding author) — luis.penailillo@unab.cl
