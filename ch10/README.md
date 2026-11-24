# Chapter 10: Build Your Personal Automation System

| File | Used in | What to do with it |
|---|---|---|
| `Claude-Work/Factory/proposal_template.txt` | Lab 10.1, Step 1 | Copy to `Claude-Work/Factory/` in your working folder |
| `Claude-Work/Factory/clients_data.csv` | Lab 10.1, Step 2 | Copy to the same folder |
| `examples/undo_log_example.csv` | "Principle 2: always keep an undo log" | An example of the log format; nothing to run |
| `prompts.md` | Invoice pipeline, report combining, Lab 10.1, Step 3, the monthly audit | Copy each prompt into Claude |

The `Claude-Work/` folder here mirrors the paths the lab uses. Copy the whole `Factory` folder into your own `Claude-Work` folder (for example `Documents/Claude-Work/Factory`), so the paths in the factory task match.

The book prints `clients_data.csv` with each record wrapped over several lines; here the file has four lines, a header and three records, as the lab requires. The `TOTAL_AMOUNT` values are written as in the book (`$8500`), without a thousands separator, so they stay one CSV field.

## Expected result

Three proposals (for example `PROP-2027-001` to `PROP-2027-003`; the year is the current one), in `Factory/Output/`, with no `{{` or `}}` left, and `Factory/proposal_index.csv` listing all three with a total of $71,500 ($8,500 + $25,000 + $38,000). For Step 4, add a fourth client row of your own to the CSV; the next run should create only the next number, such as `PROP-2027-004`.

## Not included

The invoice pipeline and the report-combining prompt work on your own invoices and team reports; the book does not supply sample invoices or reports. Claude creates `Finance/invoice_master.csv`, `Factory/proposal_index.csv`, and the logs itself.
