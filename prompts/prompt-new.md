---
description: Brain dump → file. Captures a task, idea, project, or contact from natural language.
---

**Command: /new [anything]**

Capture any thought. Classify it. Create the right file. Link what's relevant.

Examples:
- `/new follow up with Sarah about the contract by Friday`
- `/new idea — what if I ran a workshop version of this`
- `/new Alex Chen from the conference — systems thinker`

---

## Classification

| Type | Signal | Location |
|------|--------|----------|
| **Task** | Action verb + endpoint | Checkbox in relevant project file, or today's dispatch |
| **Project** | Multi-step work toward an outcome | `Notes/Work/[Project]/index.md` |
| **Idea** | Observation, possibility, no action yet | Relevant frequency folder |
| **Contact** | New person | `Notes/People/[Name].md` |

When classifying — which frequency does it primarily serve?

---

## Contact check

Before creating anything that mentions a person:
1. Search the vault for a matching file
2. If found — link it: `person: [[Name]]`
3. If not — create a minimal contact note first, then link

---

## File formats

**Project** (`Notes/Work/[Name]/index.md`):
```yaml
---
type: project
status: active
frequency: Work
created: YYYY-MM-DD
---

## Overview
[Brief description]

## Next action
- [ ] [First move]
