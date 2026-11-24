# Chapter 3 prompts: Prompt Engineering

Copied from the book. Replace every `{PLACEHOLDER}` with your own details before you send a prompt; `{option / option}` means pick one, and `{e.g., ...}` is a hint to replace.

## Iterative prompting: three feedback patterns

### Pattern 1

```text
The {PART} works well. In the {PART}, please {CHANGE}.
```

### Pattern 2

```text
Please revise it so that:
- {CHANGE 1}
- {CHANGE 2}
Keep everything else as it is.
```

### Pattern 3

```text
Right now it reads like this: {EXCERPT}.
I want it to read more like this: {EXAMPLE}.
```

## Walkthrough: build your personal template library

### Example list of repeated tasks

```text
1. Answer customer emails asking for prices
2. Summarize meeting notes
3. Write the company's social media posts
4. Analyze weekly sales
5. Draft proposals for new projects
```

### Ask Claude to draft each template

Save each tested template in the layout of `template-library-entry.md`.

```text
I do this task often: {TASK}
Details: {WHAT THE TASK INVOLVES}
The output I need: {DESCRIPTION}

Write a prompt template for this task. Use {VARIABLE} for
anything that changes each time, so I can fill in the values
and use it immediately.
```

## Lab 3.1: Improve a prompt in three rounds

### Round 1: start vague

Send this prompt exactly as written.

```text
Write a LinkedIn post introducing myself.
```

### Round 2: add context and format

```text
Write a LinkedIn post introducing {NAME}, who has worked as
{ROLE} at {COMPANY} for {N} years.
Expertise: {THREE MAIN SKILLS}
Recent achievement: {ONE RESULT YOU ARE PROUD OF}
People I want to connect with: {e.g., HR managers, IT directors}

Format:
- A hook in the first one or two sentences
- Three or four short paragraphs
- A closing call to action that invites people to connect
- Five hashtags at the end
- 200 to 250 words in total
- Professional but human; not stiff
```

### Round 3: fine-tune with feedback

```text
The {PART THAT WORKS} is good. Please change:
- {CHANGE 1}
- {CHANGE 2}
Keep everything else the same.
```

### Save the final prompt

```text
Write the single prompt that would have produced this final
post in one step, so I can save it as a template.
```
