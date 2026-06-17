# Exercise 5 — Process-Trends Update Deck

- **App:** PowerPoint (Copilot)
- **Workflow:** Turn the verified PivotTable outputs into a short monthly process-and-coaching trends deck for front-line leaders
- **Material:** your verified pivots and chart from Exercise 3 (`Training-Opportunities.xlsx`)
- **Estimated time:** 14 minutes
- **Difficulty:** Core

---

## Objective

Close the loop: the trends you found in Exercise 3 and the readout you drafted in Exercise 4 become a five-slide deck a team lead can present. Copilot drafts it from the content you provide; you keep every number honest.

## Before you start

- [ ] `Training-Opportunities.xlsx` saved in OneDrive with your PivotTables, chart, and trend summary from Exercise 3.
- [ ] PowerPoint open (web or desktop) with Copilot available.

## What Copilot is doing here

Copilot drafts slides **from content you give it** — reference the workbook with `/` rather than pasting numbers, then verify every figure against the source. It can tighten titles to conclusions and add speaker notes. It does not decide what the trend "means" — you do.

---

## Step 1 — Draft the deck *(reference the file with `/` — don't paste numbers)*
```text
Create a clean, 5-slide monthly process & coaching trends update for front-line leaders using /Training-Opportunities.xlsx. Slide 1: title with the month and "ONB Operations — Process Optimization". Slide 2: overall trend — total opportunities logged and the headline shift vs. last month. Slide 3: the top departments and their leading themes. Slide 4: severity mix and the High-severity callout. Slide 5: this month's coaching focus — two or three actions. One idea per slide. I will verify every figure against the workbook.
```

## Step 2 — Tighten to a leadership standard
```text
Make the wording tighter: one key message per slide, and make every slide title a conclusion rather than a topic (e.g., "Item Processing data-entry errors are the top coaching theme" instead of "Item Processing"). Do not change any numbers.
```

## Step 3 — Add the chart and speaker notes
```text
Add brief speaker notes with the one or two points to say out loud per slide, including the coaching action on the final slide. Leave a placeholder on slide 4 where I'll paste the "Coaching Opportunities by Department and Severity" chart from the workbook.
```

---

## Deliverable

A five-slide process-and-coaching trends deck with conclusion-style titles, speaker notes, and a placeholder for the verified chart.

## Verify before you rely on it

- [ ] Every number on every slide ties to the PivotTables in `Training-Opportunities.xlsx` — check each one.
- [ ] The "headline shift vs. last month" matches the month-over-month pivot, not a guess.
- [ ] Slide titles are conclusions, and no number changed when Copilot reworded them.
- [ ] You pasted the **verified** chart, not a Copilot-generated lookalike.

## Key takeaways

- Build the chart **once** in Excel (Exercise 3), reuse it in the deck — don't let Copilot redraw the data.
- **Conclusion titles** make a readout land in seconds.
- Copilot drafts the deck; **you own every figure that goes in front of leaders.**

---

## The reusable Operations workflow (recap)

1. **Copy first** — Copilot never touches the file of record.
2. **Save in OneDrive** with AutoSave on so version history works.
3. **Shape the data** — one header row, no merged cells/subtotals/blanks; Clean Data button.
4. **One workbook** — source, translation table, and template as tabs (Copilot only sees the open file).
5. **Translate, then flag** — XLOOKUP against the mapping table; unmapped codes say "NOT MAPPED", never a guess.
6. **Validate the intake** — dropdowns stop bad data at the keyboard.
7. **Let the list police itself** — computed follow-up dates + conditional formatting replace the manual filter.
8. **Pivot, then judge** — Copilot builds the trend; you decide the coaching action.
9. **Draft with placeholders** — verify every figure before it leaves the team.
10. **You execute** — Copilot drafts and translates; the upload, the post, and the send are yours.

**Copilot never decides:** which variance is real, which code maps where, what the trend means, what to coach, or what goes in front of leaders. An operations professional does.
