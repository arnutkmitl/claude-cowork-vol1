# Chapter 5 prompts: Claude as Your Team's Writer and Editor

Copied from the book. Replace every `{PLACEHOLDER}` with your own details before you send a prompt; `{option / option}` means pick one, and `{e.g., ...}` is a hint to replace.

## Walkthrough: test your brand voice

### Method 1: derive a style guide from existing content

Replace the three pieces with your own.

```text
You are a brand communication specialist. I want a style guide
for my organization. Here are three pieces we have published.

Piece 1 (social media post):
"Hi everyone! Today the BrightPath team is introducing a new
service that helps your business grow faster. Get in touch
anytime."

Piece 2 (customer email):
"Dear Ms. Lee, thank you for placing your trust in our team.
We are here to support your business every step of the way."

Piece 3 (website article):
"Choosing the right technology is the key to..."

Analyze all three and write a style guide in Markdown that I can
give to Claude.
```

### Line to put above the style guide in your writing Project

```text
Whenever you write content, follow the style guide below.
```

## Lab 5.1: Build a content factory

Step 3: replace the topic and the style guide section with yours.

```text
You are an experienced content strategist.

Topic: "How to save two hours a day with AI"

Our style guide:
- Voice: friendly and encouraging
- Readers: office professionals aged 25 to 40
- Address readers as "you"; refer to ourselves as "we"

Create five formats from this topic:
1. LinkedIn post (200 words): a short story, three bullet
   points, and five hashtags
2. Email newsletter (250 words): subject line, body, and call
   to action
3. Chat or SMS broadcast (80 words): short and easy to read on
   a phone
4. Thread for X or Threads (five posts): each under 280
   characters
5. Presentation outline: six slide titles, three bullets each

Put a clear heading above each format.
```
