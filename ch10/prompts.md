# Chapter 10 prompts: Build Your Personal Automation System

Copied from the book. Replace every `{PLACEHOLDER}` with your own details before you send a prompt; `{option / option}` means pick one, and `{e.g., ...}` is a hint to replace.

## Invoice processing

```text
Process the invoices in Claude-Work/Invoices/New.

For each file:

STEP 1: Extract
- Invoice number
- Supplier or customer name
- Issue date and due date
- Line items
- Subtotal before tax
- Tax (VAT or sales tax) and its rate
- Total

STEP 2: Record
Add a row to Finance/invoice_master.csv with the columns
invoice_no, supplier, issue_date, due_date, subtotal, tax,
total, status, file_path. Set status to "new".

STEP 3: Check completeness
If any field is unreadable or ambiguous, create
{FILENAME}_NEEDS_REVIEW.txt explaining what must be checked,
and do not guess the value.
Also check that subtotal plus tax equals the total.

STEP 4: File
Fully processed -> Invoices/Processed/{YYYY-MM}/
Needs review    -> Invoices/NeedsReview/

STEP 5: Report
Number of files, how many processed and how many need review,
and the total value processed.
```

## Combining reports from several teams

```text
Combine this week's team reports into one master report.

Sources:
- Sales:      Reports/Sales/weekly_{WEEK}.xlsx
- Marketing:  Reports/Marketing/weekly_{WEEK}.pdf
- Support:    Reports/Support/weekly_{WEEK}.docx
- Operations: Reports/Ops/weekly_{WEEK}.xlsx

Steps:
1. Read each report and extract the main KPIs, highlights, and
   concerns.
2. Check that every team has reported. If one is missing, say
   which and continue with the rest.
3. Create Reports/Master/Master_Weekly_{WEEK}.docx with:
   - A one-page executive summary
   - One KPI table covering every team
   - One section per team
   - Cross-team issues that need coordination
   - All action items in one list
4. Create a Gmail draft to {MANAGERS} saying the report is
   ready, with the three most important points. Do not send it.

Tell me which teams were missing, which concerns need urgent
attention, and when the pipeline has finished.
```

## Lab 10.1, Step 3: run the factory

Uses `Claude-Work/Factory/proposal_template.txt` and `Claude-Work/Factory/clients_data.csv` from this folder.

```text
TASK: Document factory
Template: Claude-Work/Factory/proposal_template.txt
Data: Claude-Work/Factory/clients_data.csv

Skip any row whose CLIENT_COMPANY and SERVICE_NAME are already
in Factory/proposal_index.csv. For each remaining row:
1. Replace every {{VARIABLE}} with the value from that row.
2. Set {{PROPOSAL_NO}} to PROP-{YYYY}-{NNN}, continuing from the
   last number in the index (start at 001), e.g. PROP-2027-001.
3. Set {{DATE}} to today's date.
4. Save the result as
   Factory/Output/Proposal_{PROPOSAL_NO}_{CLIENT_COMPANY}.docx,
   with hyphens in place of spaces in the file name.
5. Add a row to Factory/proposal_index.csv with proposal_no,
   client, company, service, amount, created_date, file_path.

If a field is empty, insert [NOT PROVIDED], flag the row, and
continue.

Show me the first proposal as a preview and wait for my
approval before creating the rest. When finished, list every
output file, the total value of all proposals, and any rows
with missing data.
```

## Design your personal automation system

```text
Help me design a personal automation system.

Role: {JOB TITLE} at {TYPE OF ORGANIZATION}
Working hours: {HOURS}
Main tools: Google Workspace and the Claude desktop app

Tasks I repeat:
1. {TASK}: {HOW OFTEN}
2. {TASK}: {HOW OFTEN}
3. {TASK}: {HOW OFTEN}
(up to 10)

Design a system that:
1. Shows a daily, weekly, and monthly automation schedule
2. Separates tasks to automate fully from tasks to automate in
   part, with my approval
3. Names each task template or skill I need to create
4. Estimates the hours saved per week

Present it as a schedule table, a list of templates to build,
and a simple return-on-investment estimate: hours to build the
system against hours saved per year.
```

## Principle 4: monitor and alert

Add this to every scheduled task.

```text
Notify me immediately if:
- Any step fails
- The task finds far more or far fewer items than usual
- The expected output was not created
- A file or folder the task needs is missing
```

## Principle 5: monthly audit

```text
Analyze this month's automation logs.
{ATTACH THE LOG FILES FROM Claude-Work/Logs}

Check:
1. Which tasks ran most and least often
2. The error rate of each task
3. Runs that took much longer than usual
4. Files that look misfiled
5. Total items processed this month

Summarize as:
- A health score for the system from 1 to 10
- Three things working well
- Three things to improve
- New tasks worth automating, based on patterns in the logs
```

## Worked example: the letters that went to Finance

### The correction task

```text
Use Logs/inbox_log.csv to find every file moved to Finance/
since {START_DATE} whose summary describes an engagement letter
or other contract. List them and wait for my approval. Then
move each one to Legal/, never overwrite, and add a row to the
log for each move with the note "moved by correction".
```

### The revised destination rule (replaces step 3 of the inbox processor)

```text
3. Choose a destination, checking the rules in this order:
   a signed agreement or engagement letter      -> Legal/
   an invoice, with an invoice number and total -> Finance/
   If a file fits more than one rule, move it to NeedsReview/
   and say which rules matched in the run report.
```
