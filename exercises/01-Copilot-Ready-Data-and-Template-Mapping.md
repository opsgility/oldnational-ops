# Exercise 1 — Copilot-Ready Data & Template Mapping

- **App:** Excel for the web
- **Featured skill:** **Formulas & Functions** (XLOOKUP, IFERROR, text/number cleanup)
- **Workflow:** Clean a messy third-party export, then translate its coded values into your upload template using a translation table
- **Workbooks:** **Process-Intake-Raw.xlsx** (cleanup), then **Template-Builder.xlsx** (tabs: `Source`, `Mapping`, `Template`, `Validation-Lists`)
- **Estimated time:** 22 minutes
- **Difficulty:** Foundational — do this first

---

## Objective

Learn the #1 success factor for Copilot in Excel — data shape — then use Copilot and a **translation table** to convert a third-party file's codes into the standard values your upload template needs. This is the real Operations workflow behind feeding a Docusign upload or a list: many incoming formats, one template, and a mapping in between.

## Before you start

- [ ] Both workbooks open in **Excel for the web**, AutoSave on, **working on a copy**.
- [ ] Open `Process-Intake-Raw.xlsx` — notice the merged title, the stacked two-row header, the per-department subtotal rows mixed into the data, the blank rows, the request numbers that lost their leading zeros, and the trailing spaces in customer names.

## What Copilot is doing here

Copilot reads **table-shaped** data: one header row, unique headers, no merged cells, no subtotal rows, no blank rows/columns. Most "Copilot doesn't work" complaints are data-shape problems. Then, because Copilot only sees the **open workbook**, the translation works by referencing tabs that live in one file — the `Source`, the `Mapping` table, and the `Template` are all in `Template-Builder.xlsx`.

---

## Part A — Make the raw export Copilot-ready (`Process-Intake-Raw.xlsx`)

### Step 1 — Diagnose (Chat only)
Switch the Copilot pane to **Chat only** and run:
```text
Look at the data on this sheet and tell me what would prevent Copilot from analyzing it reliably. Check for merged title cells, multiple header rows, per-department subtotal rows mixed into the data, blank rows, request numbers stored as numbers that have lost leading zeros, and trailing spaces in text. List each issue and where it is.
```
Read the list — that is your cleanup plan.

### Step 2 — Restructure to a clean table (**Allow editing**)
```text
Restructure this data into a proper Excel table on a new sheet called CleanIntake: a single header row with the columns Req Number, Customer Full Name, Dept Code, Request Type, Date Received, Amount, Status Code, Assigned To. Remove the merged title, the stacked header, every per-department subtotal row, the grand total row, and all blank rows. Keep the original sheet unchanged.
```

### Step 3 — Fix the request numbers and spacing
```text
In the CleanIntake table, format Req Number as text with leading zeros preserved (10 digits), and trim leading and trailing spaces from Customer Full Name. Tell me how many cells you changed in each column.
```

> Also run **Data tab → Clean Data** for spacing, capitalization, and number-vs-text inconsistencies — it shows each suggestion for you to Apply or Ignore.

---

## Part B — Translate codes into the template (`Template-Builder.xlsx`)

The `Source` tab holds clean third-party data with **coded** values. The `Mapping` tab is your **translation table** (DeptCode → Department, ReqTypeCode → Document Type, StatCode → Status). The `Template` tab is the empty upload layout.

### Step 4 — Translate with XLOOKUP (**Allow editing**)
```text
On the Source sheet, add three columns using XLOOKUP against the Mapping sheet: "Department" (look up DeptCode in the DeptCode/Department block), "Document Type" (look up ReqTypeCode in the ReqTypeCode/Document Type block), and "Status" (look up StatCode in the StatCode/Status block). Where a code has no match, return "NOT MAPPED" instead of an error. Explain the XLOOKUP you used.
```

### Step 5 — Flag the exceptions
```text
Tell me every row where Department, Document Type, or Status came back "NOT MAPPED": give me the row number, the original code, and which field it's in. Then highlight those cells in light red so I can chase the vendor for the correct values.
```
*(You should find the unknown request-type code `XQZ` and the dept code `TR`, which isn't an Operations department.)*

### Step 6 — Build the upload template
```text
Fill the Template sheet from the Source sheet: Document ID = Req Number, Signer Name = Customer Full Name, Department, Document Type, Effective Date = Date Received, Amount (USD) = Amt, Status. Only include rows where nothing is "NOT MAPPED". Tell me how many rows you wrote and how many you held back.
```

---

## Deliverable

A clean `CleanIntake` table, a `Source` tab translated via the mapping table with exceptions flagged, and a populated `Template` upload layout containing only fully-mapped rows.

## Verify before you rely on it

- [ ] Request numbers kept their leading zeros (they begin with `00`).
- [ ] Every value in the Template's Department, Document Type, and Status columns is a real standard value — none say "NOT MAPPED".
- [ ] The held-back rows are exactly the ones with `XQZ` / `TR` — spot-check them against the Mapping tab.
- [ ] Row count: rows written + rows held back = rows on the Source tab (nothing dropped or duplicated).

## Key takeaways

- **Data shape is the #1 success factor** — fix merged cells, subtotals, and blanks before judging Copilot's answer.
- A **translation table + XLOOKUP** is the backbone of "convert their format into ours" — and wrapping it so unmapped codes say "NOT MAPPED" beats silently guessing.
- Copilot only sees the **open workbook** — the translation works because Source, Mapping, and Template are tabs in one file.
- **Copilot fills the template; you upload it.** Verify the unmapped list before anything goes to Docusign or a list.

---

*Next: Exercise 2 — Process & 90-Day Follow-Up Tracker.*
