---
description: End-of-day processing. Reads the dispatch, surfaces patterns, writes the End of Dispatch debrief, seeds tomorrow's Morning Signal.
---

**Command: /closeday**

Process the day's dispatch. Find the patterns. Close the loops. The debrief seeds tomorrow's Morning Signal — what you write here is what the morning reads first.

---

## Read

1. Today's dispatch `Log/Daily/YYYY-MM-DD.md` — primary source.
2. Today's field orders `Relay/plans/YYYY-MM-DD.md` — what was intended.
3. `Relay/briefing/top-of-mind.md`
4. Last 3 dispatches — for pattern detection.

---

## Pass 1 — What actually happened

Read the dispatch. It is the real data — not the plan, not the intention. For each frequency (People / Body / Mind / Work): one paragraph of honest accounting. What was written or implied?

Then surface:
- **What shifted** — a reframe, a decision, something named for the first time
- **What's unresolved** — tensions named but not settled
- **Did the Morning Signal land?** — Did the writing move toward the questions, or somewhere different? Both are useful data.

---

## Pass 2 — Patterns and contradictions

- **Recurring themes:** Same topic in 3+ of last 5 dispatches? Flag it.
- **Contradictions:** Something today contradicts a recent dispatch? Name both.
- **Plan gap:** Field orders vs. what actually happened. One line. No judgment.

---

## Pass 3 — Extract and file

Pull anything that should live somewhere other than the daily dispatch:

| Item | Type | Suggested location |
|------|------|--------------------|
| Action implied ("I should X") | Task | Checkbox in relevant project file |
| Original thinking worth keeping | Note | Relevant frequency folder |
| Quote or observation with resonance | Capture | Relevant frequency folder |
| Person mentioned needing a record | Contact | `Notes/People/` |

Present as a table. Ask before creating files. Never auto-create from the dispatch.

---

## Pass 4 — End of Dispatch debrief

Append to today's dispatch under `## End of Dispatch`, inside a relay callout. The `> [!relay]` wrapper is mandatory.

