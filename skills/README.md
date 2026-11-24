# Skills

The example skill from Appendix B, "Build Your Own Skills, and Where to Learn More."

| Path | What it is |
|---|---|
| `office-writing/SKILL.md` | The office productivity skill exactly as printed in Appendix B |
| `office-writing/assets/minutes.md` | The minutes layout that `SKILL.md` refers to, built from template A-05 |
| `office-writing.zip` | The same folder, packaged and ready to upload |

Before you upload it, open `office-writing/SKILL.md` and replace `{COMPANY}` in the description with your organization's name. Change any other details to match how your organization writes. If you edit the files, rebuild the ZIP as described below.

Read every file in a skill before you install it, including this one. A skill can contain instructions and scripts that Claude will follow with the same access you have given it, including your connectors and folders.

## Package the skill

Compress the folder itself, not the files inside it, into a ZIP file. When you open the ZIP, you should see the folder `office-writing/` with `SKILL.md` inside it. A `SKILL.md` at the top level of the ZIP is not recognized, and this is the most common reason an upload fails.

`office-writing.zip` in this folder is already packaged this way.

## Install the skill

1. Check that **Create and edit files** is on under **Settings** > **Capabilities**. Skills need file creation.
2. Open **Plugins** in the sidebar, the page that holds your skills, connectors, and plugins.
3. Upload the ZIP file as a custom skill.
4. Find the skill on the **Plugins** page and make sure it is switched on.

## Test the skill

Test it in a new conversation with three requests:

1. A request that clearly matches: "Draft the minutes from these notes."
2. A request phrased the way a busy colleague would say it: "Can you tidy this up into something I can send the team?"
3. A request that should *not* trigger it, such as a question about a spreadsheet formula.

If the first two do not load the skill, add the words you used to the description. If the third one does, narrow the description. Edit, upload the new version, and test again. Two or three rounds are normal.

## Skills to build next

Appendix B suggests these starter skills. The text to start from is in this repository:

| Skill | What it does | Start from |
|---|---|---|
| `meeting-minutes` | Turns rough notes or a transcript into minutes with action items | Chapter 4, `templates/A-05-meeting-minutes-from-notes.md` |
| `email-replies` | Drafts replies in your voice with a check-before-sending list | Chapter 7, `templates/A-06` to `A-09` |
| `brand-voice` | Applies your style guide to any piece of writing | Chapter 5, `ch05/style_guide_template.md` filled in with your brand voice |
| `weekly-report` | Builds the weekly report from a sheet or pasted figures | Chapter 6, `templates/A-48-weekly-report.md` |
| `inbox-processor` | Reads, summarizes, files, and logs new files in a folder | Chapter 9, `ch09/task-templates/inbox-processor.md` |
| `proposal-factory` | Fills a proposal template from a data file | Chapter 10, `ch10/Claude-Work/Factory/` |

Features change. If a menu label above has moved, check the Claude Help Center at support.claude.com.
