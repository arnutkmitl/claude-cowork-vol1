TASK: New document processor
WHEN: a document lands in Claude-Work/Inbox

INPUT
- File: {FILENAME}
- Type: {report / contract / invoice / other}
- Owner: {OWNER} (default: me)

STEPS
1. Read and summarize {FILENAME}.
2. Extract the date, sender, subject, action items, and
   deadline.
3. Save the summary as Summary_{FILENAME}.md.
4. Move the original by type:
   report   -> Reports/{YYYY}/
   contract -> Contracts/{CLIENT}/
   invoice  -> Finance/Invoices/{YYYY-MM}/
5. Add a row to Logs/doc_log.csv.

Never overwrite a file; if the name exists, add _01, _02. Before
moving anything the first time, show me the plan and wait for my
approval.

OUTPUT
- A summary ready to read
- The original filed in the right folder
- The log updated

CHECK
- The summary has all five extracted fields
- The log has one new row per document
