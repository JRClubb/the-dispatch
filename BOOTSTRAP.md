---
modified: 2026-05-14
---
# The Dispatch - Client Bootstrap

The Dispatch is an Obsidian + Claude Code operating loop:

```text
Capture -> Process -> Plan -> Work -> Close -> Improve
```

Paste this file into Claude Code from inside a new Obsidian vault. Claude Code will interview the user, create the folder structure, write the operating files, and install the slash commands.

---

## Claude Code Instructions

You are building a Dispatch installation for a new user.

Keep the first install simple. Build the core loop. Do not add optional modules unless the user explicitly asks for them.

Do not build until the interview is complete.

---

## Step 1 - Interview

Send this:

```text
You are building The Dispatch.

It is a local work system for capturing what comes in, processing it, planning the day, doing the work, and closing the loop so tomorrow starts with context instead of static.

The system gets better because the record gets better.

A few questions before I build it.
```

Ask:

```text
1. What is your first name?
2. What kind of work should this vault support?
3. What are your one or two active goals or projects right now?
4. What usually enters your inbox: notes, meetings, articles, client work, ideas, tasks, research, or something else?
5. What kind of mornings should the Daily Spark create?
6. What tones should the relay use, and what tones should it avoid?
7. Should this install lean more toward creativity, business, reflection, relationships, learning, or operations?
```

Parse answers as:

- `NAME`
- `WORK`
- `GOALS`
- `INBOX_TYPES`
- `SPARK_STYLE`
- `TONE_USE`
- `TONE_AVOID`
- `LEAN`
- `TODAY` as `YYYY-MM-DD`

---

## Step 2 - Create Folders

Create exactly this structure:

```text
Human/
Human/01 - Inbox/
Human/03 - Journal/
Human/03 - Journal/Daily/
Human/03 - Journal/Templates/
Human/04 - Writing/
Human/04 - Writing/Drafts/
Human/04 - Writing/Voice Reference/
Human/05 - Work/
Human/05 - Work/Clients/
Human/05 - Work/Finance/
Human/05 - Work/Operations/
Human/05 - Work/Outreach/
Human/05 - Work/Pipeline/
Human/05 - Work/Projects/
Human/05 - Work/Social/
Human/05 - Work/TaskNotes/
Human/05 - Work/TaskNotes/Tasks/
Human/05 - Work/Templates/
Human/06 - Research/
Human/06 - Research/Captures/
Human/06 - Research/Ideas/
Human/06 - Research/Research/
Human/07 - Life/
Machine/
Machine/Briefing/
Machine/Briefing/sessions/
Machine/Personalization/
Machine/Plans/
Machine/Sessions/
Machine/Systems/
System/
System/Archive/
99 - ASSETS/
.claude/
.claude/commands/
```

Do not create old station folders such as `00 - DEAD DROP`, `01 - DISPATCHES`, `02 - INTEL`, `03 - WORKS`, `04 - OPS`, `05 - VITALS`, or `06 - RELAY`.

---

## Step 3 - Create Operating Files

Create `AGENTS.md` and `.claude/CLAUDE.md` with the same content:

```markdown
# The Dispatch - [NAME]'s Operating File

Read first every session:

1. `Machine/Briefing/north-star.md`
2. `Machine/Briefing/top-of-mind.md`
3. `Machine/Briefing/about.md`
4. `Machine/Personalization/relay-style.md`

## Role

You are the relay for [NAME]'s Dispatch installation.

You help preserve context, process intake, plan the day, close loops, and surface useful signal. You think with the user. You do not replace their judgment, writing, or work.

## Default Stance

Stay in thinking mode unless the user explicitly asks for a finished artifact, draft, email, file, task, or post.

## Folder Map

- `Human/01 - Inbox/` - raw intake
- `Human/03 - Journal/` - daily notes and reviews
- `Human/04 - Writing/` - drafts and outputs
- `Human/05 - Work/` - projects, clients, tasks, pipeline, money
- `Human/06 - Research/` - captures, ideas, sources, synthesis
- `Human/07 - Life/` - personal context when needed
- `Machine/` - briefing, plans, sessions, system files
- `System/` - install docs and archive
- `99 - ASSETS/` - attachments and media

## Write Rules

Write freely in `Machine/`, `Human/01 - Inbox/`, and approved work outputs.

Ask before overwriting human-authored writing, journal entries, or briefing files.

Daily notes are human-authored records. Machine sections must be clearly marked.

## Operating Loop

Capture -> Process -> Plan -> Work -> Close -> Improve
```

Create `Machine/Briefing/north-star.md`:

```markdown
# North Star

## Work This Vault Supports

[WORK]

## Active Goals

- [GOAL 1]
- [GOAL 2 if provided]

## What This System Is For

To keep context alive across days, process what enters, and make the next useful move visible.
```

Create `Machine/Briefing/top-of-mind.md`:

```markdown
# Top Of Mind

## Live Now

- [GOAL 1]
- [GOAL 2 if provided]

## Inbox Pattern

[INBOX_TYPES]

## Next Useful Step

Run `/daily-spark`, write into the daily note, then run `/today`.
```

Create `Machine/Briefing/about.md`:

```markdown
# About [NAME]

## Work

[WORK]

## Current Focus

[GOALS]
```

Create `Machine/Personalization/relay-style.md`:

```markdown
# Relay Style

## Use

[TONE_USE]

## Avoid

[TONE_AVOID]

## System Lean

[LEAN]
```

Create `Machine/Personalization/daily-spark-prompt.md`:

```markdown
# Daily Spark Personalization

## Desired Morning

[SPARK_STYLE]

## Lenses

- Great Dreamer: image, memory, intuition, strangeness, possibility
- Great Thinker: deeper question, frame, live idea
- Great Contrarian: challenge stale assumptions without nagging
- Great Ghost: answer from the user's own archive, values, and prior words
- Great Stranger: reflect what the vault says from the outside

## Avoid

[TONE_AVOID]
```

Create `Human/03 - Journal/Templates/Daily Note Template.md`:

```markdown
---
date: {{date}}
author: user
---
# {{date}}

## Daily Spark

> [!relay] Daily Spark
> [/daily-spark writes here]

---

## Notes

Write here.

---

## Plan

> [!relay] Today
> [/today writes here]

---

## Close

> [!relay] Close
> [/close writes here]
```

Create today's daily note at `Human/03 - Journal/Daily/[TODAY].md` from the template.

---

## Step 4 - Install Core Commands

Create the following files in `.claude/commands/`.

### `.claude/commands/start.md`

```markdown
---
description: Orient the user and check the Dispatch vault structure.
---

# /start

Check that the expected folders exist:

- `Human/01 - Inbox/`
- `Human/03 - Journal/`
- `Human/04 - Writing/`
- `Human/05 - Work/`
- `Human/06 - Research/`
- `Human/07 - Life/`
- `Machine/Briefing/`
- `Machine/Personalization/`
- `Machine/Plans/`
- `Machine/Sessions/`
- `Machine/Systems/`
- `System/Archive/`
- `99 - ASSETS/`

Read `Machine/Briefing/north-star.md`, `Machine/Briefing/top-of-mind.md`, and `Machine/Personalization/relay-style.md`.

Return what is set up, what is missing, and the next useful command to run. Keep it short.
```

### `.claude/commands/interview.md`

```markdown
---
description: Build or refresh the user's operating profile.
---

# /interview

Ask only what is needed to personalize the system:

1. What work should this vault support now?
2. What is active this month?
3. What should the relay remember about tone?
4. What should the relay avoid?
5. What kind of Daily Spark makes the user want to write?
6. What topics are energizing?
7. What topics are draining, nagging, or off-limits?

Update `Machine/Briefing/` and `Machine/Personalization/`. Ask before overwriting existing user-authored briefing text. Prefer small patches.
```

### `.claude/commands/daily-spark.md`

```markdown
---
description: Generate the daily note starter.
---

# /daily-spark

Create or update today's daily note at `Human/03 - Journal/Daily/YYYY-MM-DD.md`.

Read the last 3 daily notes, the last 7 Daily Spark sections for repetition, `Machine/Briefing/top-of-mind.md`, `Machine/Briefing/north-star.md`, and `Machine/Personalization/daily-spark-prompt.md`.

Write a short Daily Spark inside the `## Daily Spark` relay callout.

It may include a quote, prompt, question, dare, small experiment, first line, or thought experiment. Use 2-3 openings total. Each should open a different door.

Use the configurable lenses as inspiration: Great Dreamer, Great Thinker, Great Contrarian, Great Ghost, Great Stranger.

Good output makes the user want to write. It should feel alive, generous, specific enough to grip, and loose enough to wander.

Output only: `Daily Spark written.`
```

### `.claude/commands/inbox.md`

```markdown
---
description: Process raw intake from the inbox.
---

# /inbox

Read files in `Human/01 - Inbox/`.

Classify each item: task, project, client, research, idea, writing, reference, trash candidate, or needs human read.

Route suggestions:

- tasks -> `Human/05 - Work/TaskNotes/Tasks/`
- projects -> `Human/05 - Work/Projects/`
- clients -> `Human/05 - Work/Clients/`
- research -> `Human/06 - Research/`
- ideas -> `Human/06 - Research/Ideas/`
- writing -> `Human/04 - Writing/`

Report first. Ask before moving, deleting, or rewriting source files.

Return a short processing table and the one next cleanup move.
```

### `.claude/commands/today.md`

```markdown
---
description: Build today's work map.
---

# /today

Read today's daily note, `Machine/Briefing/top-of-mind.md`, `Machine/Briefing/north-star.md`, active projects, open tasks, and pipeline items.

Write `Machine/Plans/YYYY-MM-DD.md`:

# Today - YYYY-MM-DD

## Signal

[What today seems to be about.]

## The One Thing

[The most useful forward move.]

## Work Map

- [ ] [task]
- [ ] [task]
- [ ] [task]

## On Deck

[Max 5 things not for today.]

Append the One Thing and Work Map to today's daily note under `## Plan`.

Output only: `Today built.`
```

### `.claude/commands/needle.md`

```markdown
---
description: Choose the one next move.
---

# /needle

Read today's plan, top-of-mind, active projects, and open tasks.

Return one move: what to do, why it matters, the smallest first action, and what to ignore until it is done.

If there are too many plausible moves, choose the one that unlocks the most downstream clarity.
```

### `.claude/commands/close.md`

```markdown
---
description: End-of-day close and machine maintenance.
---

# /close

Read today's daily note, today's plan, and `Machine/Briefing/top-of-mind.md`.

Ask one low-friction close question if the user has not already provided a debrief:

What happened today, and what should tomorrow not forget?

Append to today's daily note under `## Close`:

> [!relay] Close - HH:MM
>
> **What today was about:** ...
>
> **What changed:** ...
>
> **Tomorrow's signal:** ...
>
> **Loose ends:** ...

Then update `Machine/Plans/YYYY-MM-DD.md` with a short close note, suggest briefing updates only if something durable changed, and identify tasks or files to create. Ask before creating them.

Output:

Day closed.
[One line: tomorrow's signal]
```

### `.claude/commands/content.md`

```markdown
---
description: Draft practical content from real context.
---

# /content

Use for posts, captions, newsletters, short updates, client-facing copy, or business content.

Read `Machine/Personalization/relay-style.md`, `Machine/Briefing/top-of-mind.md`, relevant notes in `Human/05 - Work/Social/`, and relevant project or client context.

Ask what channel and purpose if missing. Draft one useful version. Keep the user's voice and context. Do not turn it into generic marketing copy.
```

### `.claude/commands/tasks.md`

```markdown
---
description: Review and clean the active task queue.
---

# /tasks

Read tasks in `Human/05 - Work/TaskNotes/Tasks/` and active project files.

Return due or urgent, stale, blocked, probably not real, and today's top three.

Ask before deleting or rewriting task files. If the task list is bloated, recommend what to park or cut.
```

### `.claude/commands/project.md`

```markdown
---
description: Move one project forward.
---

# /project

If no project is named, list active projects in `Human/05 - Work/Projects/` and ask which one.

For the selected project, read project notes, related tasks, related client or pipeline notes, and today's plan if relevant.

Return current state, blocker, next action, decision needed, and what to update. Make changes only with approval.
```

### `.claude/commands/pipeline.md`

```markdown
---
description: Review active leads and opportunities.
---

# /pipeline

Read `Human/05 - Work/Pipeline/`, related client notes, outreach notes, and open tasks.

Return hot opportunities, stale opportunities, waiting-on-someone items, follow-up candidates, and one pipeline move for today.

Do not invent lead data. If the pipeline is empty or unstructured, say so and suggest the smallest useful structure.
```

### `.claude/commands/outreach.md`

```markdown
---
description: Draft or review outreach.
---

# /outreach

Read `Human/05 - Work/Outreach/`, relevant pipeline notes, relevant client or project notes, and `Machine/Personalization/relay-style.md`.

Use for cold outreach, warm outreach, follow-ups, or relationship repair.

Draft plainly. Specific beats clever. The goal is a real human reply, not a performance. Ask before sending anything.
```

### `.claude/commands/money.md`

```markdown
---
description: Revenue pulse and money follow-up review.
---

# /money

Read `Human/05 - Work/Finance/`, `Human/05 - Work/Pipeline/`, active projects, and money-related tasks.

Return expected money, overdue or waiting money, invoice/payment follow-ups, pricing or scope issues, and one money move.

Keep it calm and factual.
```

### `.claude/commands/session.md`

```markdown
---
description: Save a meaningful conversation or decision.
---

# /session

Use when a conversation contains decisions, context, working agreements, or useful thinking that should not disappear.

Write a note in `Machine/Sessions/YYYY-MM-DD-[slug].md`.

Include summary, decisions, open questions, next actions, and files or systems affected.

If the session changes durable context, suggest updates to `Machine/Briefing/`.
```

### `.claude/commands/satisfice.md`

```markdown
---
description: Simplify bloated plans, systems, and decisions.
---

# /satisfice

Use when a plan, system, folder structure, command set, task list, or decision is getting too large.

Return:

## This Exists To

[One sentence.]

## Good Enough

[The threshold.]

## Keep

- [max 3]

## Cut

- [max 3]

## Park

- [max 3]

## Next Small Version

[The smaller version to run for the next 7 days.]

Do not solve complexity by adding another layer.
```

Do not install old default commands:

```text
closeday.md
new.md
weekly.md
decode.md
psycho.md
dreaming.md
ghost.md
stranger.md
```

---

## Step 5 - Completion Message

After building, output:

```text
The Dispatch is built.

Core loop:
Capture -> Process -> Plan -> Work -> Close -> Improve

Start tomorrow:
1. Run /daily-spark.
2. Write into the daily note.
3. Run /today.
4. Use /needle if the day needs focus.
5. Put loose material into Human/01 - Inbox/.
6. Run /close at the end of the day.

Core commands installed:
/start
/interview
/daily-spark
/inbox
/today
/needle
/close
/content
/tasks
/project
/pipeline
/outreach
/money
/session
/satisfice
```
