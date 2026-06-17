# Practice Inbox Pack — Operations Cohort

Four synthetic email threads for the Copilot for Operations session. Email each one to **yourself** before the session (see the [Pre-Work](../prework/00-PreWork-Setup-and-Upload.md)). Use the **subject line exactly as written** — you'll reference these names with `/` inside Copilot. Send the first message, then **Reply** to yourself with each following message so the thread builds up.

All names, numbers, departments, vendors, and customers below are **fictional**. Do not add real ONB content, customer names, account numbers, or balances.

---

## Thread 1 — Subject: `Monthly Coaching Trends — Operations Readout` (3 messages)

**Message 1 — from "Renee Castillo (BPM / Process Optimization Lead)"**
```
Team,

Pulling together the monthly coaching readout for the front-line leaders. From the training-
opportunity log this period:

- Item Processing is still showing a cluster of data-entry errors on the returns queue —
  it's the single most logged theme this month.
- Wire Services has a run of "procedure not followed" items, mostly on the callback step.
- Documentation accuracy is creeping up across two or three departments.
- Severity is mostly Low/Medium, but a few High items in Wire Services need a callout.

I want the trends summarized so each department lead gets the two or three things to coach
on this month — not a data dump. Can someone pull the pivot and draft the readout?
— Renee
```

**Message 2 — Reply, from "Marcus Bell (Process Analyst)"**
```
Renee,

On it. I'll pivot the log by Department and Theme, then by Severity, so we can see where to
focus. First read: Item Processing data-entry errors are concentrated in the Returns unit,
and the Wire callback items are all the same root cause — the new procedure step isn't in
the job aid yet.

I'll draft a short readout per department with the top themes and a suggested coaching focus.
— Marcus
```

**Message 3 — Reply, from "Renee Castillo (BPM / Process Optimization Lead)"**
```
Perfect. For the readout I want: one line on the overall trend, then per department the top
two themes, the severity mix, and a single coaching action. Keep it to something a team lead
can read in two minutes. I'll verify the counts against the log before it goes out.
— Renee
```

---

## Thread 2 — Subject: `Vendor File Mapping — Servicing Export to Template` (3 messages)

**Message 1 — from "Priya Raman (Vendor / Intake Coordinator)"**
```
Hi all,

The Q2 servicing export from the third-party portal is in. Same problem as last quarter — the
vendor's codes don't match our template, so before it can go into the upload template it has
to be translated: their DeptCode/ReqTypeCode/StatCode into our standard Department, Document
Type, and Status values.

Two things I'm seeing this time:
- A couple of request-type codes I don't recognize (one looks like "XQZ").
- One row has a dept code "TR" that isn't one of our operations departments.

Can ops run it through the translation table and flag anything that doesn't map, before we
build the upload file?
— Priya
```

**Message 2 — Reply, from "Marcus Bell (Process Analyst)"**
```
Priya,

Yes — I'll map it against the translation table (DeptCode -> Department, ReqTypeCode ->
Document Type, StatCode -> Status) and add a column that flags any code with no match instead
of guessing. The "XQZ" and "TR" rows will come back as NOT MAPPED so we can chase them down
rather than push a bad value into the template.

Once it's clean I'll fill the upload template. Nothing gets uploaded until you've eyeballed
the unmapped list.
— Marcus
```

**Message 3 — Reply, from "Priya Raman (Vendor / Intake Coordinator)"**
```
Great. For the unmapped codes, give me a short list: the row, the original code, and which
field it's in, so I can get the vendor to confirm the correct values. I'll verify the mapped
template against the source before anyone uploads it.
— Priya
```

---

## Thread 3 — Subject: `90-Day Follow-Up Items — Q2 Review` (2 messages)

**Message 1 — from "Alan Whitfield (Operations Manager)"**
```
Ops team,

Time for the quarterly sweep of the follow-up tracker. We log items with a 90-day follow-up
date, and the team has been finding them by manually filtering the list — I'd like a cleaner
view this quarter.

Please pull together: everything where the follow-up date has already passed and the item
isn't Closed, plus anything coming due in the next two weeks so nothing slips. Group it by
department and owner so I can route it.
— Alan
```

**Message 2 — Reply, from "Dana Okafor (Team Lead)"**
```
Alan,

Will do. I'll compute the follow-up date as date-logged plus 90 days, flag the overdue ones
and the due-soon ones, and highlight them so they're obvious instead of relying on a manual
filter. I'll send the overdue list grouped by owner with item IDs.

I'll verify each date before it goes out — a couple of items were re-logged so the dates
moved.
— Dana
```

---

## Thread 4 — Subject: `Process Exception — Wire Services Callback Gap` (3 messages)

**Message 1 — from "Dana Okafor (Team Lead)"**
```
Hi Renee,

Flagging a process gap before it becomes an audit finding. On outbound wires above the
callback threshold, the new second-callback step is being done but not consistently
documented in the system — so from the record it looks like the control was skipped even when
it wasn't.

It's showing up repeatedly in the training-opportunity log under "procedure not followed,"
but the real issue is the job aid and the system field, not the people.
— Dana
```

**Message 2 — Reply, from "Renee Castillo (BPM / Process Optimization Lead)"**
```
Dana,

Agreed — this is a process/documentation fix, not a coaching-the-individual fix. Let's: (1)
add the callback-documentation step to the job aid, (2) make the system field required, and
(3) re-baseline the log so we can show the trend coming down next month.

Can you write this up as a short process-improvement note I can take to the Change Initiatives
intake? Keep it factual — what's happening, the impact, the proposed fix.
— Renee
```

**Message 3 — Reply, from "Dana Okafor (Team Lead)"**
```
Got it — job aid update, required field, re-baseline. I'll draft the improvement note and
route it to you before it goes to Change Initiatives. I'll keep the numbers as placeholders
until I've tied them to the log.
— Dana
```

---

*All content is synthetic and for training only. Keep it inside ONB's Microsoft 365 tenant.*
