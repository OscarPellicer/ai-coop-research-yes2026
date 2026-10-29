---
marp: true
theme: a4
paginate: false
html: true
---

# AI in research: a one-page checklist

*ICA CCR Europe 2026 · YES Workshop · O. J. Pellicer Valero (Universitat de València)*

## Before using an AI tool

- ☐ **What data am I giving it?** 🟢 public / my own non-sensitive text / code → any tool · 🟡 pseudonymised transcripts, unpublished work → enterprise/institutional tool with a DPA, if the DPO agrees · 🔴 raw audio, identifiable or special-category data (union membership, politics, health), others' manuscripts, student work with names → local tools only, or no AI
- ☐ **Which plan am I on?** Consumer plans (free *and* paid personal) may train on your data → check the settings. Business/Enterprise/Edu/API: no training by default.
- ☐ **Does my consent form / ethics approval cover it?** If not, don't, and fix it for the next study.

## While using it

- ☐ Literature: start from tools grounded in real papers (Semantic Scholar, Elicit, Consensus, Scite, NotebookLM). **Open every paper you cite.**
- ☐ Code: work on a copy or in **git**; ask for a plan first; **review every change**; re-run from scratch. Make sure you can explain every line.
- ☐ Qualitative: AI as a *second reader* with **your** codebook; check that quotes are verbatim; record tool, version and prompts.
- ☐ Agents (Claude Code, Codex): keep personal data **out** of the folder; read commands before approving them; write rules in `CLAUDE.md` / `AGENTS.md`.
- ☐ Keep a **log**: tool, model version, date, purpose, prompts.

## Before submitting

- ☐ Every reference exists and its DOI resolves; details are correct
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
