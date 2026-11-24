# Chapter 9: Automate Repetitive Work

| File | Used in | What to do with it |
|---|---|---|
| `task-templates/daily-file-organizer.md` | Template 1 | Save in an "Automation" Project, or as a skill |
| `task-templates/new-document-processor.md` | Template 2 | As above |
| `task-templates/weekly-report-compiler.md` | Template 3 | Run inside your Reports Project |
| `task-templates/inbox-processor.md` | Lab 9.1, Step 2 | Save as a skill or in your Automation Project, named "Inbox processor" |
| `prompts.md` | File management prompts; the four schedules | Copy each prompt into Claude, or into a scheduled task |

## Folders for Lab 9.1

This repository does not include the lab folders, because any file left in them, even a placeholder, would be picked up by the inbox processor. Create them yourself inside your working folder (for example `Documents/Claude-Work`):

```text
Claude-Work/
|-- Inbox/       put the test files here
|-- Summaries/
`-- Logs/
```

Claude creates the destination folders (Finance, Legal, Reports, Data, General) the first time it needs them, and asks for your approval first.

## Test files

The lab uses your own test files: a PDF (a report or an invoice), a spreadsheet, and a Word document, plus, for Step 5, a password-protected PDF and a file whose name already exists at its destination. Use copies of non-confidential files, never originals. For the spreadsheet you can use any CSV from `../ch06/`.

Test any automation that moves, renames, or deletes files on a copy first, and run it by hand at least three times before you schedule it.
