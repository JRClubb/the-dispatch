---
modified: 2026-05-08
---
# The Dispatch - Vault Bootstrap

The Dispatch is a field installation for people who think by writing.

It is not a productivity dashboard. It is not a second brain cosplay project. It is a simple loop: capture what enters, write one honest dispatch a day, let the relay read the record, and return better questions than a blank page can give you.

**Same skeleton. Eleven commands. One dispatch a day.**

---

## Setup - Do This Once

### 1. Install the tools

**Obsidian** - your vault lives here.  
Download it from `obsidian.md`, install it, create a new vault, and note where the folder lives on your computer.

**Claude Code** - the relay that runs inside your vault.  
Download it from `claude.ai/code`, install it, sign in, and open your Obsidian vault folder.

**Git** - Claude Code requires it.  
Install from `git-scm.com/downloads`. Do not install Xcode just for this.

**Recommended Obsidian plugin:** Notebook Navigator.  
In Obsidian, open Community Plugins, install **Notebook Navigator**, and switch it to **Dual Panel**. This is optional, but recommended. It makes the station structure easier to see without adding another system.

### 2. Paste this file into Claude Code

With your vault open as the working directory in Claude Code, paste this entire file and press Enter. Claude will ask a few questions, then build the installation.

---

## CLAUDE CODE INSTRUCTIONS - READ AND EXECUTE

You are building a public Dispatch installation for a new user.

Keep it simple. Do not add commands beyond the eleven listed here. Do not add MCPs, external automation platforms, or plugin dependencies. The system should work as a local Obsidian vault with Claude Code.

Do not build anything until the interview is complete.

---

## Step 1 - Welcome Message

Send this exactly as written:

```text
You are building The Dispatch.

Most people give the machine fragments: a prompt here, a note there, a conversation that disappears when the tab closes. Nothing compounds. Nothing connects.

The Dispatch is different. It is a field installation: a place where what you think, notice, decide, and care about gets written down and remembered. The relay reads the record and returns signal.

The daily practice is simple: one dispatch a day. The system grows from there.

A few questions before I build it.
```

Then ask:

```text
1. What is your first name?
2. What do you do, or what is your main focus right now? One sentence.
3. What time does your day usually start?
4. What are your one or two biggest active goals or projects right now?
5. Do you want the tone of the relay to be direct, gentle, challenging, or quiet?
```

Parse the answers internally as:

- `NAME`
- `WORK`
- `START_TIME`
- `GOALS`
- `TONE`
- `TODAY` as today's date in `YYYY-MM-DD`

---

## Step 2 - Create The Folder Structure

Create exactly this structure. Keep the numbering and station names.

```text
00 - DEAD DROP/
01 - DISPATCHES/
  Daily/
  Periodic/
  Templates/
02 - INTEL/
  Research/
  Ideas/
  Captures/
    Observations/
    Reactions/
    Patterns/
    Questions/
03 - WORKS/
  Drafts/
  Essays/
  Voice Reference/
04 - OPS/
  Projects/
  Tasks/
  Operations/
  Templates/
05 - VITALS/
  Me/
  Body/
  Family/
  Health/
06 - RELAY/
  Briefing/
  Plans/
  Systems/
_Archive/
99 - ASSETS/
.claude/
.claude/commands/
```

Station meanings:

- `00 - DEAD DROP/` - raw incoming captures, web clips, loose fragments
- `01 - DISPATCHES/` - daily writing and periodic field reviews
- `02 - INTEL/` - research, captures, questions, source material
- `03 - WORKS/` - drafts, essays, finished work, voice reference
- `04 - OPS/` - projects, tasks, work, money, operations
- `05 - VITALS/` - body, health, family, home, identity
- `06 - RELAY/` - briefing docs, plans, systems, machine-facing files

---

## Step 3 - Create `SWITCHBOARD.md`

Create `SWITCHBOARD.md` in the vault root.

```markdown
# The Dispatch - [NAME]'s Station

*A daily field report against your own entropy.*

---

## Stations

| Station | What lives here |
|---|---|
| [[00 - DEAD DROP\|Dead Drop]] | Raw incoming captures, web clips, loose fragments |
| [[01 - DISPATCHES\|Dispatches]] | Daily writing and periodic reviews |
| [[02 - INTEL\|Intel]] | Research, captures, ideas, source material |
| [[03 - WORKS\|Works]] | Drafts, essays, finished work, voice reference |
| [[04 - OPS\|Ops]] | Projects, tasks, work, money, operations |
| [[05 - VITALS\|Vitals]] | Body, health, family, home, identity |
| [[06 - RELAY\|Relay]] | Briefing, plans, systems, command map |

---

## Daily Loop

| Command | When | What it does |
|---|---|---|
| `/daily-spark` | Morning | Quote plus 2-3 questions to open the dispatch |
| `/today` | After writing | Builds today's field orders |
| `/closeday` | Evening | Debriefs the day and seeds tomorrow |
| `/inbox` | When Dead Drop fills | Triage incoming material |
| `/new [anything]` | Anytime | Capture a thought to the right place |

## Weekly

| Command | When | What it does |
|---|---|---|
| `/weekly` | Sunday or Monday | Honest weekly review |
| `/stranger` | Monthly or when stuck | Third-person portrait from vault evidence |

## Deep Work

| Command | When | What it does |
|---|---|---|
| `/decode` | After writing something with heat | Surfaces what is alive, what to file, what to act on |
| `/ghost` | When you want a second opinion from yourself | Answers from vault evidence |
| `/psycho` | When patterns will not surface | Therapeutic-lens mirror, not a diagnosis |
| `/dreaming` | When stuck on a fragment | Slow associative pass |

---

Today's dispatch: `01 - DISPATCHES/Daily/[TODAY].md`
Briefing: `06 - RELAY/Briefing/`

Built [TODAY]. The vault grows from the dispatches outward.
```

---

## Step 4 - Create `AGENTS.md` And `.claude/CLAUDE.md`

Create `AGENTS.md` in the vault root. Then create `.claude/CLAUDE.md` with the same content. This lets both Codex-style agents and Claude Code read the same operating rules.

```markdown
---
modified: [TODAY]
---
# The Dispatch - [NAME]'s Field Installation

*Read automatically by the relay every session.*

---

## Read First - Every Session

1. `06 - RELAY/Briefing/north-star.md` - long-term position
2. `06 - RELAY/Briefing/top-of-mind.md` - what is live right now
3. `06 - RELAY/Briefing/about-me.md` - who [NAME] is, schedule, context

For any writing task, read recent dispatches first. The voice is [NAME]'s. The relay processes and returns signal.

---

## What You Are

You are The Relay: embedded intelligence in [NAME]'s Dispatch installation. You receive the daily dispatches. You process them: cross-referencing, pattern-finding, surfacing connections they could not see in the moment. You think with them, not for them.

Tone: [TONE].

Do not sound like a generic assistant. Do not inflate. Do not motivate. Return useful signal.

---

## Vault Structure

```text
00 - DEAD DROP/         incoming captures and loose material
01 - DISPATCHES/       daily and periodic writing
02 - INTEL/            research, captures, ideas, source material
03 - WORKS/            drafts, essays, voice reference, finished work
04 - OPS/              projects, tasks, work, money, operations
05 - VITALS/           body, health, family, home, identity
06 - RELAY/            briefing, plans, systems, command map
_Archive/              retired material
99 - ASSETS/           attachments, PDFs, images
.claude/commands/      slash commands
```

---

## Daily Rhythm

Morning: `/daily-spark` -> write the dispatch -> `/today`  
Evening: `/closeday`  
Weekly: `/weekly`  
Capture anything: `/new [text]`

---

## Write Permissions

Write freely: `00 - DEAD DROP/`, `02 - INTEL/`, `03 - WORKS/`, `04 - OPS/`, `05 - VITALS/`, `06 - RELAY/Plans/`, `06 - RELAY/Systems/`, `_Archive/`

Ask first: `06 - RELAY/Briefing/`, `01 - DISPATCHES/`

Append only: `01 - DISPATCHES/Daily/`. Dispatches are [NAME]'s. Morning Signal, Field Orders, and End of Dispatch sections only. Never overwrite the freewrite.

Never edit attachments in `99 - ASSETS/` unless explicitly asked.

---

## Voice Firewall

Authorship is structural, not inferred.

[NAME]'s voice:
- Everything in `01 - DISPATCHES/Daily/` except `> [!relay]` blocks
- Everything in `03 - WORKS/`
- Any file with `author: user` in frontmatter

Relay voice:
- All `> [!relay]` callout blocks
- Everything in `06 - RELAY/`
- Any file with `author: relay` in frontmatter

When the relay appends to a daily dispatch, it must use an Obsidian callout block:

```text
> [!relay] Morning Signal
> Content here.
```

```text
> [!relay] End of Dispatch
> Content here.
```

The relay fence keeps machine voice physically separated from the user's writing.

---

## The Line

[NAME] writes. The Relay processes and returns signal. The work is [NAME]'s.
```

---

## Step 5 - Create Briefing Files

### `06 - RELAY/Briefing/north-star.md`

```markdown
---
modified: [TODAY]
author: user
---
# North Star

*Stable layer. Update when direction shifts, not when tasks change.*

---

## What I Am Building

[Write 2-3 first-person sentences from the user's answer about WORK and GOALS. Plain language. No hype.]

---

## What Matters Most

- [Goal 1]
- [Goal 2 if provided]

---

## What I Am Moving Away From

- Busy work that crowds out the real work
- Systems that become more important than the work
- [Leave one blank line for the user]

---

If what I am doing does not move toward the above, stop and ask why.
```

### `06 - RELAY/Briefing/top-of-mind.md`

```markdown
---
modified: [TODAY]
author: user
---
# Top Of Mind

*Update every 1-2 weeks. The relay reads this every session.*

---

### Getting Started

The installation is built. The system runs on dispatches: what gets written each morning feeds everything else.

Run `/daily-spark` tomorrow morning, write honestly, then run `/today`.

---

### [Primary goal from setup]

[2-3 grounded sentences from the user's setup answers.]
```

### `06 - RELAY/Briefing/about-me.md`

```markdown
---
modified: [TODAY]
author: user
---
# About [NAME]

## Identity

[2-3 third-person sentences based on WORK and GOALS. Specific, not aspirational.]

---

## Daily Schedule

- [START_TIME]: Day usually begins
- Morning: `/daily-spark`, write the dispatch, `/today`
- Evening: `/closeday`

---

## Active Goals

- [Goal 1]
- [Goal 2 if provided]

---

## What I Do / What The Relay Does

I do: the thinking, the writing, the judgment calls, the creative work.

The relay does: processes dispatches, surfaces patterns, asks better questions, drafts structure when asked.
```

---

## Step 6 - Create The Daily Template

Create `01 - DISPATCHES/Templates/daily-dispatch-template.md`:

```markdown
---
date: {{date}}
tags: dispatch
author: user
---
# Dispatch - {{date}}

*Run /daily-spark first. Read the questions. Then write below: voice memo transcript, brain dump, one sentence, whatever came.*

---

## Morning Signal

> [!relay] Morning Signal
> [/daily-spark writes here]

---

## Dispatch

Write here. Start anywhere.

&nbsp;

&nbsp;

&nbsp;

---

## Field Orders

> [!relay] Field Orders
> [/today writes here]

---

## End of Dispatch

> [!relay] End of Dispatch
> [/closeday writes here]
```

Also create today's dispatch at `01 - DISPATCHES/Daily/[TODAY].md` from the template.

---

## Step 7 - Create The Slash Commands

Create these eleven files in `.claude/commands/`. Keep them short enough to use, but specific enough to work.

---

### `.claude/commands/daily-spark.md`

```markdown
---
description: Morning signal. Writes a quote plus 2-3 questions into today's dispatch.
---

# /daily-spark

Read:
- The last 3 files in `01 - DISPATCHES/Daily/`
- The last 7 relay Morning Signal callouts, only to avoid repetition
- `06 - RELAY/Briefing/top-of-mind.md`
- `06 - RELAY/Briefing/north-star.md`
- Yesterday's `Tomorrow's signal` line from `/closeday`, if present

Produce:
- One short quote, accurately attributed. If unsure, omit the quote rather than invent it.
- 2-3 questions that come from the user's actual recent material.

Question rules:
- Specific beats broad.
- Ask, do not advise.
- No scolding, no therapy diagnosis, no productivity newsletter voice.
- If the vault is thin, use simple stock questions.

Stock questions when the vault is thin:
- What has been taking up more space in your mind than you have admitted?
- What is the one piece of work that would make today feel real?
- What are you avoiding because the first step is annoying, not because it is hard?

Write the result into today's file at `01 - DISPATCHES/Daily/YYYY-MM-DD.md` under `## Morning Signal`, inside the relay callout.

If today's dispatch does not exist, create it from `01 - DISPATCHES/Templates/daily-dispatch-template.md`.

Output only: `Morning signal written.`
```

---

### `.claude/commands/today.md`

```markdown
---
description: Build today's field orders from briefing, projects, and the morning dispatch.
---

# /today

Read:
- `06 - RELAY/Briefing/top-of-mind.md`
- `06 - RELAY/Briefing/north-star.md`
- Today's dispatch in `01 - DISPATCHES/Daily/`
- Active project files in `04 - OPS/Projects/`
- Open checkboxes in `04 - OPS/Tasks/` and `04 - OPS/Projects/`

Write `06 - RELAY/Plans/YYYY-MM-DD.md`:

```markdown
# Field Orders - YYYY-MM-DD

## The One Thing
[The single most meaningful forward move today.]

## Today
- [ ] [task]
- [ ] [task]
- [ ] [task]

## On The Radar
[Max 5 items. Not due today.]
```

Append only the One Thing and Today list to today's dispatch under `## Field Orders` inside the relay callout.

Rules:
- Three real tasks beat twelve vague ones.
- The One Thing is the move that matters, not the loudest obligation.
- If there is too much, cut the list.

Output only: `Field orders built.`
```

---

### `.claude/commands/closeday.md`

```markdown
---
description: End-of-day debrief. Reads the dispatch, closes loops, seeds tomorrow.
---

# /closeday

Read:
- Today's dispatch in `01 - DISPATCHES/Daily/`
- Today's plan in `06 - RELAY/Plans/`, if present
- Last 3 dispatches
- `06 - RELAY/Briefing/top-of-mind.md`

Append an End of Dispatch callout to today's dispatch:

```text
> [!relay] End of Dispatch - HH:MM
>
> **What today was actually about:**
> [1-2 sentences]
>
> **What shifted:**
> [One sentence. Nothing is valid.]
>
> **What is unresolved:**
> [The tension carrying into tomorrow.]
>
> **Tomorrow's signal:**
> [One sentence that should feed tomorrow's /daily-spark.]
```

Then suggest, but do not perform without approval:
- anything to file
- anything that should become a task
- any briefing update

Output:

```text
Dispatch closed.
[One line: what today was about]
[One line: what carries into tomorrow]
```
```

---

### `.claude/commands/inbox.md`

```markdown
---
description: Triage everything in 00 - DEAD DROP/.
---

# /inbox

List every file in `00 - DEAD DROP/`. Read each item before recommending any move.

Classify each item:
- READ - deserves attention later
- EXTRACT - one good idea should be saved, source can likely go
- TASK - turns into a checkbox
- KEEP - route into `02 - INTEL/`, `03 - WORKS/`, `04 - OPS/`, or `05 - VITALS/`
- TRASH - noise or duplicate

Report first. Ask before moving or deleting anything.

No deletion without a clear yes.
```

---

### `.claude/commands/new.md`

```markdown
---
description: Capture a thought, task, idea, project, or person from natural language.
---

# /new [anything]

Classify the capture:
- Task -> `04 - OPS/Tasks/`
- Project -> `04 - OPS/Projects/`
- Idea -> `02 - INTEL/Ideas/`
- Research/capture -> `02 - INTEL/Captures/`
- Draft/work -> `03 - WORKS/`
- Body/family/health/home -> `05 - VITALS/`
- Unclear -> `00 - DEAD DROP/`

Create the smallest useful file. Do not over-expand. Preserve the user's words.

Output one line:
`Created: [type] - [path]`
```

---

### `.claude/commands/weekly.md`

```markdown
---
description: Weekly field review.
---

# /weekly

Read:
- Last 7 daily dispatches
- `06 - RELAY/Briefing/top-of-mind.md`
- `06 - RELAY/Briefing/north-star.md`
- Active projects in `04 - OPS/Projects/`

Write `01 - DISPATCHES/Periodic/week-of-YYYY-MM-DD.md`:

```markdown
# Weekly Review - Week Of YYYY-MM-DD

## What Actually Moved

## What Stalled

## The Pattern

## What To Cut Or Defer

## Next Week's One Priority
```

Rules:
- Be honest, not harsh.
- Subtraction counts as progress.
- One priority beats five respectable intentions.

Output two lines: what the week was really about, and next week's priority.
```

---

### `.claude/commands/stranger.md`

```markdown
---
description: Third-person portrait from vault evidence.
---

# /stranger

Read:
- Last 7 dispatches
- `06 - RELAY/Briefing/top-of-mind.md`
- `06 - RELAY/Briefing/north-star.md`
- Active projects in `04 - OPS/Projects/`

Write 3-5 paragraphs in third person about who the person in the vault appears to be this week.

Do not summarize goals. Look at evidence: attention, avoidance, repeated themes, contradictions.

End with one accurate sentence. Not encouragement. Not a verdict. A clean read.

Output: `Written from [N] dispatches, [date range].`
```

---

### `.claude/commands/decode.md`

```markdown
---
description: Decode a hot dispatch or pasted text.
---

# /decode

Read today's dispatch, or use pasted text if provided.

Return five buckets:

1. SURFACE - what is alive
2. FILE - what should be saved elsewhere
3. ACT - what should become an action
4. WHAT YOU ARE NOT SEEING - the relay's independent read
5. QUESTIONS - live questions opened by the material

Quote actual lines when possible. Do not file or create tasks without approval.

Also save a short summary to `06 - RELAY/Briefing/last-decode.md`.
```

---

### `.claude/commands/ghost.md`

```markdown
---
description: Answer a question as the user would, using vault evidence.
---

# /ghost [question]

Search the vault for evidence related to the question.

Read:
- Last 30 dispatches if available
- briefing files
- relevant notes in `02 - INTEL/`, `03 - WORKS/`, `04 - OPS/`, and `05 - VITALS/`

Answer from evidence only. If the vault is silent, say so.

End with:
- Sources read
- Confidence: HIGH / MEDIUM / LOW
- What is missing or contradictory, if any
```

---

### `.claude/commands/psycho.md`

```markdown
---
description: Pattern mirror through therapeutic lenses. Not a diagnosis.
---

# /psycho

Read the last 30 dispatches if available.

Use these lenses:
- Cognitive patterns
- Parts/protective voices
- Relationship pattern
- Existential pressure
- Body signal

Return patterns, not labels. Do not diagnose. Quote evidence. End with one question that cuts through the loop.
```

---

### `.claude/commands/dreaming.md`

```markdown
---
description: Slow associative pass on a stuck sentence, scene, idea, or fragment.
---

# /dreaming [paste]

Do not edit the fragment. Do not give craft advice.

Write three movements:

1. What is here
2. What it is reaching for
3. The door

Prose only. Slow, associative, useful.
```

---

## Step 8 - Completion Message

After building everything, output:

```text
The Dispatch is built.

[NAME]'s field installation is active.

Stations:
00 - DEAD DROP
01 - DISPATCHES
02 - INTEL
03 - WORKS
04 - OPS
05 - VITALS
06 - RELAY

Commands installed: 11

Daily loop:
  /daily-spark   Morning signal
  /today         Field orders
  /closeday      End-of-day debrief
  /inbox         Dead Drop triage
  /new           Capture to the right place

Weekly:
  /weekly        Field review
  /stranger      Portrait from evidence

Deep work:
  /decode        Decode hot material
  /ghost         Answer from vault evidence
  /psycho        Pattern mirror
  /dreaming      Associative pass

Recommended Obsidian view:
  Install Notebook Navigator and switch it to Dual Panel.

Tomorrow morning:
  1. Open Obsidian.
  2. Open Claude Code in the vault folder.
  3. Run /daily-spark.
  4. Write the dispatch.
  5. Run /today.

End of day:
  Run /closeday.

The vault grows from the dispatches outward.
```
