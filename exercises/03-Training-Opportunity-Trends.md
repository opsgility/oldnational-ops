# Exercise 3 — Training-Opportunity Trends

- **App:** Excel for the web
- **Featured skill:** **PivotTables** (and PivotCharts) for trend analysis
- **Workflow:** Turn a department's coaching/training-opportunity log into the two or three trends each team lead should act on
- **Workbook:** **Training-Opportunities.xlsx** (tab: `Log`)
- **Estimated time:** 20 minutes
- **Difficulty:** Core

---

## Objective

Your team logs the coaching and training opportunities it finds — by department, theme, severity, and source — so trends can be communicated to the front line. This exercise turns that log into **PivotTables and a chart** that answer "what should we coach on this month?" instead of leaving the log as a pile of rows.

## Before you start

- [ ] `Training-Opportunities.xlsx` open in **Excel for the web**, AutoSave on, **working on a copy**.
- [ ] Look at the `Log` tab: each row is one logged opportunity with Date, Department, Team/Unit, Employee Role, Opportunity Theme, Severity, Source, and Coached (Yes/No).

## What Copilot is doing here

Copilot can **build a PivotTable from a natural-language question** ("count by department and theme"), add a **PivotChart**, and then **read the pivot back to you in words**. PivotTables need clean, table-shaped data — which is exactly what Data Validation (Exercise 2) gives you.

---

## Part A — The core trend pivots (**Allow editing**)

### Step 1 — Volume by department and theme
```text
Create a PivotTable on a new sheet showing the count of logged opportunities by Department (rows) and Opportunity Theme (columns), with a grand total. Then tell me the top three department-and-theme combinations by count.
```

### Step 2 — Severity mix
```text
Add a PivotTable showing count of opportunities by Department (rows) and Severity (columns: Low, Medium, High). Tell me which departments have the most High-severity items.
```

### Step 3 — Trend over time
```text
Create a PivotTable of count by Month (from the Date column) and Department, then a PivotTable of count by Month and Opportunity Theme. Tell me which themes are rising month over month and which are falling.
```

---

## Part B — Coaching coverage and a chart

### Step 4 — What hasn't been coached yet
```text
Using the Coached column, show count of opportunities by Department split by Coached (Yes/No), and the percentage still uncoached per department. List the departments with the most uncoached items.
```

### Step 5 — Build the trend chart
```text
Create a clustered column PivotChart of opportunity count by Department, broken out by Severity. Title it "Coaching Opportunities by Department and Severity". Keep it clean enough to drop into a readout.
```

---

## Part C — Turn the pivots into words

### Step 6 — Draft the trend summary (Chat only)
```text
Based on the PivotTables on this workbook, write a short trend summary for the monthly coaching readout: one line on the overall trend, then for the three departments with the most activity, the top theme, the severity mix, and one suggested coaching focus. Keep it to something a team lead reads in two minutes. I will verify the counts against the log.
```

---

## Deliverable

A set of PivotTables (department × theme, department × severity, month-over-month trend, coaching coverage), a clustered-column PivotChart, and a short written trend summary ready for the readout deck (Exercise 5).

## Verify before you rely on it

- [ ] The grand total of the department × theme pivot equals the number of data rows in the `Log` (78).
- [ ] Spot-check one cell: filter the `Log` to that department + theme and confirm the count matches the pivot.
- [ ] The "rising / falling" claims in the summary actually match the month-over-month pivot — don't take the prose on faith.
- [ ] Uncoached percentages add up sensibly (Yes% + No% = 100% per department).

## Key takeaways

- A **PivotTable** answers "where should we focus?" in seconds — but only if the underlying log is clean (that's why Exercise 2 came first).
- Ask Copilot to **read the pivot back in words**, then **verify the numbers** before they become a coaching message.
- **PivotCharts** are the bridge from analysis to the readout deck — build the chart once, reuse it in PowerPoint.

---

*Next: Exercise 4 — Inbox Summary to Coaching Readout & Draft.*
