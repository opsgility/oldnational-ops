# Copilot for Operations — ONB Hands-On Exercises

Hands-on materials for the *Microsoft 365 Copilot for Operations* session (Old National Bank). The session is anchored in **Excel** — built around the four features the cohort uses most: **Formulas & Functions, PivotTables, Data Validation, and Conditional Formatting** — with **Outlook** for summarizing and drafting, and a single **PowerPoint** exercise to turn the numbers into a process-trends update.

It is designed for ONB Operations, with the **Process Optimization / Business Process Management (BPM)** team as the lead audience, and content drawn from real Operations workflows: translating a third-party file into an upload template, logging projects and process items, tracking 90-day follow-ups, and turning coaching trends into a readout.

## Start here
- [Pre-Work — Set up and upload your practice materials](prework/00-PreWork-Setup-and-Upload.md) — **complete before the session.**

## Exercises
1. [Copilot-Ready Data & Template Mapping](exercises/01-Copilot-Ready-Data-and-Template-Mapping.md) — *Excel · Formulas & Functions*
2. [Process & 90-Day Follow-Up Tracker](exercises/02-Process-and-Follow-Up-Tracker.md) — *Excel · Data Validation + Conditional Formatting*
3. [Training-Opportunity Trends](exercises/03-Training-Opportunity-Trends.md) — *Excel · PivotTables*
4. [Inbox Summary to Coaching Readout & Draft](exercises/04-Inbox-Summary-and-Draft.md) — *Outlook*
5. [Process-Trends Update Deck](exercises/05-Process-Trends-Update-Deck.md) — *PowerPoint*

## Sample materials (`assets/`)
- `Process-Intake-Raw.xlsx` — a deliberately messy third-party servicing export (merged title, stacked header, per-department subtotal rows, blank rows, request numbers that lost their leading zeros, trailing spaces) for the data-prep lesson
- `Template-Builder.xlsx` — a `Source` tab of coded vendor data, a `Mapping` (translation table) tab, an empty `Template` upload layout, and a `Validation-Lists` tab — for the translate-and-build-the-template workflow
- `Process-Tracker.xlsx` — a project/process log with date-logged, a 90-day follow-up workflow, `Lists` for dropdowns, and a `Legacy` formula tab to explain
- `Training-Opportunities.xlsx` — a 78-row coaching/training-opportunity log across departments, themes, and months for PivotTable trend analysis
- `Practice-Inbox-Pack.md` — four synthetic Operations email threads you email to yourself in pre-work

## How to use
Each exercise is self-contained: objective, prerequisites, step-by-step prompts, a deliverable, and a verification checklist. All prompts are copy-paste ready. Work in **Excel for the web** and **Outlook on the web** with the sample materials saved in **OneDrive**.

## Ground rules
Copilot accelerates the mechanics; the operations professional decides. **There is no Track Changes in Excel — work on a copy** and rely on OneDrive version history. Copilot only sees the **open workbook** (put the source, the translation table, and the template as tabs in one file) and the **mail you can open**. **Nothing uploads, posts, or sends until a person clicks the button** — Copilot drafts and translates; you verify the mapping and execute the upload to Docusign or a list yourself. Verify every translated value, follow-up date, count, and flagged exception before it goes into a template, a tracker, a readout, or an email. Use only synthetic sample data inside ONB's Microsoft 365 tenant — never live customer, account, or vendor information.

> **A note on storage:** these exercises assume your files live in **OneDrive** (Copilot in Excel requires a cloud-saved file with AutoSave on). They do **not** assume SharePoint access. If your team's lists or templates live elsewhere, the template you build here is still the clean, validated source — uploading it to its destination remains a manual, human step.
