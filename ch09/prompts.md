# Chapter 9 prompts: Automate Repetitive Work

Copied from the book. Replace every `{PLACEHOLDER}` with your own details before you send a prompt; `{option / option}` means pick one, and `{e.g., ...}` is a hint to replace.

## Task template structure

```text
TASK:    a short, memorable name
WHEN:    what should prompt you (or a schedule) to run it
INPUT:   what changes each time, as {VARIABLES} with defaults
STEPS:   exactly what Claude should do, in order
OUTPUT:  what you should have at the end
CHECK:   how to confirm it worked
```

## Rename files in bulk

```text
Rename every file in {FOLDER} using these rules.

New pattern: {YYYY-MM-DD}_{CATEGORY}_{ORIGINAL NAME}
Category by extension:
- .pdf .docx .xlsx -> DOC
- .jpg .png .webp  -> IMG
- .mp4 .mov        -> VID
- anything else    -> MISC

Examples:
"Annual Report 2026.pdf" -> "2027-03-25_DOC_Annual-Report-2026.pdf"
"Screenshot 2027-03-20.png" -> "2027-03-20_IMG_Screenshot.png"

Conditions:
- Rename in place; do not delete anything
- Replace spaces with hyphens
- If a name already exists, add _01, _02, and so on
- Write renamed_{TODAY}.csv with original_name, new_name, and
  timestamp

Show me a preview of every change and wait for my approval.
```

## Sort and move files by rules

```text
Sort the files in {SOURCE} with these rules, checked in order:
1. Name contains "invoice" -> Finance/Invoices/{YYYY-MM}/
2. Name contains "contract" -> Contracts/Pending/
3. .xlsx or .csv with "report" in the name -> Reports/{YYYY}/
4. Last modified more than six months ago -> Archive/{YYYY}/
5. Anything else -> Unsorted/

Before moving anything:
- Show every file with its destination
- Ask me to confirm
- Write an undo log listing each move, so every change can be
  reversed

Match names case-insensitively.
```

## Process new files regularly

```text
Check Claude-Work/Inbox for files that are not listed in
Logs/watch_log.csv. If there are none, stop and report only
"Inbox empty".

For each new file:
- PDF: summarize the five main points and save the summary as
  {FILENAME}_summary.md next to it
- Spreadsheet: report the number of rows and columns and the
  average of each numeric column
- Image: report the file name and size
- Anything else: report the name and extension

Add one row per file to Logs/watch_log.csv, then send me a
single notification listing what arrived.
```

## Four schedules worth setting up

### Morning briefing, weekdays at 8:00 a.m.

```text
1. Summarize email received since yesterday evening (Gmail)
2. List today's events (Google Calendar)
3. Check for new files in Claude-Work/Inbox
4. Produce the morning briefing from Chapter 7
Result: the briefing waiting in the app, plus a notification
```

### Daily file organizer, every day at 6:00 p.m.

```text
Run the daily file organizer on the Downloads copy.
Only act if there are more than five files; otherwise stop and
report only "Nothing to do".
```

### Weekly report, Fridays at 4:30 p.m.

```text
Run the weekly report compiler for the current week.
Create the report and a Gmail draft, never send it, and notify
me: "Weekly report ready for review."
If anything fails, tell me which step failed and why.
```

### Monthly archive, daily at 9:00 a.m., acting only on the 1st

```text
If today is not the first day of the month, stop.
1. Move files in Claude-Work/Work and Claude-Work/Reports that
   are older than three months to Archive/{YYYY}/{MM}/. Never
   move anything in Logs/, Archive/, Factory/, or Inbox/.
2. Update Archive/archive_index.csv
3. Report how many files moved and how much space they use
Write an undo log; do not delete anything.
```
