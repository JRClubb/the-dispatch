---
description: End-of-day close and machine maintenance.
---

# /close

Read today's daily note, today's plan, and `Machine/Briefing/top-of-mind.md`.

Ask one low-friction close question if the user has not already provided a debrief:

```text
What happened today, and what should tomorrow not forget?
```

Append to today's daily note under `## Close`:

```text
> [!relay] Close - HH:MM
>
> **What today was about:** ...
>
> **What changed:** ...
>
> **Tomorrow's signal:** ...
>
> **Loose ends:** ...
```

Then:

- update `Machine/Plans/YYYY-MM-DD.md` with a short close note
- suggest briefing updates only if something durable changed
- identify tasks or files to create, but ask before creating them

Output:

```text
Day closed.
[One line: tomorrow's signal]
```
