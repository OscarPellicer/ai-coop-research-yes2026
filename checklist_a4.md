---
marp: true
theme: a4
paginate: false
html: true
---

# AI in research: a one-page checklist

*ICA CCR Europe 2026 · YES Workshop · O. J. Pellicer Valero (Universitat de València)*

## Before using an AI tool

- ☐ **What data am I giving it?** *Green*: public data, your own text, code → any tool. *Amber*: personal data (pseudonymised or not), unpublished work → only a Team/Enterprise/API plan with a DPA, with a legal basis, an Art. 9 exception for special categories, informed participants and your DPO's approval. *Red*: personal data in a free or personal plan, others' manuscripts under review → never; use a local tool.
- ☐ **Which plan am I on?** Free and personal plans (Pro, Plus) follow consumer terms and may train on your data. Team/Business/Enterprise/API: no training by default and a DPA. Researchers: apply for the **Claude Team plan for scientists**.
- ☐ **Does my consent form / ethics approval cover it?** If not, don't, and fix it for the next study.

## While using it

- ☐ Literature: let the agent search and map the field, then **read every paper you cite**. Look for what it misses (non-English journals, reports).
- ☐ Code: work on a copy or in **git**; ask for a plan first; **review every change**; re-run from scratch. Make sure you can explain every line.
- ☐ Qualitative: AI as a *second reader* with **your** codebook; check that quotes are verbatim; record tool, version and prompts.
- ☐ Agents (Claude Code, Codex): keep personal data **out** of the folder; read commands before approving them; write rules in `CLAUDE.md` / `AGENTS.md`.
- ☐ Keep a **log**: tool, model version, date, purpose, prompts.

## Before submitting

- ☐ Every cited paper read; every DOI resolves
- ☐ Every number in the text is traceable to a script output
- ☐ The replication package runs from scratch
- ☐ **AI-use statement** written following **this journal's current** policy
- ☐ No AI-generated figures/images (unless explicitly allowed)
- ☐ As a reviewer: **never** upload the manuscript to an AI tool

## AI-use statement template

```text
During the preparation of this work the authors used <tool> (<provider>, <model/version>,
accessed <month year>) to <purpose: language editing / code assistance / ...>.
<What was verified and how.> <How data was protected, if relevant.>
The authors reviewed and edited the output and take full responsibility for the content.
```

## Teaching

- ☐ Rules on AI use written **in the syllabus**, per assignment
- ☐ Assessment that does not depend on detectors (they are unreliable and biased against non-native writers)
- ☐ No student work with names in consumer tools
