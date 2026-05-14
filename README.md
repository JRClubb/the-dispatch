# The Dispatch

*An Obsidian + Claude Code bootstrap for people who want their work, notes, decisions, and daily thinking to compound.*

---

The Dispatch is a local operating system for a small body of work.

It is built around a simple loop:

```text
Capture -> Process -> Plan -> Work -> Close -> Improve
```

The human writes, decides, and does the work. The relay reads the record, keeps context alive, asks better questions, and helps turn loose material into useful next moves.

The point is not to automate the life out of the system. The point is to preserve signal: what came in, what matters now, what needs a decision, what deserves to become work, and what can be released.

---

## What You Need

- [Obsidian](https://obsidian.md)
- [Claude Code](https://claude.ai/code)
- Git, if Claude Code asks for it

Optional:

- Notebook Navigator for a cleaner Obsidian sidebar

No paid templates, no required MCPs, no dashboard maze.

---

## Install

1. Create a new Obsidian vault.
2. Open Claude Code in that vault folder.
3. Copy the contents of [BOOTSTRAP.md](BOOTSTRAP.md), paste into Claude Code, and press Enter.
4. Answer the setup questions.

Claude Code will build the folders, briefing files, daily template, and command prompts.

---

## Folder Structure

```text
Human/
  01 - Inbox/          raw intake, clips, notes, transcripts
  03 - Journal/        daily notes, reviews, human-authored records
  04 - Writing/        drafts, outputs, voice examples, finished work
  05 - Work/           clients, projects, tasks, pipeline, money, social
  06 - Research/       captures, ideas, sources, synthesis
  07 - Life/           personal context when needed
Machine/
  Briefing/            durable context the relay reads
  Personalization/     tone, preferences, daily spark settings
  Plans/               daily plans and work maps
  Sessions/            saved conversations and decisions
  Systems/             operating docs and maintenance notes
System/
  Archive/             retired material
99 - ASSETS/           attachments and media
.claude/
  commands/            Claude Code slash commands
```

The default work folder is:

```text
Human/05 - Work/
```

---

## Core Commands

The default install ships the commands that support the operating loop.

| Command | When | What it does |
|---|---|---|
| `/start` | First run or reset | Checks the vault structure and orients the relay. |
| `/interview` | Setup or refresh | Builds the personalization layer. |
| `/daily-spark` | Morning | Creates the daily note starter: quote, prompts, questions, experiments, or lenses. |
| `/inbox` | When intake piles up | Processes raw material from `Human/01 - Inbox/`. |
| `/today` | Start of work block | Builds the daily work map. |
| `/needle` | When the day needs focus | Chooses the one next move that matters most. |
| `/close` | End of day | Captures a short debrief, extracts tomorrow's signal, and cleans up the machine layer. |
| `/content` | When publishing or communicating | Drafts practical content from real context. |
| `/tasks` | Task review | Cleans the active task queue. |
| `/project` | Project work | Moves one project forward. |
| `/pipeline` | Business review | Reviews active leads and opportunities. |
| `/outreach` | Business development | Drafts or reviews outreach. |
| `/money` | Revenue review | Checks invoices, follow-ups, and revenue signal. |
| `/session` | After a useful conversation | Saves decisions, context, and next actions. |
| `/satisfice` | When things get bloated | Simplifies the plan, system, or decision. |

---

## Daily Practice

Morning:

1. Run `/daily-spark`.
2. Write into the daily note.
3. Run `/today`.
4. Run `/needle` if the day feels noisy.

During the day:

1. Put loose material into `Human/01 - Inbox/`.
2. Use `/inbox` to process it.
3. Use `/project`, `/tasks`, `/pipeline`, `/outreach`, `/money`, or `/content` when the work calls for it.

Evening:

1. Run `/close`.

That is the loop. The system gets better because the record gets better.

---

## Daily Spark

`/daily-spark` is a core feature, not decoration.

It creates the daily note and gives the user a reason to write into it. It should not feel like a taskmaster. It should feel like an opening.

The generic install uses configurable lenses:

| Lens | Job |
|---|---|
| Great Dreamer | Opens image, memory, intuition, strangeness, possibility. |
| Great Thinker | Finds the deeper question, frame, or live idea. |
| Great Contrarian | Challenges stale assumptions without nagging. |
| Great Ghost | Answers from the user's own archive, values, and prior words. |
| Great Stranger | Reflects what the vault says from the outside. |

Users can personalize these during `/interview`.

---

## What This Is Not

This is not a total productivity system.

It is not a replacement for judgment, writing, or actual work.

It is not meant to ship every possible command by default. Optional modules can be added later, but the first install should stay easy to understand:

```text
Capture -> Process -> Plan -> Work -> Close -> Improve
```

If a command does not support that loop, it does not belong in the default install.
