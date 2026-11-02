# Proposal demo: from a Word template to a LaTeX PDF

This folder contains the material for the live demo. An AI agent (Claude Code in VS Code) converts an official Word proposal template to LaTeX, fills in some sections from rough notes, and compiles a PDF.

| file | what it is |
|---|---|
| `template.docx` | Official proposal template (unchanged copy, see below) |
| `idea.md` | Rough notes for a **fictional** project (COOPCYCLE, "Dr. Ana Ferrer"). The researcher and research group are invented. |

## The template

- **What it is:** *Memoria Científico-Técnica, Proyectos Individuales* (scientific and technical report for single-PI projects), English/Spanish bilingual version. It is the main narrative document of a Spanish national research project application.
- **Call:** Agencia Estatal de Investigación (AEI), *Convocatoria 2025, «Proyectos de Generación de Conocimiento» y actuaciones para la formación de personal investigador predoctoral* (PID2025). Application period: 20 Nov to 16 Dec 2025.
- **Source (file):** https://www.aei.gob.es/sites/default/files/convocatory_info/2025-10/MemoriaCT-individual-2025-ingles.docx
- **Call page:** https://www.aei.gob.es/convocatorias/buscador-convocatorias/proyectos-generacion-conocimiento-actuaciones-formacion-0 (tab "Convocatoria")
- **Instructions:** https://www.aei.gob.es/sites/default/files/convocatory_info/assistants/2025-11/Instrucciones-MemoriaCT-individual-2025-v2.pdf
- **Version:** file dated 20 Oct 2025, downloaded 30 Oct 2026. SHA-256: `b31efc43ff23ee09163cb6bd239c60538706a340f9014ed51d3941172f0f25ac`. It is a plain `.docx` with no macros.

### Rules from the template and instructions

- Maximum **20 pages** for the whole document.
- Recommended format: Times New Roman, Calibri or Arial, at least 11 pt; side margins 2.5 cm; top and bottom margins 1.5 cm; at least single line spacing.
- English is compulsory if the requested direct costs are 100,000 EUR or more. Otherwise English is recommended but optional.
- The document is submitted as a PDF (max 4 MB).

### Sections

1. Proposal data: PI 1, PI 2, title and acronym (Spanish and English)
2. Justification and novelty of the proposal
   - 2.1 Adequacy to the selected modality
   - 2.2 Justification and expected contribution to knowledge; starting hypothesis
   - 2.3 (oriented research only) Contribution to the selected thematic priority
3. Objectives, methodology and work plan
   - 3.1 General and specific objectives
   - 3.2 Methodology
   - 3.3 Work plan and schedule
   - 3.4 Critical points and contingency plan
   - 3.5 Previous results of the team
   - 3.6 Human, material and equipment resources available
4. Expected impact of the results
   - 4.1 Impact on scientific-technical knowledge
   - 4.2 Social and economic impact
   - 4.3 Scientific communication and internationalisation (including open access publications)
   - 4.4 Dissemination to relevant groups and society
   - 4.5 (if applicable) Transfer and valorisation
   - 4.6 (if applicable) Data management plan summary
   - 4.7 (if applicable) Gender inclusion in the content
5. Justification of the requested budget
6. Training capacity
   - 6.1 Training programme
   - 6.2 Theses in the team (last 10 years)
   - 6.3 Careers of past PhD graduates
7. Specific conditions for the execution of certain projects

Only the whole document has a page limit (20 pages); there are no limits per section. In the online application form (not in this document), the impact summary is limited to 3,500 characters.

### Reuse terms

The AEI legal notice (https://www.aei.gob.es/aviso-legal) forbids total or partial reproduction of the portal's content "sin citar su origen o solicitar autorización". Reproduction is therefore allowed **if the source is cited**, which this README does. Spanish public-sector information is also reusable under Ley 37/2007 and RD 1495/2011, on condition that you cite the source, do not distort the meaning, and give the update date. The template is redistributed here unchanged, for teaching.

**Caveat:** the page header contains the Ministry and AEI logos. The legal notice says logos and trademarks belong to the AEI and are protected. Showing them in an unchanged copy of the official form is fine. In LaTeX versions shown in the demo or shared afterwards, **drop the logos** or replace them with a plain text header, so that the fictional proposal cannot be mistaken for a real AEI application.

## Why not the MSCA Postdoctoral Fellowships template?

It was the first choice, but the official Part B Word template (HORIZON-MSCA-2026-PF-01, v5.0) can only be downloaded from inside the Funding & Tenders submission system, which requires an EU Login. The public topic page only gives the full application form as a PDF: https://ec.europa.eu/info/funding-tenders/opportunities/docs/2021-2027/horizon/temp-form/af/af_he-msca-pf_en.pdf. EC documents are reusable under Commission Decision 2011/833/EU, so the PDF could be redistributed with attribution. The `.docx` copies hosted by universities, such as the University of Zurich, include each university's own guidance and personal metadata, so they are not clean official copies.

## Demo prompt

> Convert `proposal/template.docx` to a LaTeX document that keeps its layout (A4, margins, fonts, the numbered bilingual section structure, and the footer with page X of Y; leave out the logos). Then fill in section 1 (Proposal data), 2.2 (Justification and hypothesis) and 3.1 (Objectives) from `proposal/idea.md`. Write proper academic prose in English, do not invent references or results, and leave all other sections with their original guidance text as placeholders. Compile it to PDF with latexmk and show me the result.

Follow-up prompts if there is time:

- "Now add 3.3 Work plan with a Gantt chart (TikZ or pgfgantt) from the timeline in idea.md."
- "Check the PDF against the template's rules (20 pages max, 11 pt, margins) and list any violations."
