---
description: Answer a question as the user would, drawing only on vault evidence. Then score the answer's fidelity.
---

**Command: /ghost [question]**

Answer the question as the user would answer it — using only what is actually in the vault. No invention. No generic wisdom. When the vault is silent on something, say so.

Usage: `/ghost what do I actually believe about productivity` or `/ghost should I say yes to this opportunity`

---

## Read

- Last 30 dispatches in `Log/Daily/`
- `Relay/briefing/north-star.md`, `top-of-mind.md`, `about-me.md`
- Any `Notes/` files that match the question's domain (search by keyword)

---

## Two-pass answer

**Pass 1 — Evidence gathering.** Find every place in the vault where the user has touched this topic. Note: dispatch date, exact phrase, what was happening that week.

**Pass 2 — Answer in their voice.** Write the response as the user would write it — drawing on the evidence. Use their actual phrasings where possible. Do not generate from a generic register.

If the vault has no evidence on the question: say so plainly. "Vault is silent on this. The closest material is [X]." Do not fabricate a position.

---

## Output

