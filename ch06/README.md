# Chapter 6: Analyze Data and Build Reports

All figures are invented, for the fictional software company Northwind Cloud.

| File | Used in | Notes |
|---|---|---|
| `northwind_sales_last_year.csv` | Lab 6.1, Step 1; the trend-line prompt (same revenue figures) | 12 months: revenue, orders, new customers, target |
| `sales_jan_mar.csv` | "Three ways to send data" | Q1 this year, monthly |
| `q1_sales_vs_target_by_region.csv` | "A bar chart against target" | Five regions, Q1 sales and target |
| `kpi_dashboard_march.csv` | "A KPI dashboard" | For cost per lead, lower is better |
| `q1_revenue_by_region.csv` | Worked example "a growth rate on the wrong base" | Newest quarter first, exactly as Dana exported it |
| `week12_sample.txt` | Walkthrough "a weekly report generator" | Sample data to test the generator |
| `summary_stats.py` | "Send summary statistics" | Reads `data.csv`, which must have `category` and `sales` columns; edit the file and column names to match your data. Needs `pip install pandas` |
| `prompts.md` | Lab 6.1, the walkthrough, the worked example | Copy each prompt into Claude |

The book prints the data with a space after each comma, and the chart and dashboard data as tables with thousands separators. The CSV files hold the same column names and values in plain CSV form, without those spaces and separators, so they open cleanly in Excel or Google Sheets.

## Expected results for Lab 6.1

From the book's "Check your result":

- Total revenue $1,633,000 against a $1,535,000 target (106.4%).
- Four months below target: January, February, April, and July.
- Best month: December ($192,000).
- Second-half growth over the first half: 28.7% ($919,000 against $714,000).

If Claude's figures differ, ask it to recalculate from the data and show its working.

## Expected results for the worked example

Growth is measured against the earlier period: (this year - last year) / last year. The correct total is 14.9% ($50,000 / $335,000), and Northeast is 18.1%. A reply that gives 13.0% in total has used this year as the base.
