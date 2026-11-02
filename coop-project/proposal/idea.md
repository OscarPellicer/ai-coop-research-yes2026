# Proposal notes (rough, for the memoria)

> FICTIONAL. The researcher, research group and project below are invented for a teaching demo. Any resemblance to real people or groups is unintended. The data sources are real.

## Basics
- working title: "Cooperatives over the business cycle: entry and employment of Spanish cooperatives, 2008-2026"
- acronym: COOPCYCLE (alt: ANTICYCLE? too cute)
- PI: Dr. Ana Ferrer (FICTIONAL), postdoc, PhD 2022 in applied economics, thesis on worker co-ops & local labour markets
- host: "Social Economy & Labour Markets" research group (fictional), Faculty of Economics, a Valencian public university
- modality: non-oriented research (investigación no orientada), type A (young PI)
- duration: 36 months (AEI PID: 3 or 4 years)
- budget rough: ~60k direct costs -> under 100k so English optional, but write in English anyway

## Why / gap
- old idea (Ben-Ner 1988; Pérotin 2006): co-ops created more in downturns, "defensive" creation, workers buy out failing firms, employment smoothing (cut wages not jobs)
- evidence mostly France, Italy, Uruguay; Spain = big co-op sector but almost no province-level panel evidence
- 2008 crisis + 2020 COVID + recovery = 2 big downturns in one window, nice variation across 52 provinces
- most studies look at stocks, not entry -> we do both (entry vs stock vs employment)
- hypothesis: co-op entry rises with unemployment (counter-cyclical), co-op employment falls less than conventional firms in downturns; effect stronger for worker co-ops / self-employed-only co-ops

## Objectives
- O1 build harmonised province x quarter panel of co-ops + co-op workers 2008-2026
- O2 estimate cyclicality of co-op entry and employment (vs. all firms)
- O3 heterogeneity: co-op type, sector (agri vs services), region
- O4 understand the mechanism: why do people found a co-op in a crisis? (interviews)
- O5 open dataset + policy brief for regional social-economy policy

## Research questions
- RQ1 does co-op entry go up when provincial unemployment goes up?
- RQ2 is co-op employment less pro-cyclical than total employment?
- RQ3 is it "necessity" (no other jobs) or "opportunity" + public support (capitalización del paro, regional grants)?
- RQ4 did 2008 and 2020 look different? (COVID = ERTEs, very different shock)

## Data
- Ministerio de Trabajo, Estadística de Entidades de Economía Social inscritas en la Seg. Social (ESI): co-ops, workers, by province, quarterly. New method from 2020Q1; pre-2020 only PDFs, different method -> harmonisation needed!!
- INE EPA: unemployment & activity rate by province (table 65349)
- INE DIRCE / Seg. Social affiliation for all-firm benchmark
- regional registries of co-ops for new registrations (entry) - check which CCAA publish this
- pilot panel 2020Q1-2026Q2 already built (data/coops_panel.csv), 1,352 obs

## Methods
- panel, province + quarter FE, SEs clustered by province
- dep vars: log co-ops, log co-op workers, entry rate, growth y-o-y
- regressors: unemployment rate, lagged; Bartik/shift-share for exogenous local demand shock (national sector shocks x pre-2008 sector mix)
- event study around 2008 and 2020
- seasonality (agri co-ops Almería, Huelva) -> y-o-y diffs
- robustness: drop Ceuta/Melilla, weighted by population
- quali: ~20 semi-structured interviews w/ founders of co-ops created 2009-2013 and 2020-2022, Valencian Community + 1 other region; thematic analysis, codebook, consent + pseudonymisation, DMP

## Critical points / contingency
- pre-2020 data harmonisation might fail -> fallback: two separate windows, national series
- entry data patchy by region -> use net change in stock as proxy
- interview recruitment -> via regional co-op federations

## Work plan (36 m)
- WP1 data & harmonisation: m1-9
- WP2 econometrics: m7-24
- WP3 interviews: m10-27 (fieldwork m13-21)
- WP4 synthesis, papers, policy brief, open data: m22-36
- WP5 management & dissemination: m1-36
- milestones: panel released m12, WP paper 1 m21, final workshop m33

## Impact
- science: first long province-level evidence for Spain; 2 papers (econ journal + co-op journal, e.g. Annals of Public and Cooperative Economics), open access
- policy: does co-op support work as an anti-crisis tool? -> regional gov, federations
- open data on Zenodo, code on GitHub
- dissemination: ICA CCR conference, workshop with co-op federations, blog, 1 talk for co-op members
- gender: share of women in co-op jobs, by cycle (variable exists in ESI)
