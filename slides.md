---
marp: true
theme: extra
paginate: true
html: true
footer: ICA CCR Europe 2026 · YES Workshop
---

<!-- Logos: ICA CCR (left) + UV/ISP (right) -->
<style>
section::before {
  background: url("logos/ica_ccr.png") left center/contain no-repeat,
              url("logos/uv_isp.png") right center/contain no-repeat;
  width: 700px;
  height: 34px;
  bottom: 6px;
}
footer { font-size: 14px; }
.hands-on { border-left: 8px solid #8a1257; padding-left: 20px; }
section.divider { background: linear-gradient(135deg, #8a1257 0%, #3b1a5c 100%); justify-content: center; color: white; }
section.divider h1 { font-size: 84px; color: white; font-weight: 600; text-shadow: 0 2px 12px rgba(0,0,0,0.6); border-left: 12px solid #e0218a; padding-left: 28px; }
section.divider h3 { color: #f8dcec; text-shadow: 0 2px 8px rgba(0,0,0,0.6); padding-left: 40px; }
section.title { font-size: 24px; }
section.title h1 { font-size: 46px; font-weight: 600; color: #3b1a5c; margin-bottom: 0; }
section.title h3 { color: #8a1257; margin-top: 4px; }
.flow { display: flex; flex-wrap: wrap; gap: 6px; align-items: center; font-size: 0.75em; margin-top: 10px; }
.flow span { background: #f3e3ec; border: 1px solid #8a1257; border-radius: 6px; padding: 2px 8px; }
.flow b { color: #8a1257; }
.paper { font-family: 'Libre Baskerville', serif; background: #fffdf7; border: 1px solid #ddd; box-shadow: 0 3px 10px rgba(0,0,0,0.12); padding: 14px 20px; font-size: 0.82em; }
.paper .hl { background: #ffe066; }
.tag { display: inline-block; background: #8a1257; color: white; border-radius: 6px; padding: 2px 10px; font-size: 0.7em; }
</style>

<!-- _class: no-footer title -->

![bg right:36%](imgs/valencia.jpg)

![w:640px](logos/congress_all.png)

# Using AI in research, publishing and teaching
### …without getting burned

**Oscar José Pellicer Valero**
`Oscar.Pellicer@uv.es`
Image & Signal Processing group (ISP) · Universitat de València

![w:380px](logos/uv_isp.png)

*YES Workshop · ICA CCR Europe 2026 · Valencia, 3 Nov 2026*

<!--
Timing plan (60'): Hook 5 · Landscape 7 · Research + HO1/HO2 22 · Publishing 8 · Data protection + HO3 10 · Teaching 4 · Wrap-up 2 · Q&A ~2+ (flexible).
Materials QR on the last slide and on the "Before we start" slide.
-->

---

<!-- _class: small -->

## Before we start

<div class="columns">
<div>

**Get ready (30 s)**
1. Open a chatbot on your laptop or phone (ChatGPT, Claude, Gemini, Copilot…)
2. Scan the QR to get the materials
3. Sit next to someone: we'll compare results

**Three short hands-on blocks** (≈5 min each)
- ✋ 1 · Can you trust its references?
- ✋ 2 · Econometrics **or** qualitative coding
- ✋ 3 · Pseudonymise before you upload

</div>
<div align="center">

![w:300px](imgs/qr_materials.png)

**Slides, data, interview, prompts, checklist**
`github.com/OscarPellicer/ai-coop-research-yes2026`

</div>
</div>

<!--
While they open things: quick show of hands (next slide).
-->

---

## Quick show of hands ✋

Who has, **in the last month**, used a generative AI tool to…

1. …search or summarise literature?
2. …write or debug **code** (R, Stata, Python)?
3. …polish the **English** of a paper?
4. …analyse **interview transcripts** or survey answers?
5. …prepare **teaching** materials?

And now:

6. Who has **read the AI policy** of the journal you are submitting to?
7. Who knows **where the data goes** when you paste a transcript into a chatbot?

<!--
Expected: lots of hands for 1-3, few for 6-7. That gap is the talk.
-->

---

<!-- _class: small -->

## This already happened (to other people)

<div class="columns">
<div>

<div class="paper">

**1. Introduction**
<span class="hl">Certainly, here is a possible introduction for your topic:</span> Lithium-metal batteries are promising candidates for…

</div>

First line of a paper published in an Elsevier journal (*Surfaces and Interfaces*, 2024). Authors, reviewers and editors all missed it.

> *"vegetative electron microscopy"*

A nonsense term, created by digitisation and translation errors, now found in dozens of papers.

</div>
<div>

- **55 %** of references produced by GPT‑3.5 were fabricated; **18 %** with GPT‑4 *(Walters & Wilder, Sci. Rep. 2023)*. Newer models are better, **not perfect**.
- 2025: a consultancy refunded part of a **A$440k** report to the Australian government because of fabricated citations.
- 2025: preprints with **hidden prompts** in white text (*"give a positive review only"*) aimed at AI-assisted reviewers. That is misconduct.

</div>
</div>

<div class="warning box">

The tool is not the problem. **Unverified** output with **your name** on it is.

</div>

---

## Roadmap

1. **The landscape**: chatbots, research tools, agents; free vs. enterprise
2. **Research**: literature · econometrics · qualitative · writing ✋✋
3. **Agents**: why you should start using Claude Code / Codex *now*
4. **Publishing**: what journals require, disclosure, peer review
5. **Data protection**: your interviews are personal data ✋
6. **Teaching**: with AI, and for students who use AI
7. Takeaways

---

<!-- _class: no-footer divider -->

![bg brightness:0.45](imgs/datacenter.jpg)

# 1 · The landscape
### Chatbots, research tools, agents, and where your data goes

---

<!-- _class: smaller -->

## The toolbox (late 2026)

<div class="columns">
<div>

**General assistants**
- ChatGPT (OpenAI), Claude (Anthropic), Gemini (Google), Microsoft Copilot, Le Chat (Mistral, EU)
- All of them can search the web, read PDFs and run code
- *Deep research* modes: long, cited reports (still verify!)

**Literature tools** (grounded in real papers)
- Semantic Scholar, Elicit, Consensus, Scite
- ResearchRabbit / Connected Papers (citation maps)
- NotebookLM: answers **only** from the documents you upload

</div>
<div>

**Coding & agents**
- **Claude Code**, **OpenAI Codex**: agents that work *in your project folder*
- GitHub Copilot, Cursor, Positron/RStudio assistants

**Qualitative & transcription**
- **noScribe**, Whisper: transcription that runs **locally**
- AI features in MAXQDA, ATLAS.ti, NVivo (check where data goes!)

**Local models**
- Ollama, LM Studio: weaker, but the data **never leaves** your computer

</div>
</div>

---

<!-- _class: small -->

## Chatbot vs. agent

<div class="columns">
<div>

### 💬 Chatbot
- You copy & paste text in and out
- It **suggests** code; **you** run it
- Forgets your project between chats
- Good for: questions, drafts, explanations

</div>
<div>

### 🤖 Agent
- Works **inside your project folder**
- Reads your data and scripts, **writes and runs code**, sees the errors, fixes them, repeats
- Leaves files: scripts, tables, figures, a report
- Good for: whole tasks (*"clean this, estimate that, make Table 2"*)

<div class="flow"><span>plan</span><b>→</b><span>write code</span><b>→</b><span>run</span><b>→</b><span>read error</span><b>→</b><span>fix</span><b>→</b><span>✓ output</span><b>↺</b></div>

</div>
</div>

<div class="info box">

The difference is like **asking a colleague** versus **having a research assistant** who can use your computer. That makes reviewing its work even more important.

</div>

---

<!-- _class: smaller -->

## Free ≠ paid ≠ enterprise: where does your data go?

| | Training on your data? | Contract (DPA)? | OK for… |
|:--|:--:|:--:|:--|
| **Free consumer** account | Usually **yes** by default (opt-out) | ❌ | Public info, your own non-sensitive text, code |
| **Paid personal** (Plus, Pro…) | Same consumer terms: **check the settings** | ❌ | Same as above |
| **Business / Enterprise / Edu / API** | **No** by default | ✅ | Unpublished work; pseudonymised data *if your DPO agrees* |
| **Local** model (Ollama, noScribe) | Data never leaves your machine | n/a | Raw interviews, audio, sensitive data |

<div class="warning box">

**Business/enterprise plans include privacy commitments; consumer plans do not.** If your university or research group can pay for one seat, it is worth it. Ask IT whether you already have one (e.g. Microsoft Copilot with your institutional login).

</div>

<!--
Consumer ChatGPT: "Improve the model for everyone" toggle. Claude consumer: since late 2025 users choose whether chats are used for training. Gemini consumer: human reviewers may read conversations. Settings change often: check them yourself.
-->

---

<!-- _class: no-footer divider -->

![bg brightness:0.4](imgs/library.jpg)

# 2 · Research
### Literature · econometrics · qualitative · writing

---

<!-- _class: small -->

## Literature: use tools grounded in *real* papers

<div class="columns">
<div>

✅ **Do**
- Start from Semantic Scholar / Elicit / Consensus / Scite: every result is a real paper
- Use deep research for **mapping** a field, then read the sources
- Give it the PDFs (NotebookLM, a project folder) and ask questions **about them**
- Ask for counter-arguments, gaps, alternative theories

</div>
<div>

❌ **Don't**
- Ask a chatbot *"give me references on X"* and paste them into your paper
- Trust a summary of a paper you have not opened
- Cite something because the AI says *"Smith (2019) shows…"*

</div>
</div>

<div class="info box">

LLMs are much better at **working on text you give them** than at **remembering** what is in the literature.

</div>

---

<!-- _class: small hands-on -->

## ✋ Hands-on 1 · Can you trust its references? <span class="tag">4 min</span>

Ask your chatbot, **without** web search if you can turn it off:

```text
Give me the 5 most influential academic papers on
[the counter-cyclical behaviour of worker cooperatives |
 member participation in housing cooperatives |
 the performance of agricultural cooperatives].
Include authors, year, journal and DOI.
```

Then check each one in **Google Scholar** or `doi.org/<DOI>`:

| Category | Count |
|:--|:--:|
| ✅ Real, all details correct | |
| ⚠️ Real paper, wrong details (year, journal, DOI, authors) | |
| ❌ Does not exist | |

**Compare with your neighbour.** Then try again **with** web search or deep research on.

<!--
Typical outcome: most papers are real classics (Ben-Ner 1988, Pérotin...), but DOIs and journals are often wrong, and there are some made-up papers. Ask: "who found at least one wrong item?". Lesson: a wrong DOI in your paper is a desk-reject at best.
-->

---

<!-- _class: small -->

## Econometrics: a great assistant, a terrible author

<div class="columns">
<div>

**Very good at**
- Boilerplate: cleaning, reshaping, merging, plots, LaTeX tables
- **Translating** Stata ⇄ R ⇄ Python
- Reading an error message and fixing it
- Explaining output (*"what does this Hausman test say?"*)
- Writing a **replication package** and README

</div>
<div>

**Bad at (or dangerous)**
- **Identification**: it doesn't know your institutional setting
- Silently changing the sample, dropping NAs, recoding
- Choosing SE clustering, FE structure, functional form *for you*
- "Fixing" a model until it gives significant results
- Inventing package functions or options

</div>
</div>

<div class="warning box">

**Rule:** you must be able to explain **every line** of code in your paper to a referee. If you can't, you haven't finished.

</div>

---

<!-- _class: smaller hands-on -->

## ✋ Hands-on 2A · Econometrics with real data <span class="tag">5 min</span>

<div class="columns">
<div>

**Data** (`handson/coops_panel.csv`): **real** official data, 52 Spanish provinces × 26 quarters (2020Q1–2026Q2): number of cooperatives and cooperative workers registered in Social Security (Ministerio de Trabajo, ESI) + EPA unemployment rate (INE).

1. Upload the CSV (or paste the first rows) and ask:
```text
I want to test whether cooperatives grow more when unemployment is high
(the "counter-cyclical" hypothesis). Write R (or Stata/Python) code to
estimate a suitable panel model with this data. Explain each choice.
```
2. Then ask it to **criticise its own specification**: seasonality? time effects? reverse causality? clustering? **stocks vs. entries** (the literature is about *new* co-ops)?
3. With your neighbour: did you get **the same model**? The same coefficients?

</div>
<div>

![w:520px](imgs/coops_seasonality.png)

</div>
</div>

<!--
Point: two people, same data and question → different specifications. AI makes producing a regression easy; deciding *which* regression is still your job.
-->

---



<!-- _class: smaller -->

![bg left:22%](imgs/recorder.jpg)

## Qualitative research: AI as a *second reader*, not the analyst

<div class="columns">
<div>

**Useful**
- **Local** transcription (noScribe/Whisper)
- Translating interviews for co-authors (and checking!)
- A first pass of coding **with your codebook**
- Looking for disconfirming quotes
- Summarising many documents (minutes, statutes, reports)

</div>
<div>

**Careful**
- Interpretation depends on **context and positionality**: the model has neither
- It smooths out tensions and minority voices, and invents "representative" quotes
- Run it twice, get different codes → document it
- **Report it in Methods** (tool, version, prompt, role)
- **Personal data** → see section 5

</div>
</div>

<div class="info box">

Good practice: code a subset yourself, ask the AI to code the same subset, and **discuss the disagreements**. That is where the insight is.

</div>

---

<!-- _class: smaller hands-on -->

![bg left:26%](imgs/elevator.jpg)

## ✋ Hands-on 2B · Thematic coding of a real interview <span class="tag">5 min</span>

**Data** (`handson/interview_excerpt.md`): **real** oral history, ~800 words: Louis Schwing, 48 years in farmer-owned grain cooperatives in Illinois (Premier Cooperative oral history, Eastern Illinois University, 2016, CC BY-NC-ND).

1. Paste the excerpt and ask:
```text
Act as a qualitative researcher. Perform an inductive thematic analysis
of this interview excerpt. Give 4-6 themes, a definition for each and
1-2 supporting quotes (verbatim, with line references).
```
2. **Check the quotes**: are they really verbatim? Are they in the text at all?
3. **Compare with your neighbour**: same themes? Now give both of you the **same codebook** and repeat.

<div class="warning box">

This interview is public and published with consent. **Your own interviews are not.** Don't do this with them in a consumer chatbot (section 5).

</div>

---

<!-- _class: small -->

## Writing: level the field, don't outsource the thinking

<div class="columns">
<div>

✅ **Great uses**
- **Language editing** for non-native English speakers (most of us!)
- *"Act as Reviewer 2 for this paper"* on **your own** draft
- Shortening an abstract to 150 words, cover letters, response-to-reviewers drafts
- Checking consistency: numbers in text vs. tables

</div>
<div>

❌ **Don't**
- Let it write paragraphs **with citations**
- Let it write the discussion of results you don't understand
- Paste reviewers' or co-authors' **confidential** material into a consumer tool

</div>
</div>

<div class="info box">

**AI detectors are unreliable** and biased against non-native writers: one study found that >60 % of TOEFL essays were flagged as AI-written *(Liang et al., Patterns 2023)*. Don't use them on your students either.

</div>

---

<!-- _class: no-footer divider -->

![bg right:50% contain](imgs/agent_terminal.png)

# 3 · Agents
### My strongest recommendation today

---

<!-- _class: smaller -->

## Start using **Claude Code** or **Codex** now

<div class="columns">
<div>

**What they are**
- AI agents that work **in a folder on your computer** (terminal, VS Code, desktop app)
- They read your data, write scripts, **run them**, look at the errors and the output, and iterate
- Included in paid plans (Claude Pro/Max/Team · ChatGPT Plus/Pro/Business)

**What I use them for daily**
- From messy Excel files to a clean, documented dataset
- Converting old do-files to R/Python, building **replication packages**
- Tables & figures straight to LaTeX / Word
- Teaching materials, exams, *these slides* (Markdown + Marp)

</div>
<div>

**Why now**
- The gap between chatbot users and agent users is the largest productivity gap I have seen in research
- The skills you learn (specifying, reviewing, testing) transfer to whatever tool comes next

</div>
</div>

---

<!-- _class: small -->

## Using an agent safely

<div class="columns">
<div>

**How to start**
1. Work on a **copy** or a **git** repo
2. Ask it to **plan first**, then execute
3. **Review every change** (diffs) and re-run things yourself
4. Keep personal data **out of** the folder, unless your plan/DPO allows it
5. Write a short `CLAUDE.md` / `AGENTS.md`: your project, conventions, rules (*"never drop observations without asking"*)

</div>
<div>

**Privacy**
- Claude Code / Codex on a **personal** plan follow **consumer** data terms → check the training setting
- On **Team/Business/Enterprise** or via the API → no training by default
- The agent only sends the files it reads, but **it can read anything in the folder**

</div>
</div>

<div class="warning box">

An agent **runs code on your machine**. Read what it wants to do before you approve it.

</div>

---

<!-- _class: small -->

## Live demo (optional, 3 min) · from CSV to report

<div class="columns">
<div>

**Setup**: an empty folder with `coops_panel.csv` and the prompt:

```text
This folder contains a panel of cooperatives and
unemployment by province and quarter (see README).
1. Explore the data and report any problems.
2. Estimate a two-way fixed-effects model of
   cooperative employment on lagged unemployment,
   with clustered SEs. Add one robustness check.
3. Produce one figure and a LaTeX table.
4. Write report.md explaining what you did and
   the main limitations. Use a single R script.
Ask me before dropping any observation.
```

</div>
<div>

**What to point out while it works**
- It **plans**, then asks for permission to run code
- It hits an error and **fixes it by itself**
- It **asks** before dropping data (because we told it to)
- The final report: is the interpretation right? (**you** decide)

**Plan B**: a recorded screen capture of the same run, in case Wi-Fi fails.

</div>
</div>

<!--
Decide on the day: if time is short after HO2, skip this slide and just show the final report.md.
-->

---

<!-- _class: no-footer divider -->

![bg brightness:0.4](imgs/printing.jpg)

# 4 · Publishing
### What journals require

---

<!-- _class: smallest -->

## What publishers say (consensus, 2023–2026)

<div class="columns">
<div>

**Everywhere** (COPE, ICMJE, all major publishers)
- AI **cannot be an author**: it cannot take responsibility
- **You** are accountable for everything, including errors made by the AI
- **Disclose** substantive use (how depends on the journal)
- **No AI-generated images/figures** in most journals
- **Reviewers and editors must not upload manuscripts** to AI tools

**Differences between publishers**
- *Where* to disclose: dedicated statement (Elsevier), Methods section (Springer Nature), acknowledgements…
- Whether **language editing** must be disclosed (often not)

</div>
<div>

**Check your journal**, e.g.:
- *J. of Co-operative Organization and Management*: Elsevier
- *Annals of Public and Cooperative Economics*: Wiley
- *CIRIEC-España*, *REVESCO*: read their author guidelines (often silent → disclose anyway)

<div class="info box">

Policies change every few months. **Read the current "Guide for authors"** before every submission, not a blog post (and not these slides).

</div>

</div>
</div>

---

<!-- _class: small -->

## A disclosure statement that works

```text
Declaration of generative AI use
During the preparation of this work the authors used Claude (Anthropic,
model <version>, accessed <month year>) to (i) edit the language of the
manuscript and (ii) assist in writing R code for data cleaning and
estimation. All code was reviewed, executed and verified by the authors.
The qualitative coding was performed by the authors; the AI tool was used
only as a second reader on pseudonymised transcripts, via an enterprise
account that does not use data for training. The authors take full
responsibility for the content of the publication.
```

- **What** tool & version · **for what** · **what you verified** · **how data was protected**
- Keep a **log** (prompts, dates, versions): it helps with replication and with reviewers' questions

---

<!-- _class: small -->

## Peer review & "before you hit submit"

<div class="columns">
<div>

**When *you* review**
- The manuscript is **confidential**: don't paste it into ChatGPT
- Polishing **your own** review text is usually fine (check the journal's policy)
- Some publishers offer in-house, approved AI tools: use those

**Never**
- Hide prompts for AI reviewers in your paper
- Use AI to fake data, images or references

</div>
<div>

**Pre-submission checklist**
- ☐ Every reference opened and verified (DOI resolves)
- ☐ Every number traceable to a script output
- ☐ Code runs from scratch (replication package)
- ☐ AI-use statement, following **this journal's** policy
- ☐ No personal data went to a non-approved tool
- ☐ Consent forms / ethics approval cover what you did

</div>
</div>

---

<!-- _class: no-footer divider -->

![bg brightness:0.4](imgs/padlock.jpg)

# 5 · Data protection
### Your interviews are personal data

---

<!-- _class: small -->

## Your interviews are personal data (GDPR)

<div class="columns">
<div>

- **Names, voices, e-mails**: obviously
- **Indirect identifiers**: *"the president of a 12-member housing co-op in Benimaclet"* = one person
- **Special categories** (Art. 9 GDPR): **trade-union membership**, political opinions, health, religion. These come up often in cooperative research!
- **Audio** is harder to anonymise than text

</div>
<div>

Pasting a transcript into a chatbot means:
- Processing by a **third party** → you need a legal basis and a contract (DPA)
- Possibly an **international transfer** (servers outside the EU)
- Possibly **reuse for training** (consumer plans)
- Something your **consent form** probably did **not** mention

</div>
</div>

<div class="error box">

Uploading identifiable interview data to a free chatbot is likely a **GDPR breach** and a breach of your ethics approval, even if "everybody does it".

</div>

---

<!-- _class: smaller -->

## A simple traffic light

| | Data | Where |
|:--:|:--|:--|
| 🟢 | Public data, published papers, your own non-sensitive text, code without data | Any tool |
| 🟡 | **Pseudonymised** transcripts, unpublished manuscripts, grant proposals | **Enterprise/institutional** tools with a DPA, if your DPO agrees |
| 🔴 | Raw audio, identifiable transcripts, special categories, **others'** manuscripts under review, student work with names | **Local** tools only (noScribe, Ollama), or no AI at all |

**From your next study on:**
- Talk to your **Data Protection Officer** and ethics committee **before** collecting data
- Say it in the **consent form**: *"Pseudonymised transcripts may be processed with AI tools under a data processing agreement that excludes use for model training."*
- **Pseudonymise first**, upload later. Keep the key file offline.

---

<!-- _class: small hands-on -->

## ✋ Hands-on 3 · Pseudonymise, then disclose <span class="tag">5 min</span>

<div class="columns">
<div>

**Part A (3 min)**: take the interview excerpt from HO 2B and, **without AI**, mark everything that could identify someone:
- names, places, dates, organisations, roles, unusual events…

Then compare with your neighbour. **Who found more?**

*(Bonus: ask a **local** model or the chatbot to do it on a public text, and see what it misses.)*

</div>
<div>

**Part B (2 min)**: write the **AI-use statement** for the paper you are working on now:
- which tool, for what
- what you verified
- how you protected the data

Would you be comfortable if your **supervisor** or a **referee** read it?

</div>
</div>

<!--
Answer key in handson/interview_README.md. Usual finding: people miss indirect identifiers (job + place + date).
-->

---

<!-- _class: small -->

## And the EU AI Act?

- Since **2 Feb 2025**, organisations that deploy AI (including universities) must ensure **AI literacy** of their staff (Art. 4). Sessions like this one exist partly for that reason.
- **Research exemption**: AI systems developed **only** for scientific research are outside the scope (Art. 2(6)). *Using* ChatGPT in your research does not make it an AI system that you develop.
- What matters most in your daily work is still **GDPR + your contract with the provider + research ethics**.

---

<!-- _class: no-footer divider -->

![bg brightness:0.4](imgs/lecture.jpg)

# 6 · Teaching
### With AI, and for students who use AI

---

<!-- _class: small -->

## Teaching with AI, and teaching students who use AI

<div class="columns">
<div>

**For you (saves hours)**
- Case studies: *"a fictional agricultural co-op facing a merger vote; 2 pages + 5 discussion questions"*
- Exercises **with solutions**, several versions of an exam
- Rubrics and feedback drafts
- Slides (Markdown + Marp), lab notebooks, quizzes
- ⚠️ Check every fact and number; don't upload graded work with names

</div>
<div>

**For your students**
- Assume they use it. Bans can't be enforced, and detectors don't work
- Assessment that resists it: **oral defence**, in-class work, process (drafts, logs), **personal data/fieldwork**
- Or embrace it: *"use AI, attach the conversation, critique its answer"*
- Teach **verification** (HO1 works well in class)
- Make the rules explicit **in the syllabus**

</div>
</div>

---

<!-- _class: small -->

## Five takeaways

1. **Verify everything** that goes out with your name: references, numbers, quotes, code.
2. **Know where your data goes.** Consumer ≠ enterprise ≠ local. Personal data needs a legal basis, a DPA, consent and your DPO's approval.
3. **Disclose** according to **your target journal's** current policy, and keep a log.
4. **Use AI for the craft, keep the judgement**: identification, interpretation and argument are your job.
5. **Start with an agent (Claude Code / Codex) this week**, on a copy of a real project. It is the biggest productivity gain available to you today.

---

<!-- _class: no-footer divider -->

![bg brightness:0.35](imgs/valencia.jpg)

<style scoped>
p, code, strong { color: white !important; }
code { background: rgba(255,255,255,0.15); }
.qr { position: absolute; right: 70px; top: 110px; width: 380px; text-align: center; }
.qr img { width: 320px; border-radius: 8px; }
.qr code { font-size: 15px; }
</style>

# Thank you!
### Questions?

**Oscar José Pellicer Valero** · `Oscar.Pellicer@uv.es`

<div class="qr">

![](imgs/qr_materials.png)

`github.com/OscarPellicer/ai-coop-research-yes2026`

</div>

---

<!-- _class: smallest -->

## References

<div class="reference">

- COPE (2023). *Authorship and AI tools*. COPE position statement.
- Elsevier. *Generative AI policies for journals*. Springer Nature. *Artificial Intelligence (AI)* editorial policy. Wiley. *Using AI tools in your writing*. (Check current versions.)
- Liang, W., Yuksekgonul, M., Mao, Y., Wu, E., & Zou, J. (2023). GPT detectors are biased against non-native English writers. *Patterns*, 4(7).
- Walters, W. H., & Wilder, E. I. (2023). Fabrication and errors in the bibliographic citations generated by ChatGPT. *Scientific Reports*, 13, 14045.
- Regulation (EU) 2016/679 (GDPR), Arts. 4, 9, 28, 44–49. Regulation (EU) 2024/1689 (AI Act), Arts. 2(6), 4.
- Ben-Ner, A. (1988). The life cycle of worker-owned firms in market economies. *J. of Economic Behavior & Organization*, 10(3).
- Pérotin, V. (2006). Entry, exit, and the business cycle: Are cooperatives different? *J. of Comparative Economics*, 34(2).
- noScribe: https://github.com/kaixxx/noScribe · Claude Code: https://claude.com/claude-code · Codex: https://openai.com/codex

</div>

---

<!-- _class: smallest -->

## Image credits

<div class="reference">

Photos from Wikimedia Commons (no changes other than cropping/darkening):
- Title & closing: *Ciudad de las Artes y las Ciencias* by Elemaki, mod. Alvaro qc, CC BY-SA 3.0
- Landscape: *BalticServers data center* by BalticServers.com, CC BY-SA 3.0
- Research: *Graz University-Library reading-room* by Dr. Marcus Gossler, CC BY-SA 3.0
- Qualitative: *Got Audio?* by Alan Levine, CC BY 2.0
- Hands-on 2B: *Palmer elevator 2026-07-03* by Visviva, CC BY-SA 4.0
- Publishing: *The Historic Printing Press in Petah Tikva* by Yarkon River 54, CC0
- Data protection: *Solex 99 30 padlock with keys* by Trougnouf, CC BY 4.0
- Teaching: *Curtis Lecture Halls interior view1 empty class* by Theonlysilentbob, CC BY-SA 3.0

Chart: own elaboration with data from Ministerio de Trabajo y Economía Social (ESI). Agent terminal: illustrative mock-up. Logos belong to their respective institutions.

</div>
