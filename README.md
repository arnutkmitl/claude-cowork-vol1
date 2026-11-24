# Claude Cowork: Build Your Own AI Team

Companion files for the book *Claude Cowork: Build Your Own AI Team: Automate Tasks, Delegate Work, and Boost Productivity with AI Agents* by Arnut Ruttanatirakul, published by SysAdmin Knowledge Press ([www.sysadmin.in.th](https://www.sysadmin.in.th)).

This repository holds the sample data, templates, and skills used in the book, so you can copy them instead of retyping them from the page.

## What is in this repository

- **Sample data** for the labs and walkthroughs: CSV files and sample documents, with the same values, column names, and file names the book uses. All companies, people, and figures in them are fictional.
- **Prompts** from each chapter's lab and walkthroughs, in a `prompts.md` file per chapter.
- **Project instructions, style guides, and task templates** that the book asks you to fill in and save.
- **Appendix A's 50 prompt templates**, one file per template, in `templates/`.
- **The example skill from Appendix B**, `office-writing`, as a folder and as a ZIP file ready to upload, in `skills/`.

## Chapter and lab map

| Chapter | Lab | Folder | Main files |
|---|---|---|---|
| 1. Meet Claude, Your New AI Coworker | Lab 1.1: Create your first Claude Project | [`ch01/`](ch01/) | Project instructions template, test prompts |
| 2. Set Up Your AI Workspace | Lab 2.1: Set up Projects for three kinds of work | [`ch02/`](ch02/) | `company_profile.md`, instructions for three Projects |
| 3. The Art of Delegating to AI: Prompt Engineering | Lab 3.1: Improve a prompt in three rounds | [`ch03/`](ch03/) | Template library layout, language defaults, lab prompts |
| 4. Delegate Documents and Files | Lab 4.1: Summarize a 30-page report in minutes | [`ch04/`](ch04/) | `cedar_peak_annual_report.txt`, recruitment walkthrough files |
| 5. Claude as Your Team's Writer and Editor | Lab 5.1: Build a content factory | [`ch05/`](ch05/) | Style guide template and example, content factory prompt |
| 6. Analyze Data and Build Reports | Lab 6.1: Analyze 12 months of sales and brief the CEO | [`ch06/`](ch06/) | `northwind_sales_last_year.csv` and four more datasets |
| 7. Manage Email and Workplace Communication | Lab 7.1: Build a daily communication workflow | [`ch07/`](ch07/) | Email Assistant Project instructions, briefing prompts |
| 8. Put Claude to Work in Google Workspace | Lab 8.1: Build a full pipeline from Sheet to email | [`ch08/`](ch08/) | `project_tracker.csv`, pipeline prompts |
| 9. Automate Repetitive Work | Lab 9.1: Build a daily inbox processor | [`ch09/`](ch09/) | Four task templates, including the inbox processor |
| 10. Build Your Personal Automation System | Lab 10.1: Build a document factory | [`ch10/`](ch10/) | `Claude-Work/Factory/proposal_template.txt`, `Claude-Work/Factory/clients_data.csv` |
| Appendix A: 50 Prompt Templates | | [`templates/`](templates/) | `A-01` to `A-50`, with an index |
| Appendix B: Build Your Own Skills | | [`skills/`](skills/) | `office-writing/`, `office-writing.zip` |

Each folder has its own README that says which file goes with which step, and what the lab expects you to bring yourself (your own inbox, your own test files, and so on).

## How to download

1. On this repository's page on GitHub, click the green **Code** button.
2. Choose **Download ZIP**.
3. Unzip the file into a folder you can find again, for example `Documents/claude-cowork-vol1`.

If you use Git, you can clone it instead:

```text
git clone https://github.com/arnutkmitl/claude-cowork-vol1.git
```

For the desktop-app labs in Chapters 9 and 10, copy the files you need into the working folder you gave Claude access to in Chapter 2 (for example `Documents/Claude-Work`). Do not give Claude access to this whole download folder.

## A note on features that change

Anthropic updates Claude often. The book describes the Claude apps as they were in late 2026, and the files here match the book. If a menu item has moved or been renamed, search the Claude Help Center at [support.claude.com](https://support.claude.com), or ask Claude: "Where do I find {FEATURE} in the current version?" The prompts and methods do not depend on where a button sits.

## License

- **Code and sample data files** (the `.csv`, `.txt`, and `.py` files, and `skills/office-writing.zip` as a package) are released under the MIT License; see [LICENSE](LICENSE).
- **Prompt templates and text** (the Markdown files, including the templates, prompts, Project instructions, style guides, and the skill's instructions) are © 2026 Arnut Ruttanatirakul. They are provided for readers' personal and internal business use: copy them, adapt them, and use them in your own work and your organization's work.

The data is fictional and provided as is, for practice. Review anything Claude produces from it, and from your own data, before you rely on it.
