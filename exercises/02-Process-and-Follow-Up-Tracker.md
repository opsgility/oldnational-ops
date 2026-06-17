# Exercise 2 — Process & 90-Day Follow-Up Tracker

- **App:** Excel for the web
- **Featured skills:** **Data Validation** (dropdowns, consistent intake) and **Conditional Formatting** (overdue / due-soon flags) + date functions
- **Workflow:** Turn a project/process log into a self-policing tracker that surfaces 90-day follow-ups automatically instead of by manual filtering
- **Workbook:** **Process-Tracker.xlsx** (tabs: `Tracker`, `Lists`, `Legacy`)
- **Estimated time:** 24 minutes
- **Difficulty:** Core

---

## Objective

Replace the manual "filter the list every quarter to find what's due" habit with a tracker that **computes** the follow-up date, **flags** what's overdue or coming due, and **prevents** inconsistent entries at the point of typing. This is the follow-up workflow your team already runs — just made automatic.

## Before you start

- [ ] `Process-Tracker.xlsx` open in **Excel for the web**, AutoSave on, **working on a copy**.
- [ ] Look at the `Tracker` tab: each item has a **Date Logged**, and your rule is **follow up 90 days later**. Some items were logged well over 90 days ago.
- [ ] The `Lists` tab holds the allowed values for Department, Priority, Status, and Follow-Up Needed.

## What Copilot is doing here

Copilot can write the **date math** (Date Logged + 90), build **Data Validation** dropdowns from a list, and apply **Conditional Formatting** rules from a plain-English description ("highlight overdue items red"). It applies these directly to the open workbook — so work on a copy.

---

## Part A — Compute the follow-up date (**Allow editing**)

### Step 1 — Fill in the follow-up dates
```text
On the Tracker sheet, where Follow-Up Needed is "Yes" and Follow-Up Date is blank, set Follow-Up Date = Date Logged + 90 days. Leave it blank where Follow-Up Needed is "No". Tell me how many you filled in.
```

### Step 2 — Add a status flag column
```text
Add a column called "Follow-Up Flag". For rows where Follow-Up Needed is "Yes" and Status is not "Closed": "OVERDUE" if the Follow-Up Date is before today, "DUE SOON" if it is within the next 14 days, otherwise "On Track". Blank for everything else. Use TODAY() so it stays current.
```

---

## Part B — Conditional Formatting (the visual flags)

### Step 3 — Highlight by flag
```text
On the Tracker sheet, apply conditional formatting: fill the row light red where Follow-Up Flag is "OVERDUE", light amber where it is "DUE SOON", and light green where it is "On Track". Apply it across the used columns so the whole row is shaded.
```

### Step 4 — Isolate what needs action
```text
Filter the Tracker to show only OVERDUE and DUE SOON items, sorted by Follow-Up Date oldest first. Then tell me how many of each there are, broken down by Department and Owner.
```

---

## Part C — Data Validation (stop bad data at the source)

### Step 5 — Add dropdowns from the Lists tab
```text
Add Data Validation dropdowns on the Tracker sheet: Department from the Department list on the Lists sheet, Priority from the Priority list, Status from the Status list, and Follow-Up Needed from its Yes/No list. Make them reject entries that aren't in the list, and apply to the whole column so new rows are covered.
```

### Step 6 — Catch existing inconsistencies
```text
Before I trust the dropdowns, check the existing Department, Priority, and Status values against the allowed lists and tell me any cell whose value isn't an exact match — wrong spelling, casing, or extra spaces — with its cell address.
```

---

## Part D — Formula literacy (the `Legacy` tab)

### Step 7 — Explain the inherited formula (Chat only)
```text
Explain what the formula in cell C4 of the Legacy sheet does, step by step, in plain language for someone reviewing this tracker. Note anything fragile, such as the hard-coded 90 and 75 day thresholds and how it behaves on a "Closed" or "Resolved" item.
```

---

## Deliverable

A `Tracker` with computed follow-up dates, a live `Follow-Up Flag`, row-level conditional formatting, list-enforced dropdowns on the key fields, and a plain-language explanation of the legacy flag formula.

## Verify before you rely on it

- [ ] Pick two items by hand: Date Logged + 90 matches the Follow-Up Date Copilot wrote.
- [ ] An item logged over 90 days ago and not Closed shows **OVERDUE**; a recent one shows **On Track**.
- [ ] Typing a junk value (e.g., "Widgets") into the Department column is **rejected** by validation.
- [ ] The flag uses `TODAY()` (re-open tomorrow — a borderline DUE SOON item should be able to roll to OVERDUE).

## Key takeaways

- **Data Validation** turns a free-text log into a clean dataset — and clean data is what makes PivotTables (Exercise 3) trustworthy.
- **Conditional Formatting** replaces the manual quarterly filter: the list tells *you* what's due, every time you open it.
- Date math with `TODAY()` is **live** — the tracker re-evaluates itself; you don't re-run anything.
- Always have Copilot **explain inherited formulas** before you rely on or change them.

---

*Next: Exercise 3 — Training-Opportunity Trends.*
