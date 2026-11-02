# Using AI in research, publishing and teaching

Materials for the session at the **Young and Emerging Scholars (YES) Workshop**, ICA CCR Europe Research Conference 2026 (Valencia, 3 November 2026).

Oscar José Pellicer Valero · Universitat de València · Oscar.Pellicer@uv.es

## Contents

| File | What it is |
|:--|:--|
| [`slides.pdf`](slides.pdf) | The slides ([`slides.md`](slides.md) is the Marp source) |
| [`checklist_a4.pdf`](checklist_a4.pdf) | One-page checklist: before using AI, while using it, before submitting |
| [`coop-project/`](coop-project/) | The project folder we build during the session. Open it in VS Code with Claude Code or Codex to follow along |
| [`coop-project/papers/`](coop-project/papers/) | Open-access papers on cooperatives and the business cycle (live 1). See its README for references and licences |
| [`coop-project/data/coops_panel.csv`](coop-project/data/coops_panel.csv) | Real panel of cooperatives, cooperative workers and unemployment, 52 Spanish provinces × 26 quarters (2020Q1–2026Q2) (hands-on 2). See [`data/README.md`](coop-project/data/README.md) |
| [`coop-project/interviews/interview_excerpt.md`](coop-project/interviews/interview_excerpt.md) | Excerpt of a real, public oral-history interview with a cooperative manager (hands-on 3). Codebook and notes in [`interviews/README.md`](coop-project/interviews/README.md) |
| [`coop-project/proposal/`](coop-project/proposal/) | Official Word template of the AEI 2025 call and rough notes for a fictional proposal (live 3) |

## How to follow along

- **Minimum**: any AI assistant in the browser (Claude, ChatGPT, Gemini). Upload the files when the prompts mention them.
- **Better**: [VS Code](https://code.visualstudio.com) with the Claude Code or Codex extension, and [Miniconda](https://www.anaconda.com/download/success?reg=skipped-miniconda) for Python. Download this repository (Code → Download ZIP) and open the `coop-project/` folder.

## Prompts

### Hands-on 1 · Is the AI's literature map your map?

With web search on:

```text
What are the 5 most important academic papers on [the counter-cyclical behaviour of worker
cooperatives | member participation in housing cooperatives | the performance of agricultural
cooperatives]? Give full references with DOI and a one-paragraph synthesis.
```

```text
Which important work is missing from this list? Look at Spanish-language journals
(CIRIEC-España, REVESCO) and reports (ICA, Euricse, CICOPA). Which of the papers are open access?
```

Check: do the DOIs resolve, are these the papers you would choose, does the synthesis of a paper you know well get it right? Compare with your neighbour.

### Live 1 · From PDFs to a literature table

```text
Convert every PDF in papers/ to Markdown with the document2md skill
(github.com/OscarPellicer/document2md) and save them in papers/md/.
If a paper is on arXiv, download its LaTeX source instead.
```

```text
Write notes/literature.md with a table: research question, data, method and main finding of each
paper, with the page of each claim. Which papers support the counter-cyclical hypothesis?
```

### Hands-on 2 · Econometrics, prompt by prompt

```text
Set this folder up as a project: code/, output/, paper/, a CLAUDE.md and git. Use Python.
Explore data/coops_panel.csv and report any problems. Never modify the raw data.
```

```text
I want to test whether cooperatives grow more when unemployment is high (the "counter-cyclical"
hypothesis). Write a Python script that estimates a suitable panel model. Explain each choice.
Ask me before dropping any observation.
```

```text
The data are quarterly and the chart shows a strong seasonal pattern. Add quarter and time fixed
effects. What happens to the coefficient?
```

```text
The literature is about the entry of new co-ops, and this panel has stocks. Re-estimate with the
net change in the number of cooperatives.
```

```text
Cluster the standard errors by province and explain why. Could causality run the other way?
What can and can't this data tell us?
```

```text
Save one figure and one LaTeX table with all the specifications in output/. Write in CLAUDE.md
what we decided and why.
```

### Hands-on 3 · Thematic coding of a real interview

```text
Act as a qualitative researcher. Perform an inductive thematic analysis of this interview excerpt.
Give 4-6 themes, a definition for each and 1-2 supporting quotes (verbatim, with line numbers).
```

```text
Now code it again using ONLY the codebook in interviews/README.md. Which passages contradict
the themes you found?
```

Check that the quotes are really verbatim.

### Writing loop

```text
Launch a review agent that reads paper/ as a referee for J. of Co-operative Organization and
Management. It must not edit; it lists the problems by severity.
```

### Live 3 · A Word template, filled in LaTeX

```text
Convert proposal/template.docx to LaTeX, keeping the layout as close as possible
(without the logos). Compile it to PDF and show me the differences with the original.
```

```text
Fill in sections 2.2 (justification and hypothesis) and 3.1 (objectives) from proposal/idea.md,
notes/literature.md and the results in output/.
Do not add anything that is not in those files; mark the gaps with TODO.
```

## Sources and licences

- Papers: see [`coop-project/papers/README.md`](coop-project/papers/README.md). Each is redistributed under its own open licence.
- Cooperatives data: Ministerio de Trabajo y Economía Social, *Estadística de Entidades de Economía Social inscritas en la Seguridad Social*. Unemployment: INE, EPA (table 65349). Reusable public-sector information (Ley 37/2007); cite the source.
- Interview: Halpern, B. (2016). *Louis Schwing: Interview Transcript, Part 1*. Eastern Illinois University, The Keep. CC BY-NC-ND 3.0. Use it for practice only; do not redistribute modified versions.
- Proposal template: Agencia Estatal de Investigación, *Memoria Científico-Técnica*, Proyectos de Generación de Conocimiento 2025. Reproduced unchanged, citing its origin. The proposal notes in `idea.md` are fictional.
- Photos: Wikimedia Commons, see [`imgs/CREDITS.md`](imgs/CREDITS.md).
- Slides built with Marp and the template at <https://github.com/OscarPellicer/marp_template>.

Unless otherwise stated, the slides and checklist are licensed under CC BY 4.0.
