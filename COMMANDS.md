# Command Reference

The default command set is intentionally small enough to remember and complete enough to run a client-facing work system.

## Core Loop

| Command | Role | Primary Paths |
|---|---|---|
| `/start` | Orient and check setup. | `System/`, `Machine/Briefing/`, `Machine/Systems/` |
| `/interview` | Build personalization. | `Machine/Personalization/`, `Machine/Briefing/` |
| `/daily-spark` | Generate the daily note starter. | `Human/03 - Journal/Daily/`, `Machine/Personalization/`, `Machine/Briefing/` |
| `/inbox` | Process intake. | `Human/01 - Inbox/`, `Human/05 - Work/`, `Human/06 - Research/` |
| `/today` | Build today's work map. | `Machine/Plans/`, `Human/05 - Work/`, `Machine/Briefing/` |
| `/needle` | Pick the one next move. | `Machine/Plans/`, `Human/05 - Work/` |
| `/close` | End the day and maintain context. | `Human/03 - Journal/Daily/`, `Machine/Plans/`, `Machine/Briefing/` |

## Work Layer

| Command | Role | Primary Paths |
|---|---|---|
| `/content` | Draft practical content from real context. | `Human/05 - Work/Social/`, `Machine/Personalization/` |
| `/tasks` | Clean the task queue. | `Human/05 - Work/TaskNotes/Tasks/` |
| `/project` | Move one project forward. | `Human/05 - Work/Projects/` |
| `/pipeline` | Review leads and active opportunities. | `Human/05 - Work/Pipeline/` |
| `/outreach` | Draft or review outreach. | `Human/05 - Work/Outreach/`, `Human/05 - Work/Pipeline/` |
| `/money` | Review revenue, invoices, and payment follow-ups. | `Human/05 - Work/Finance/`, `Human/05 - Work/Pipeline/` |

## Maintenance

| Command | Role | Primary Paths |
|---|---|---|
| `/session` | Save a meaningful conversation or decision. | `Machine/Sessions/`, `Machine/Briefing/sessions/` |
| `/satisfice` | Simplify a bloated plan, command, folder structure, or decision. | Current context |

## Optional Modules

These can be added when the client actually needs them.

| Command | Use When |
|---|---|
| `/client-prep` | The client has calls, shoots, sessions, delivery meetings, or account reviews. |
| `/after-session` | The client needs a post-session closeout workflow. |
| `/7plan` | Weekly planning will actually be used. |
| `/lint` | The vault has enough research or documentation to need health checks. |
| `/book` | The client works from books, PDFs, transcripts, or long source documents. |
| `/harvest` | The client needs research-to-work synthesis. |
| `/great-thinker` | The client wants thinking mode without artifact pressure. |
| `/great-dreamer` | The client wants associative creative exploration. |
| `/great-contrarian` | The client wants strategy challenge without nagging. |
| `/great-ghost` | The client wants answers grounded in their own archive. |
| `/great-stranger` | The client wants an outside read of what the vault reveals. |

## Retired From Default Install

The default bootstrap does not ship old Dispatch commands such as `/closeday`, `/new`, `/weekly`, `/decode`, `/psycho`, `/dreaming`, `/ghost`, or `/stranger`.

Some of those ideas survive as generic lenses or optional modules. They do not belong in the default menu.
