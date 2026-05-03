# The Dispatch

*A field installation for people who think with a pen.*

---

The machine is very good at one thing: making everything sound like it was made by the machine. The way out is not better prompts, smarter models, or more carefully organized folders. It is context — the accumulated record of what you actually think, what you actually care about, and what you were doing on a given Tuesday six months ago when something shifted in a way you have not yet named.

The machine cannot fake that. It can only read it.

The Dispatch is a system for building that record. You write a daily dispatch — a brain dump across four frequencies of your life. Over time, the vault accumulates weight. The relay reads that weight and returns signal: patterns you missed, contradictions you have not reconciled, drafts in your own voice that no model could have generated cold.

It does not generate filler. It surfaces what you have already put in.

---

## What you need

- [Obsidian](https://obsidian.md) — free
- [Claude Code](https://claude.ai/code) — Claude Pro or Max account
- Git — installer at [git-scm.com](https://git-scm.com/downloads). One-time, ~100MB. Don't install Xcode.

That's it. No MCP. No plugins. No paid templates.

---

## Install

1. Create a new Obsidian vault. Note where it lives.
2. Open Claude Code in that folder.
3. Copy the contents of [BOOTSTRAP.md](BOOTSTRAP.md). Paste into Claude Code. Press Enter.
4. Answer four questions.

Two minutes. Your vault is built — folders, briefing files, eleven slash commands.

---

## The shape of it

**Seven folders.** Four for what you keep, three for the system.

```
Drop/         everything incoming lands here first
Log/          your dispatches — sacred, append-only
Notes/
  Mind/         what you know and are learning
  People/       the people who matter
  Body/         physical reality
  Work/         the campaign — projects, output, money
Relay/        briefing files, daily plans
```

**Eleven commands.** Five for the daily loop, two for weekly calibration, four for deep work when the loop isn't enough.

**Daily loop**
- `/spark` — four excavation questions, one per frequency, drawn from what you've actually been writing
- `/today` — the day's field orders
- `/closeday` — end-of-day debrief that seeds tomorrow's spark
- `/inbox` — triage the Drop folder
- `/new` — brain dump to the right file, instantly

**Weekly calibration**
- `/weekly` — honest review of what moved and what didn't
- `/stranger` — third-person portrait of who you actually are this week, written from evidence

**Deep work**
- `/decode` — run right after writing something with heat. Surfaces what's alive, what to file, what to act on, what you're not seeing
- `/ghost` — answers a question as you would, using only vault evidence, then scores its fidelity
- `/psycho` — runs your dispatches through five therapeutic lenses and surfaces the loops you can't see from inside
- `/dreaming` — drop a stuck sentence or fragment and let the relay find what it's reaching for

Full reference in [COMMANDS.md](COMMANDS.md).

---

## What makes it different

**Voice firewall.** Every command knows the structural difference between what *you* wrote and what the *relay* wrote. The relay can never quietly start speaking for you, because its output is physically quarantined inside callout blocks. Six months from now, when you ask it to write in your voice, it will not have contaminated its own training data with its own voice.

**No content generation. Period.** The relay edits, structures, surfaces, challenges. The hands that write are yours. This is not a feature — it is the entire premise.

**Built to compound.** The first week is thin. The first month begins to bite. After three months the analytical commands become uncanny — they will surface things you said and forgot, contradictions you have not reconciled, patterns the day-to-day made invisible.

---

## The daily dispatch — what it actually is

The dispatch is a single file per day in `Log/Daily/`. It is the engine of the whole system. Everything else — the analytical commands, the weekly review, the portrait, the ghost — is reading what you put here.

The format is simple: `/spark` loads four questions into today's file, one per frequency of your life (People / Body / Mind / Work). You write below them. Voice memo transcript, brain dump, one sentence — whatever came out that morning. Then `/today` builds your field orders. In the evening, `/closeday` processes it and seeds the next morning.

**The vault is only as smart as the dispatches are honest.** The first week is thin. After two weeks it starts to bite. After two months the relay will surface things you said and forgot. That is when it gets interesting.

---

## How to run it

Tomorrow morning:

1. Open Obsidian. Open Claude Code in your vault.
2. Type `/spark`. Four questions appear in today's dispatch file.
3. Write below them. Whatever came. Don't edit it.
4. Type `/today`. Get your field orders.
5. Work them.

End of day:

6. Type `/closeday`. The relay debriefs, files what should be filed, seeds tomorrow's signal.

That's the loop. Once a week, run `/weekly`. Once a month, run `/stranger`. Use the deep work commands when something specific calls for them.

The vault grows from the dispatches outward.

---

## Automate the morning signal

Once you have the rhythm, you can have `/spark` run automatically each morning — questions already waiting in your dispatch file before you sit down.

In Claude Code, type:

```
Set a daily schedule to run /spark at 6am.
```

Claude will confirm. After that, the morning signal writes itself. Run `/closeday` at the end of the day the same way:

```
Set a daily schedule to run /closeday at 9pm.
```

The loop runs itself. Your only job is to write into it.

---

## A note on what this is not

This is not a productivity system. It will not make you a better operator overnight, hit your inbox to zero, or 10x your output. It is a writing instrument and a memory layer. The output is *signal*, not *throughput*.

If you want a tool that books your meetings and tracks your habits, this is not it. If you want a place where the texture of your actual thinking lives — and a relay that reads that texture and gives it back to you — this is exactly it.

---

## License & credit

Use it. Modify it. Make it yours. Built by [J.R. Clubb](https://jrclubb.substack.com).

The Dispatch is the public, opinionated core. The private version that runs my own life has more — but more is not the goal. Eleven commands is the ceiling. Four note folders, plus three for the system, is the ceiling. If you find yourself adding a command, ask first whether the existing eleven can already do it.

The discipline is the point.
