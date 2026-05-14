# Client Bootstrap V2

This is the next shape of The Dispatch bootstrap.

The old public version is a writing-first field installation. This version is a client operating loop: capture, process, plan, work, close, improve.

## Folder Structure

```text
Human/
  01 - Inbox/
  03 - Journal/
  04 - Writing/
  05 - Work/
  06 - Research/
  07 - Life/
Machine/
  Briefing/
  Personalization/
  Plans/
  Sessions/
  Systems/
System/
  Archive/
99 - ASSETS/
.claude/
  commands/
```

Default work slot:

```text
Human/05 - Work/
```

## Core Commands

Ship these first:

| Command | Job |
|---|---|
| `/start` | Orient the client and check setup. |
| `/interview` | Build the operating profile and personalization layer. |
| `/daily-spark` | Generate the daily note starter: quote, questions, prompts, experiments, or lenses. |
| `/inbox` | Process raw intake into tasks, captures, projects, or research candidates. |
| `/today` | Create the daily work map. |
| `/needle` | Choose the one next move from the day map. |
| `/close` | Combined end-of-day close and machine maintenance. |
| `/content` | One door for practical business content. |
| `/tasks` | Review and clean the task queue. |
| `/project` | Move one project forward. |
| `/pipeline` | Review active leads and opportunities. |
| `/outreach` | Draft or review outreach with business context. |
| `/money` | Revenue pulse and invoice/follow-up review. |
| `/session` | Save important conversations and decisions. |
| `/satisfice` | Simplify bloated plans, systems, and decisions. |

## Daily Spark

`/daily-spark` stays central. It is one of the product's signature moves: the system creates the daily note and gives the user a reason to write into it.

The generic version should not ship fixed artist references or private persona language. It should use configurable lenses:

| Lens | Job |
|---|---|
| Great Dreamer | Opens image, memory, intuition, strangeness, possibility. |
| Great Thinker | Finds the deeper question, the frame, the live idea. |
| Great Contrarian | Challenges the stale assumption without nagging. |
| Great Ghost | Answers from the client's own archive, values, and prior words. |
| Great Stranger | Reflects what the vault says from the outside, without flattery. |

The daily starter can include:

- a quote or line from the client's material
- questions
- prompts
- dares
- small experiments
- first lines
- thought experiments

Personalization belongs in:

```text
Machine/Personalization/daily-spark-prompt.md
```

## Close Command

Ship one command:

```text
/close
```

Clients should not have to understand the difference between a quick human close and a machine maintenance close.

`/close` should:

1. Ask one low-friction end-of-day question.
2. Append a short machine-marked debrief to the daily note.
3. Extract tomorrow's signal.
4. Update small briefing facts if clearly warranted.
5. Clean up today's machine plan.

## Optional Modules

Ship these only when the client needs them:

| Command | When to include |
|---|---|
| `/client-prep` | Client-service businesses with calls, shoots, sessions, or delivery meetings. |
| `/after-session` | Service delivery clients who need a post-session closeout. |
| `/7plan` | Clients who will actually use weekly planning. |
| `/lint` | Research-heavy or documentation-heavy vaults. |
| `/book` | Book/research-heavy clients. Assumes an uploaded file or pasted source text; no special book-manager app required. |
| `/harvest` | Research-to-work synthesis clients. |
| `/great-thinker` | Thinking-heavy clients. |
| `/great-dreamer` | Creative or vision-heavy clients. |
| `/great-contrarian` | Strategy and decision clients. |
| `/great-ghost` | Voice and values clients. |
| `/great-stranger` | Reflection and review clients. |

## Retire From Generic Bootstrap

Do not ship these in the generic client install:

```text
/closeday
/new
/weekly
/decode
/psycho
/dreaming
/ghost
/stranger
```

Some can be renamed, generalized, or moved into optional modules. The default install should be easier to remember than the private beta vault.

## Operating Loop

```text
Capture -> Process -> Plan -> Work -> Close -> Improve
```

If a command is not part of that loop, it does not ship by default.
