# Harry's vault

Personal Obsidian vault for work and project tracking. Plain markdown; edit with care.

## Structure
- `Daily Notes/YYYY-MM-DD.md` - one per day. Tasks at top, then a `## [[Project - Project]]` section per project worked on, plus notes.
- `Projects/<Name> - Project.md` - one hub note per project (HOPS, Shift Report, Sales Tracker, Forecasting Tool, Carbon Collaborate). Daily notes link back to these.
- `Meetings/YYYY-MM-DD <title>.md` - meeting notes, linked from the relevant project hub.
- `People/<First name>.md` - one note per recurring person, with a tasks query and a mentions search. Link people with `[[Name]]` (first name only) in meeting notes and tasks; use links, not tags, for people.
- `Templates/Daily Note Template.md` - template used for new daily notes (Focus query of tasks scheduled today, Due or overdue query, Notes, End of day).
- `Inbox/Mac to do.md` - misc personal to-dos. `Home.md` - dashboard: project links and task queries (overdue, next 7 days, untagged).

## Conventions
- Tasks use the Obsidian Tasks plugin format: `- [ ] text 📅 YYYY-MM-DD ⏳ YYYY-MM-DD 🔺/🔼` and `✅ date` when done. Preserve these emoji exactly.
- **Task tags** (fixed list, one per task written in a daily note): `#HOPS`, `#shift-report`, `#sales-tracker`, `#forecasting`, `#carbon`, `#admin`. Tasks in project notes get their project from the file; each project hub has a `tasks` query on its tag. Flag misspelt, missing or unlisted tags in audits.
- `tasks` query blocks: the Tasks plugin Global Query already applies `hide toolbar` and `hide task count`, so don't add them to new queries.
- Link projects with `[[Name - Project]]`; link days with `[[YYYY-MM-DD]]`.
- Project hub notes link to GitHub issues (e.g. `harryscully/hops-web#NNN`).

## Daily routine
- **Morning:** create today's note, read the "Due or overdue" query, pick up to three tasks for today. Existing tasks are chosen by giving them a scheduled date of today (⏳), never by copying or retyping them. New tasks that don't exist yet are written straight into Top 3. A task lives in exactly one place.
- **During the day:** tick tasks wherever they appear (daily note, project hub or query).
- **End of day:** "Done" is a few words. "Carry over / blocked" holds only what a task line can't say (where I stopped, who I'm waiting on, decisions needed). Unfinished tasks reappear in tomorrow's query automatically, so don't list or copy them. Delete tasks I won't do, or give them a later date.
- **Weekly (Friday):** open `Home.md`, clear Overdue, make sure Untagged is empty, review Waiting or scheduled later.
- Audits should flag: tasks copied between daily notes, undated tasks left in old daily notes, and days with a blank "Carry over / blocked".

## Rules for Claude
- Default to **read-only audits**: report findings, do not edit unless asked.
- Never delete notes or rewrite my wording; suggest changes instead. Never touch `.obsidian/` or `.git/`.
- Don't reformat task lines or change dates.
- Before any edits, make sure `git status` is clean so changes are one reviewable diff.

## What I want from audits
- Orphan notes, broken `[[links]]`, duplicate topics, inconsistent naming.
- Tasks: overdue, undated, or carried over repeatedly across daily notes.
- Open tasks in daily notes with no tag, or with a tag not in the list above.
- Project hubs that are stale or have open questions never followed up in daily notes.
- Patterns in how I use the vault (git history, task completion rate, what I capture but never process) and concrete tips to be more efficient, ideally the top 3 changes by time saved.
