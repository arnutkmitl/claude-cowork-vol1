# Chapter 4 prompts: Delegate Documents and Files

Copied from the book. Replace every `{PLACEHOLDER}` with your own details before you send a prompt; `{option / option}` means pick one, and `{e.g., ...}` is a hint to replace.

## Lab 4.1: Summarize a 30-page report in minutes

Step 1: paste `cedar_peak_annual_report.txt` into a new conversation.

### Step 2: summary at three levels (the chapter's template; add it below the data)

```text
{ATTACH THE FILE OR PASTE THE CONTENT}

Summarize this at three levels.

Level 1: one post (280 characters), to share in team chat.

Level 2: briefing, five bullet points, for a team that has two
minutes. No more than two sentences per bullet.

Level 3: executive summary, 200 words, for a manager who must
decide. Include the main point, the key figures, and what needs
to happen next.

Do not add anything that is not in the document.
```

### Step 3: extract strategic insights

```text
Based on this report, answer directly and support each answer
with figures from the report:
1. What is the biggest growth opportunity?
2. What is the most urgent problem to fix?
3. If you were CEO with an extra $100,000 to invest this year,
   where would you put it, and why?
4. Which number is most worrying, and should be watched closely?
```

### Step 4: write the team update

```text
Write an internal email to all 45 employees.
Subject: last year's results and our direction for this year.
Tone: motivating and forward-looking. Be honest about the
challenges without causing alarm. About 250 words.
```

## Walkthrough: screen job applications consistently

Paste `recruitment/recruitment-project-instructions.md` into a Project named "Recruitment", then assess the candidates in `recruitment/sample_applications.txt` one at a time.

### Assess one candidate

```text
Assess this candidate against the criteria in this Project:
{PASTE ONE CANDIDATE}

Give me:
1. A score from 1 to 5 for each criterion, with the reason
2. Three strengths
3. Two concerns
4. Category: Shortlist / Review / Not qualified
5. Three interview questions (for Shortlist or Review)
```

### Compare all three

```text
Based on your assessments of all three candidates:
1. A comparison table with a column per candidate and a row per
   criterion; scores plus a short note in each cell
2. A ranking with reasons
3. Questions for the next interview round, for shortlisted
   candidates
4. Anything the recruiter might overlook
```

### Recruitment log

```text
Create a recruitment log as CSV with these columns:
date received, candidate, role, category, total score,
main reason, next step, owner.
Add a row for each candidate and one empty row as a template.
```

### Whole folder, in the desktop app

```text
For each PDF in HR/Applications, assess the candidate using the
criteria in the Recruitment Project. Save a summary for each as
Summary_{CANDIDATE}.md in HR/Candidates, and add a row for each
to HR/recruitment_log.csv. Show me the log when you are done.
```
