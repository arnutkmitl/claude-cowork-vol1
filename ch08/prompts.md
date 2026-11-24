# Chapter 8 prompts: Put Claude to Work in Google Workspace

Copied from the book. Replace every `{PLACEHOLDER}` with your own details before you send a prompt; `{option / option}` means pick one, and `{e.g., ...}` is a hint to replace.

## Walkthrough: analyze a project tracker

The data is `project_tracker.csv`.

### Portfolio view

```text
Analyze this project portfolio. Today is March 25, 2027.
{PASTE THE DATA}

1. Which project is most worrying, and why?
2. What is the overall budget utilization across all projects?
3. Which team is most overloaded?
4. Which projects are due in March?
5. Which projects are at risk of missing their due date?

Give each project a status: Green (on track), Amber (at risk),
or Red (critical). Red means delayed, or more than 90% of budget
spent with significant work left.
```

### Status report

```text
Based on this analysis, write a one-page project status report
for the CEO:
## Project portfolio status, March 2027
### Executive summary (three sentences)
### Projects that need attention (Amber and Red only, each with
a response plan)
### Financial overview (table: project, budget, spent, % spent,
status)
### Deadlines in the next 30 days
### Three recommendations
Formal tone.
```

### Action items for each team

```text
From this status, create next week's action items for each
team. For each team, a table with: task, project, priority
(Critical, Important, Normal), and deadline. Sort by priority.
```

## Build a report pipeline: Sheets to document to email

```text
Run the monthly report pipeline.

Step 1: Get the data
Open the spreadsheet {NAME OR URL} in my Drive and read the
sheet "{SHEET NAME}", from row 2 to the last row with data.

Step 2: Analyze
- Five key KPIs: {COLUMNS}
- Compare with last month: {SHEET OR COLUMN}
- Three highlights and two areas to improve

Step 3: Write the report
Use the monthly executive summary structure saved in this
Project. Create it as a Google Doc named "{REPORT NAME},
{MONTH YEAR}" in {DRIVE FOLDER}, or save it as a .docx in the
working folder.

Step 4: Draft the email
Create a Gmail draft to {RECIPIENTS}.
Subject: "Monthly report: {MONTH YEAR}"
Body: a one-sentence summary, the five most important points,
and a link to the report.

Report back after each step. Do not send the email.
```

## Lab 8.1, Step 2: the pipeline prompt

```text
Report pipeline: {REPORT NAME}

STEP 1: DATA
Spreadsheet: {NAME OR URL}, sheet "{NAME}", all rows with data.
Report date: {DATE, or today}

STEP 2: ANALYSIS
- Main KPIs: {FIVE KPIS}
- Compare with: {target / last month / last year}
- Three highlights and two areas to improve
- Risks for next month

STEP 3: REPORT
Create "{NAME PATTERN}, {MONTH YEAR}" in {FOLDER}.
Structure: {YOUR REPORT STRUCTURE}

STEP 4: EMAIL DRAFT
To: {RECIPIENTS}
Subject: {PATTERN}
Body: a one-sentence summary, the five most important points,
a link to the report, and a closing.

OUTPUT
Report after each step. Do not send anything.
```
