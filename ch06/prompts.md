# Chapter 6 prompts: Analyze Data and Build Reports

Copied from the book. Replace every `{PLACEHOLDER}` with your own details before you send a prompt; `{option / option}` means pick one, and `{e.g., ...}` is a hint to replace.

## Lab 6.1: Analyze 12 months of sales and brief the CEO

Step 1: the data is `northwind_sales_last_year.csv`. Paste it where the prompt says {PASTE THE DATA}.

### Step 2: get the overview

```text
Analyze Northwind Cloud's sales for last year.
{PASTE THE DATA}

Summarize in five points:
1. Total revenue for the year against the total target
2. Best and worst months, with possible reasons
3. The trend over the year: rising, falling, or volatile
4. How many months fell below target
5. The single most worrying number
```

### Step 3: build a dashboard

In the same conversation, without pasting the data again.

```text
Build a dashboard with HTML and Chart.js showing:
1. A line chart of actual revenue against target for 12 months
2. A bar chart of monthly orders
3. KPI cards: total revenue, % of target, best month, and
   second-half growth over the first half
Blue as the main color, white background, professional look.
```

### Step 4: write the executive summary

```text
Write a 200-word executive summary for the CEO:
- Results, with the key figures
- Strengths this year
- Challenges
- Three recommendations for next year
Formal and concise. Support every claim with a figure from the
data.
```

### Step 5: dig deeper

```text
February was the weakest month. Based on this data, what three
practical steps would you take to lift February sales next
year?
```

## Walkthrough: a weekly report generator

### Design the template

```text
Help me build a "weekly report generator" prompt for my sales
team. Every Friday we report:
- Daily revenue, Monday to Friday
- Number of customers contacted
- Deals closed
- Deals in the pipeline
- The weekly target

Create a prompt template that:
1. Has clear {PLACEHOLDERS} for the data
2. Produces a one-page report with a summary of the week, a
   traffic-light status, what went well, what to improve, and
   the focus for next week
3. Suits a report sent to a manager every Friday

Make it as easy to use as possible.
```

### Test it with sample data (`week12_sample.txt`)

```text
Week 12 (March 16 to 20)
Daily revenue:
Monday:    $8,500 (3 orders)
Tuesday:   $12,000 (4 orders)
Wednesday: $9,500 (3 orders)
Thursday:  $14,500 (5 orders)
Friday:    $7,800 (2 orders)
Customers contacted: 42
Deals closed: 17 (40.5% conversion)
Pipeline: 28 deals worth $124,000
Weekly target: $50,000
```

### Refine it

```text
This works. Three changes:
1. Add a "Most interesting deal this week" section after the
   KPIs
2. Cut any bullet longer than two lines
3. End with one sentence that encourages the team
Update the template and regenerate the report.
```

## Worked example: a growth rate on the wrong base

The data is also in `q1_revenue_by_region.csv`.

### The original request

```text
Compare Q1 this year with Q1 last year by region. Give the
growth rate for each region and in total, and rank the regions.

region, q1_2026_usd, q1_2025_usd
Northeast, 176000, 149000
Midwest, 71000, 62000
South, 54000, 50000
West, 45000, 40000
Mountain, 39000, 34000
```

### The follow-up

```text
Your growth rates use this year as the base. Growth must be
(this year - last year) / last year. Recalculate every region
and the total, and add a column showing the division for each
row so I can check it.
```
