# Hands-on exercises: notes for the facilitator

Material: `interview_excerpt.md`, an excerpt of about 805 words from the oral history interview with Louis Schwing (Premier Cooperative / Fisher Farmers Grain and Coal, Illinois). It was recorded in 2016 by Ben Halpern and is published by Eastern Illinois University under CC BY-NC-ND 3.0.

Licence reminder: attribute the source (the citation is in the header of the excerpt file), use it only for non-commercial purposes and don't distribute modified versions. Pseudonymised versions that participants make on their own laptops during the session are for practice only. Don't collect them or republish them.

---

## Exercise (a): thematic coding with a chatbot (5 min)

**Step 1.** Each participant pastes the excerpt into a chatbot of their choice. Use only the "Excerpt" section, not the header. This step works fine with any of the prompts below. Using different prompts on purpose (A for one row of the room, B for the next) makes the contrast even clearer.

Prompt A (open, no codebook):

```text
You are a qualitative researcher studying cooperatives. Read the interview
excerpt below and perform a thematic analysis. Identify the main themes,
give each a short label and a one-sentence definition, and support each
theme with one short verbatim quote.

[PASTE EXCERPT]
```

Prompt B (a slightly different framing, to show how much the prompt matters):

```text
Code this interview excerpt with a cooperative member/manager. List 5 codes
with a quote for each, then group them into 2-3 higher-level themes.

[PASTE EXCERPT]
```

Prompt C (with a codebook, for the debrief: run it after comparing results):

```text
Code the excerpt below using ONLY the following codebook. For each code,
give the verbatim segment(s) it applies to, or "not present".
Do not create new codes.

GOV   - Democratic governance: role of the board, members' control, decision rights
MEM   - Member/patron relationship: patrons as owners, responding to member needs
FIN   - External finance & dependence: banks, lenders, their influence on decisions
SCALE - Growth, scale and market pressure: volume, competition, efficiency
PROF  - Professionalisation & management: skills, education, hiring, division of labour
TRUST - Trust & social capital: being known locally, reputation, informal networks

[PASTE EXCERPT]
```

**Step 2.** Compare your results with your neighbour's. How many themes did you each get? Do the labels match? Did you get the same quotes? Did either of you get a theme the other didn't?

**Debrief points:** the same text and a similar prompt still give different themes, labels and levels of detail. The model's output can't be reproduced, and the model can sound confident about themes that rest on thin evidence. A codebook (prompt C), a written prompt protocol, recording the model name and version and the date, and a human check of every quote make the process auditable. Ask participants to check that each quote really appears in the text. Models sometimes paraphrase quotes or invent them.

### Reference themes (one plausible reading, not the "right answer")

1. **Board governance and managerial appointment.** The board of directors interviews and hires the general manager. Members govern through the board, and management carries out its decisions ("the board did interview and hire me").
2. **Patrons as owners: management responding to member needs.** The manager's job is "to evaluate what the needs are of the owners of the company, your farmer patrons, they own the company". Investment decisions such as dryers and capacity follow what members report.
3. **External financial dependence vs. member control.** The bank of cooperatives meets the candidate before the board can hire him and gives its "blessing". Lenders who are "backing several millions in loans" have an informal veto over a decision that formally belongs to members. This is a tension between autonomy and dependence (ICA principle 4).
4. **Growth, scale and market pressure.** Many locations, "18-20 million bushels a year", technological change on farms (4 to 16 row combines, semis), and the need to keep members "productive, to stay in business".
5. **Professionalisation and division of labour.** The move from a manager who does everything to specialised roles (operations, merchandising, finance). "As companies get bigger you can't do it all and do it well."
6. **Trust, local reputation and learning (social capital).** Promotion from within, based on being known for 18 years and not on formal credentials ("people knew who you were"). Learning through cooperative networks and conferences (GROWMARK), which is cooperation among cooperatives (ICA principles 5 and 6). Learning by trial and error from the cooperative's own history.

Possible extra codes that a model may also give: humility or self-doubt about qualifications, mentoring by the previous manager, accountability, and pride in long service.

---

## Exercise (b): find and pseudonymise personal data before uploading (5 min)

**Step 1, done offline and before any chatbot.** Participants read the excerpt, including the transcript header, and mark everything that could identify the interviewee or a third party, either directly or when combined with other details. Then they replace each item with a consistent pseudonym or a more general category, for example `[INTERVIEWEE]`, `[COOPERATIVE A]`, `[TOWN, US Midwest]`, `[YEAR]`, `[~20 YEARS]`.

**Step 2, optional, to show the risk.** Paste the *original* excerpt into a chatbot with:

```text
Based only on this text, who is the interviewee, which organisation and
where? What else can you infer about him (age, career, education)?
```

Then paste the pseudonymised version with the same prompt. Even without the name, a web-connected model or a quick Google search can often re-identify the person from indirect details: a cooperative in a small town, a specific year, a career path. This shows the difference between pseudonymisation and anonymisation, and why pseudonymised data is still personal data under GDPR (Recital 26).

A prompt that can help, but only if run on a local or institutionally approved model, never on the raw data in a public chatbot:

```text
List every item in this text that could identify a person directly or
indirectly (names, organisations, places, dates, durations, education,
military service, roles, quantities). Propose a pseudonymisation table.
```

**Debrief points:**
- Pseudonymise before you upload. Pasting the text into a chatbot to ask it to find personal data already counts as disclosing that data.
- Keep the key table (real value and pseudonym) separately and securely. Pseudonymised data is still personal data under the GDPR.
- Indirect identifiers matter as much as names.
- Check your consent form and data management plan for what you may share with third-party processors.
- This transcript is published with consent, so it is ethically safe to use for practice. Your own interviews are not.

### Answer key: personal data and identifiers in the excerpt

**Direct identifiers**

| # | Item | Where | Type |
|---|------|-------|------|
| 1 | "Louis Schwing" | Header and in the LS answer ("they knew Louis Schwing") | Interviewee's full name |
| 2 | "BH" / Ben(jamin) Halpern | Speaker labels and source citation | Interviewer's name (third party, in the citation) |
| 3 | "Jessica Craig" | Header ("Transcribed by") | Third party's name (transcriber) |
| 4 | "LS" | Speaker labels | Initials of the interviewee, which identify him once the name is known |

**Organisations (employer, which allows indirect identification)**

| # | Item | Notes |
|---|------|-------|
| 5 | "Fisher Farms Grain and Coal" / "Fischer Farms" / "Fisher Farmers" / "Fisher Farmer's" / "Fisher's Farmers" | Employer, given five different ways. A good test of whether every variant gets replaced. |
| 6 | "a bank of cooperatives" | The lender, which can be identified from the context (most likely a Farm Credit System bank for cooperatives, such as CoBank). This is my inference, not something the text says. |
| 7 | "Grow Mark" (GROWMARK) | A regional cooperative or federation he belongs to |
| 8 | "United States Air Force" | Military service, which is part of his biography |

**Places**

| # | Item | Notes |
|---|------|-------|
| 9 | "Dewey, IL" | Location of the interview (header). A very small village, which makes the person easy to identify when combined with the other details. |
| (context) | Fisher, IL is implied by the cooperative's name | The organisation's name also gives away a place |

**Dates and durations**

| # | Item | Notes |
|---|------|-------|
| 10 | "4/12/2016" | Date of the interview |
| 11 | "9/1/2016" | Date of transcription |
| 12 | "01:30:22" | Length of the interview (metadata) |
| 13 | "In 1992 you became the general manger" | Year of appointment, which is a key quasi-identifier |
| 14 | "for 18 years" (said several times) | How long he worked as operations manager |
| 15 | "almost 30 years in that capacity" | How long he was in the role |

**Biographical and socio-economic details (quasi-identifiers)**

| # | Item | Notes |
|---|------|-------|
| 16 | "I did not have a college education, I went to high school" | Education level |
| 17 | "was in the United States Air Force" | Military service (see also 8) |
| 18 | Job titles: operations manager, then general manager | Career path |
| 19 | "18-20 million bushels a year", "several locations", "several millions in loans" | Business size, which helps identify the organisation |
| 20 | "the general manager was going to retire" (his predecessor) | A third party identifiable through the employer and the year |

Notes for the debrief: none of this is special-category data under Art. 9 GDPR (health, religion, political opinions, union membership, etc.). In other cooperative interviews, trade union membership or political views come up often, and those raise the bar. Two lessons that participants often miss: the five spellings of the employer's name, and the metadata in the transcript header.
