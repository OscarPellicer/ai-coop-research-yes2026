# coops_panel.csv: Spanish cooperatives and unemployment, province × quarter, 2020Q1–2026Q2

A real, open panel for a hands-on exercise. It gives the number of cooperatives (and their workers) registered in Spanish Social Security for each of the 52 provinces and each quarter, merged with the provincial EPA unemployment rate.

- **Rows:** 1,352 (52 provinces × 26 quarters, balanced, no missing values)
- **Columns:** 15
- **Unit of observation:** province–quarter. The file is in tidy long format, one row per province and quarter.

## Sources

1. **Cooperatives:** Ministerio de Trabajo y Economía Social (MITES), *Estadística de Entidades de Economía Social inscritas en la Seguridad Social (ESI)*.
   - Landing page: https://www.mites.gob.es/es/estadisticas/mercado_trabajo/EESSS/welcome.htm
   - Files used:
     - Quarterly workbooks 2020–2024: `https://www.mites.gob.es/estadisticas/ESI/ESI_{q}T_{yyyy}.xlsx`
     - Monthly workbooks 2025–2026: `https://www.mites.gob.es/estadisticas/ESI/ESI_{mm}_{yyyy}.xlsx`
   - Tables used:
     - ESI-C1: cooperatives by province
     - ESI-C5 (ESI-C6 from 2026): workers of cooperatives by province
   - Methodology: https://www.mites.gob.es/estadisticas/ESI/Notas_metodologicas_ESI.pdf
2. **Unemployment:** INE, *Encuesta de Población Activa (EPA)*, table 65349 "Tasas de actividad, paro y empleo por provincia y sexo" (both sexes).
   - https://www.ine.es/jaxiT3/Tabla.htm?t=65349
   - CSV: https://www.ine.es/jaxiT3/files/t/es/csv_bdsc/65349.csv

Data were downloaded on 2026-10-29.

**Suggested citation:** MITES (2026), *Estadística de Entidades de Economía Social inscritas en la Seguridad Social*; INE (2026), *Encuesta de Población Activa*, table 65349. Compiled by O. Pellicer.

## Licence

Both sources are Spanish public-sector information that you may reuse freely, including commercially, under Ley 37/2007 and RD 1495/2011. The conditions are:

- cite the source;
- do not distort the meaning of the data;
- state the date of the last update.

INE's reuse terms are compatible with CC BY 4.0. See the legal notices:

- MITES: https://www.mites.gob.es/es/extras/avisolegal.htm
- INE: https://www.ine.es/aviso_legal

The compiled CSV can be redistributed with the attribution above.

## Variables

| column | description |
|---|---|
| `province_code` | INE province code ("01"–"52"); keep it as a string |
| `province` | Province name (INE spelling) |
| `region` | Autonomous community (English name) |
| `year`, `quarter`, `period` | Time identifiers (`period` = "2020Q1", …) |
| `coops` | Cooperatives registered with Social Security (count; province of the head office) |
| `coops_general` | Cooperatives with at least one non-self-employed worker. It excludes cooperatives formed only by self-employed (RETA) members |
| `coops_selfemp_only` | Cooperatives whose members are all self-employed (RETA). `coops = coops_general + coops_selfemp_only` |
| `coop_workers` | Workers of cooperatives, all Social Security schemes |
| `coop_workers_women` | Of which women |
| `coop_workers_employees` | Of which in the General scheme and other non-RETA schemes (employees and worker-members) |
| `coop_workers_selfemp` | Of which in RETA, the self-employed scheme. `coop_workers = coop_workers_employees + coop_workers_selfemp` |
| `unemployment_rate` | EPA unemployment rate (%), both sexes |
| `activity_rate` | EPA activity rate (%), both sexes |

## How it was built

1. I downloaded all 20 quarterly ESI workbooks for 2020–2024 and the monthly workbooks for 2025–2026. For 2025 onwards, the month that ends each quarter (March, June, September, December) stands for that quarter.
2. I located the two province tables in each workbook by their titles, because sheet numbering changed in 2026.
3. Each single-province region, such as Madrid, Murcia or Navarra, appears only as a region row, and that row was taken as the province.
4. I checked the internal sums for every row: total cooperatives = general + self-employed-only, and total workers = General scheme + RETA. The national totals match the published TOTAL row.
5. I merged the result 1:1 with the INE EPA rates by province name and quarter. All 1,352 rows matched.

The build script is `build_panel.py`, kept outside this folder.

## Sanity check (OLS, SEs clustered by province)

| model | coef. on `unemployment_rate` | SE | p |
|---|---|---|---|
| Pooled OLS, `log(coop_workers)` | −0.011 | 0.038 | 0.77 |
| Province FE, `log(coop_workers)` | −0.0056 | 0.0021 | 0.007 |
| Province + quarter FE, `log(coop_workers)` | −0.0037 | 0.0028 | 0.19 |
| Province + quarter FE, `log(coops)` | 0.0002 | 0.0018 | 0.90 |

In the province fixed-effects model, 1 pp more unemployment goes with about 0.6% fewer cooperative workers. Once common quarter shocks are removed, there is no significant effect. In this short window, the data give no support to the counter-cyclical hypothesis.

## Suggested prompts for attendees

1. *"Here is a CSV panel of Spanish provinces by quarter. Write R (fixest) / Stata (reghdfe) / Python (linearmodels) code to estimate a two-way fixed-effects model of log cooperative employment on the unemployment rate, with standard errors clustered by province. Then list everything that could be wrong with this specification."*
   Things a good critique should raise:
   - reverse causality and simultaneity;
   - a short T (26 quarters), mostly COVID and the recovery;
   - strong seasonality from agricultural cooperatives (Almería, Huelva);
   - EPA sampling noise in small provinces;
   - few clusters per region;
   - stock versus flow (Ben-Ner and Pérotin look at entry and creation, not stocks);
   - Ceuta and Melilla as outliers.
2. *"Do cooperatives grow in crises? Propose and code a better test using these data: for example, year-on-year growth rates, lagged unemployment, or separate effects for cooperatives with only self-employed members. Explain which economic theory (Ben-Ner 1988; Pérotin 2006) each choice tests."*
3. *"Check this dataset before modelling: summarise it, plot coop_workers over time for 3 provinces, and tell me about seasonality, outliers and any structural breaks."*
   Then ask the chatbot to justify every transformation it made.

## Caveats

- **Short window.** The regional series starts in 2020Q1, when the new ESI methodology begins; older data use a different method and are published only as PDFs. In the old series, the 2020 jump in RETA cooperative workers comes from a method change, not a real increase.
- **What a quarter means.**
  - For 2020–2024, each value refers to the quarter as published in the quarterly file.
  - For 2025–2026, each value is the stock in the quarter's last month.
  - The national totals join smoothly at 2024Q4/2025Q1.
- **Location.** Cooperatives are counted by the province of their head office. Workers are counted by the province in the ESI table, and RETA members by where they carry out their activity.
- **Recent data.** EPA figures for 2026 are the latest releases and may be revised.
