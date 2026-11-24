TASK: Weekly report compiler
WHEN: Fridays at 4:30 p.m.

INPUT
- Week number: {WEEK}
- Sales data: {SALES FILE OR SHEET}
- KPI data: {KPI FILE OR SHEET}
- Recipients: {EMAIL ADDRESSES}

STEPS
1. Read the sales and KPI data.
2. Analyze it with the weekly report template saved in this
   Project (run the task inside your Reports Project).
3. Create "Weekly Report, week {WEEK}" as a document.
4. Create a Gmail draft to {RECIPIENTS} with the subject
   "Weekly report, week {WEEK}" and a five-point summary.
5. Tell me the report is ready for my review. Do not send it.

OUTPUT
- The report document
- A Gmail draft waiting for my approval

CHECK
- Every section of the report is filled in
- The draft is in Gmail Drafts
