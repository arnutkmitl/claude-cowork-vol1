# A-50: Complex multi-part task

Use for any large task that mixes instructions, data, and rules.

```text
<role>
You are {ROLE AND EXPERTISE}.
</role>

<context>
{THE SITUATION, ORGANIZATION, AND BACKGROUND}
</context>

<data>
{PASTE THE DATA OR ATTACH FILES}
</data>

<task>
{EXACTLY WHAT YOU NEED, IN CONCRETE TERMS}
</task>

<format>
{STRUCTURE OF THE OUTPUT: HEADINGS, TABLES, NUMBER OF POINTS}
</format>

<constraints>
- Use only the information in <data>; never invent figures
- {OTHER RULES}
</constraints>
```

Source: *Claude Cowork: Build Your Own AI Team*, Appendix A, Thinking tools and routines.
