# The Dispatch

*A field installation for people who think with a pen.*

---

The machine is very good at one thing: making everything sound like it was made by the machine. The way out is not better prompts, smarter models, or a more baroque folder system. It is context: the accumulated record of what you actually think, what you actually care about, and what was happening on a given Tuesday six months ago when something shifted in a way you had not yet named.

The machine cannot fake that. It can only read it.

The Dispatch is a system for building that record. You write a daily dispatch. The relay reads across the record and returns signal: patterns you missed, contradictions you have not reconciled, and questions that come from your actual life instead of from generic productivity weather.

It does not replace the work. It keeps the work from disappearing.

---

## What you need

- [Obsidian](https://obsidian.md) - free
- [Claude Code](https://claude.ai/code) - Claude Pro or Max account
- Git - installer at [git-scm.com](https://git-scm.com/downloads). One-time, about 100MB. Do not install Xcode just for this.

Recommended Obsidian setup:

- Install the community plugin **Notebook Navigator**.
- Switch Notebook Navigator to **Dual Panel** view.

That is the only Obsidian plugin I recommend for the public setup. It makes the vault easier to see without turning visibility into another project.

No MCPs. No paid templates. No connector maze.

---

## Install

1. Create a new Obsidian vault. Note where it lives.
2. Optional but recommended: install Notebook Navigator and switch it to Dual Panel.
3. Open Claude Code in that vault folder.
4. Copy the contents of [BOOTSTRAP.md](BOOTSTRAP.md), paste into Claude Code, and press Enter.
5. Answer the short setup questions.

Your vault is built: folders, briefing files, daily template, and eleven slash commands.

---

## The shape of it

The public Dispatch now uses the same station map as the private installation. The difference is not the skeleton. The difference is depth: the private vault has personal material, business commands, and private operating files. The public vault keeps the same map and a smaller command set.

```text
00 - DEAD DROP/         incoming captures and loose material
01 - DISPATCHES/       daily and periodic writing
02 - INTEL/            research, captures, ideas, source material
03 - WORKS/            drafts, essays, voice reference, finished work
04 - OPS/              projects, business, tasks, operations
05 - VITALS/           body, health, family, home, identity
06 - RELAY/            briefing, plans, systems, command map
_Archive/              retired material
99 - ASSETS/           attachments, PDFs, images
.claude/commands/      slash commands
```

The station names matter because they let Obsidian, Claude Code, Codex, and future users all speak the same language. One map. Less translation.

---

## The commands

Eleven commands. That remains the ceiling for the public version.

**Daily loop**

- `/daily-spark` - morning signal: a quote plus 2-3 questions drawn from the recent record
- `/today` - the day's field orders
- `/closeday` - end-of-day debrief that seeds tomorrow
- `/inbox` - triage the Dead Drop
- `/new` - brain dump to the right place, quickly

**Weekly calibration**

- `/weekly` - honest review of what moved and what did not
- `/stranger` - third-person portrait of who the vault shows you are this week

**Deep work**

- `/decode` - run after writing something with heat
- `/ghost` - answer a question as you would, using vault evidence
- `/psycho` - pattern mirror through therapeutic lenses, not a diagnosis
- `/dreaming` - slow associative pass on a stuck sentence, scene, or idea

Full reference in [COMMANDS.md](COMMANDS.md).

---

## What makes it different

**Voice firewall.** The relay never quietly becomes the author. J.R.'s writing and relay output are structurally separated. Relay additions live inside `> [!relay]` callout blocks so future analysis can tell the difference.

**No replacement writing.** The relay edits, structures, surfaces, challenges, and asks better questions. The hands that write are yours.

**Built to compound.** The first week is thin. The first month begins to bite. After three months the commands can surface things you said and forgot, contradictions you keep circling, and small truths the day-to-day made invisible.

---

## The daily dispatch

The daily dispatch is a single file per day in `01 - DISPATCHES/Daily/`. It is the engine of the system.

Morning:

1. Run `/daily-spark`.
2. Write below the questions.
3. Run `/today`.

Evening:

4. Run `/closeday`.

That is the loop. Capture loose material into `00 - DEAD DROP/`. Use `/inbox` when the drop zone gets noisy. Use `/weekly` to keep the week honest.

The vault is only as smart as the dispatches are honest.

---

## Automations

If your Claude Code or Codex environment supports scheduled routines, keep the automation simple:

```text
Run /daily-spark every weekday morning.
Run /closeday every evening if a dispatch exists.
Run /weekly once a week.
```

Do not automate the writing. Automate the invitation to write.

---

## A note on what this is not

This is not a total productivity system. It will not make every task visible, clean your inbox, or run your life by itself. It is a writing instrument and a memory layer. The output is signal, not throughput.

If you want a tool that books your meetings and tracks every habit, this is not it. If you want a place where the texture of your actual thinking lives, and a relay that reads that texture and gives it back to you, this is exactly it.

---

## License & credit

Use it. Modify it. Make it yours. Built by [J.R. Clubb](https://jrclubb.substack.com).

The discipline is the point: same skeleton, fewer commands, less ceremony. If you want to add another command, first ask whether one of the eleven already covers the job.
