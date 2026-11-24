# Chapter 8: Put Claude to Work in Google Workspace

| File | Used in | What to do with it |
|---|---|---|
| `project_tracker.csv` | Walkthrough "analyze a project tracker"; Lab 8.1 (if you have no sheet of your own) | Paste into Claude, or import into a Google Sheet |
| `prompts.md` | The walkthrough; the report pipeline; Lab 8.1, Step 2 | Copy each prompt into Claude |

The book prints the tracker with each row wrapped over two lines; in this file each project is one line, as the book says the real file should be.

To put the tracker in Google Sheets: create a blank spreadsheet, then choose **File** > **Import** > **Upload**, select `project_tracker.csv`, and pick **Replace current sheet**. Give the sheet a name you will use in the pipeline prompt.

Check: the Website Redesign should come out Red or Amber (due in six days at 65% complete, with "today" set to March 25, 2027), and the Data Migration as at risk (15% complete with a month left).
