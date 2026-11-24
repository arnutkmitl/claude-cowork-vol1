# Chapter 7 prompts: Manage Email and Workplace Communication

Copied from the book. Replace every `{PLACEHOLDER}` with your own details before you send a prompt; `{option / option}` means pick one, and `{e.g., ...}` is a hint to replace.

## Daily triage

```text
You are an experienced executive assistant. Review the emails I
received today {or: the unread emails in my inbox}.

Sort them into:
1. Urgent: needs a reply or action today (say what action)
2. Important: reply within 24 to 48 hours
3. Can wait: reply this week
4. Archive: no reply needed (newsletters, CCs, notifications)
5. Today's action items, as a checklist

Keep each entry to two lines or fewer.
```

### Rules for sorting (added after the worked example)

```text
Rules for sorting:
- Never put a message in Archive if it mentions a deadline,
  payment, invoice, contract, lease, or renewal.
- For each Archive item, show the sender and the exact subject
  line, so I can check the whole group in ten seconds.
```

## Walkthrough: a smart email assistant Project

Instructions: `email-assistant-project-instructions.md`. Then test it with these requests.

### Test 1

```text
Draft a follow-up to Alex Morgan, a client. I sent a quote five
days ago and have not heard back.
```

### Test 2

```text
Politely decline a meeting invitation from a vendor. Say we are
busy right now but interested in two months.
```

### Test 3

```text
Summarize this email and tell me what I need to do:
{PASTE A THREAD}
```

## Lab 7.1: Build a daily communication workflow

### The routine you will build

```text
Morning (8:00 to 8:15)
|-- Morning briefing: today's email and calendar
`-- Priorities: the three most important tasks today

Midday (12:00 to 12:15)
|-- Inbox check: what arrived this morning
`-- Quick replies: drafts for urgent messages

Evening (5:00 to 5:15)
|-- Wrap-up: what got done
|-- Tomorrow: agenda and preparation
`-- Follow-ups: what to chase tomorrow
```

### Step 1: the morning briefing prompt

```text
Morning briefing for {DATE}.
Email: everything that arrived since yesterday evening
{or paste the emails}.
Calendar: today's events {or paste the schedule}.

Use this layout:
Good morning, {DATE}
Email: {N} new, {N} urgent
Calendar: {N} events; first at {TIME}
Do first:
1. {MOST URGENT}
2. {NEXT}
Today's focus (top three):
1. ...
2. ...
3. ...
Don't forget:
- {FOLLOW-UPS OR PREPARATION}

No more than 150 words; readable in 30 seconds.
```

### Step 2: the end-of-day prompt

```text
End-of-day wrap-up for {DATE}.
Done today: {LIST, or check my sent mail and calendar}
Still open: {UNANSWERED EMAILS, or find them in my inbox}
Tomorrow: {SCHEDULE, or read my calendar}

Layout:
## End of day, {DATE}
Done today: (bullets)
Still open: (with priority)
Emails to answer tomorrow: (by priority)
Key items tomorrow: (meetings, tasks, deadlines)
Follow-ups: (who to chase, about what)
```
