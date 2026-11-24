# Chapter 1 prompts: Meet Claude, Your New AI Coworker

Copied from the book. Replace every `{PLACEHOLDER}` with your own details before you send a prompt; `{option / option}` means pick one, and `{e.g., ...}` is a hint to replace.

## Walkthrough: one request, three prompts

Start a new conversation for each prompt.

### Prompt 1: vague

```text
Write an email postponing a meeting.
```

### Prompt 2: some context

```text
Write an email moving this Friday's meeting to next week.
It goes to my team of five because something came up.
```

### Prompt 3: complete context

```text
Write an email for this situation.

From: me (Alex, team manager)
To: my team of five (Sam, Priya, Daniel, Mei, Tom)
Subject: Weekly sync moved

Details:
- Original time: Friday, March 28, 2:00 p.m.
- New time: Monday, March 31, 10:00 a.m.
- Reason: I have to visit a client out of town at short notice
- Action: ask everyone to confirm the new time works

Tone: friendly, apologize for the short notice
Length: under 100 words
```

## Lab 1.1: Create your first Claude Project

Step 2 uses `project-instructions-template.md` in this folder. Step 4: send these three tests one at a time in a new conversation inside the Project.

### Test 1

```text
What do you know about me and my work?
```

### Test 2

```text
Write a thank-you email after a first meeting with a new client.
```

### Test 3

```text
Analyze this data for me.
```
