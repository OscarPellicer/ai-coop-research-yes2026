# Using AI in research, publishing and teaching (without getting burned)

Materials for the session at the **Young and Emerging Scholars (YES) Workshop**, ICA CCR Europe Research Conference 2026 (Valencia, 3 November 2026).

Oscar José Pellicer Valero · Universitat de València · Oscar.Pellicer@uv.es

## Contents

| File | What it is |
|:--|:--|
| [`slides.pdf`](slides.pdf) | The slides ([`slides.md`](slides.md) is the Marp source) |
| [`checklist_a4.pdf`](checklist_a4.pdf) | One-page checklist: before using AI, while using it, before submitting |
| [`handson/coops_panel.csv`](handson/coops_panel.csv) | **Hands-on 2A**: real panel of cooperatives, cooperative workers and unemployment, 52 Spanish provinces × 26 quarters (2020Q1–2026Q2). See [`coops_panel_README.md`](handson/coops_panel_README.md) |
| [`handson/interview_excerpt.md`](handson/interview_excerpt.md) | **Hands-on 2B & 3**: excerpt of a real, public oral-history interview with a cooperative manager. See [`interview_README.md`](handson/interview_README.md) |

## Hands-on prompts

**1 · Is the AI's literature map your map?** Ask an assistant with web search on:

```text
What are the 5 most important academic papers on [the counter-cyclical behaviour of
worker cooperatives | member participation in housing cooperatives | the performance of
agricultural cooperatives]? Give full references with DOI and a one-paragraph synthesis.
```

Check: do they exist, are they the ones you would choose, what is missing, and does the synthesis describe a paper you know well correctly?

**2A · Econometrics.** Upload `coops_panel.csv` and ask:

```text
I want to test whether cooperatives grow more when unemployment is high (the
"counter-cyclical" hypothesis). Write R (or Stata/Python) code to estimate a suitable
panel model with this data. Explain each choice.
```

Then ask it to criticise its own specification.

**2B · Qualitative.** Paste the interview excerpt and ask:

```text
Act as a qualitative researcher. Perform an inductive thematic analysis of this interview
excerpt. Give 4-6 themes, a definition for each and 1-2 supporting quotes (verbatim).
```

Check that the quotes are really verbatim.

**3 · Pseudonymise, then disclose.** Mark everything in the excerpt that could identify a person (without AI), then write the AI-use statement for your current paper.

## Sources and licences

- Cooperatives data: Ministerio de Trabajo y Economía Social, *Estadística de Entidades de Economía Social inscritas en la Seguridad Social*. Unemployment: INE, EPA (table 65349). Reusable public-sector information (Ley 37/2007); cite the source.
- Interview: Halpern, B. (2016). *Louis Schwing: Interview Transcript, Part 1*. Eastern Illinois University, The Keep. CC BY-NC-ND 3.0. Use it for practice only; do not redistribute modified versions.
- Photos: Wikimedia Commons, see [`imgs/CREDITS.md`](imgs/CREDITS.md).
- Slides built with Marp and the template at <https://github.com/OscarPellicer/marp_template>.

Unless otherwise stated, the slides and checklist are licensed under CC BY 4.0.
