TASK: Daily file organizer
WHEN: every evening, or whenever Downloads gets messy

INPUT
- Source folder: {SOURCE} (default: Claude-Work/Downloads-copy)
- Date: {DATE} (default: today)

STEPS
1. List every file in {SOURCE}.
2. Sort by extension (all destinations inside Claude-Work/Sorted/):
   .pdf .docx .xlsx .pptx -> Work/{YYYY-MM}/
   .jpg .png .gif .webp   -> Images/{YYYY-MM}/
   .mp4 .mov              -> Videos/
   .zip .7z               -> Archives/
   .exe .dmg .pkg .msi    -> Installers/
   anything else          -> Misc/
3. Rename each file to {YYYY-MM-DD}_{original name}, using the
   file's modified date.
4. Write a log, organized_{DATE}.csv, with the original path,
   the new path, and the time.

OUTPUT
- Files moved and renamed
- The log in Claude-Work/Logs/

CHECK
- {SOURCE} contains only files you chose to leave
- The log lists every file that moved

Before moving anything, show me the plan and wait for my
approval.
