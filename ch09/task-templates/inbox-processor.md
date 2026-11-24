TASK: Inbox processor
Run date: today. Inbox: Claude-Work/Inbox

For each file in the inbox:
1. Identify the type: PDF, spreadsheet, document, image, other.
2. Extract: title or main subject; date in the document; sender
   or source; three-sentence summary; action items; deadline.
   Write "none" for anything not present.
3. Choose a destination:
   name or content mentions an invoice -> Finance/
   mentions a contract                  -> Legal/
   mentions a report                    -> Reports/
   other spreadsheets                   -> Data/
   anything else                        -> General/
4. Save Summaries/{FILENAME}_summary.md with: type, processed
   date, category, destination, summary, action items, deadline.
5. Move the file. If a file with that name exists at the
   destination, add _01, _02, and so on; never overwrite.
6. Add a row to Logs/inbox_log.csv: date, filename, type,
   category, destination, summary_path, has_action_items.

Finish with a report: files processed, files with action items,
and the nearest deadline.
If a file cannot be read, leave it in the inbox and tell me why.
