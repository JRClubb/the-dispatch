---
description: Decode a hot dispatch right after writing it. Surfaces what's alive, what to file, what to act on, what you're not seeing. Run when something has heat — don't wait for /closeday.
---

**Command: /decode**

Read today's dispatch and decode it. Surface what's alive. File what belongs somewhere. Generate tasks. Name what the user is not seeing. Run right after writing — when something has heat and shouldn't wait until evening.

Usage: `/decode` (reads today's dispatch) or `/decode [paste text]` (decodes pasted material).

---

## Step 1 — Read

1. Today's dispatch — `Log/Daily/YYYY-MM-DD.md` — full text, primary source
2. `Relay/briefing/top-of-mind.md`
3. `Relay/briefing/north-star.md`

If text is pasted, use that as primary source instead.

---

## Step 2 — Triage into five buckets

Quote actual lines. Don't paraphrase.

### SURFACE — What's alive right now

Realizations, breakthroughs, live questions, things half-said or being circled without being named. These disappear if not caught.

For each:
- Quote the line
- One sentence on what it's pointing at underneath
- Flag: **→ Go deeper?** or **→ Back burner?**

### FILE — Things that belong somewhere

Captures, seeds, fragments, observations worth keeping. For each: quote, proposed destination, one sentence on why.

**Routing:**

| Type | Destination |
|------|-------------|
| Observation, pattern, question, reaction | `Notes/Mind/` |
| Essay seed, creative fragment | `Notes/Mind/` |
| Body or health insight | `Notes/Body/` |
| Relationship insight | `Notes/People/` |
| Project or business signal | `Notes/Work/` |
| Briefing update (direction shift, priority change) | `Relay/briefing/` — ask before writing |

Nothing gets written without approval.

### ACT — Things that need to become actions

Anything in the dispatch that implies a next step — explicit or buried. For each:
- Quote or name the implied action
- Action type: **Task / Reminder / Decision / Outreach**
- Urgency: **Today / This week / Eventually**

Flag if the same action has appeared before without becoming an action. That is avoidance.

### WHAT YOU'RE NOT SEEING

The relay's independent read. Not what the dispatch says — what it's working around.

Surface up to three:
- **The contradiction** — conflicts with a stated priority or recent dispatch
- **The unnamed pattern** — appearing repeatedly without a label
- **The buried urgency** — mentioned lightly, actually more important than it sounds
- **The absent frequency** — a quadrant of life that didn't appear and probably should have
- **The avoided thing** — the subject that got the most words but the least clarity

One sentence per observation. No softening.

### QUESTIONS

The live edge of what's in the dispatch. Not for answering now unless the user wants to.

---

## Step 3 — Present

Output all five buckets. Lead with SURFACE if anything is urgent. Otherwise lead with WHAT YOU'RE NOT SEEING.

After output, ask once:

> "Which of these do you want to act on? I can file, create tasks, go deeper, or update briefing files."

**Before waiting — automatically save a decode summary to `Relay/briefing/last-decode.md`.** Overwrite if it exists. No approval needed.

