# Claude Code Memory Guide

How the three-layer system maps onto Claude Code specifically, and how to write and maintain the files that implement it.

---

## Where This Fits

Every other platform in this framework implements the three layers as account settings: a text box for preferences, a text box for project instructions, a memory feature you can't inspect directly. Claude Code implements them as files on disk. That's not a detail, it changes what you can do with them: version them, diff them, review them in a pull request, script their maintenance.

The mapping:

- **Layer 1 (Personal Preferences)** → `~/.claude/CLAUDE.md`, the user-level file, applies to every project on this machine.
- **Layer 2 (Project Context)** → `./CLAUDE.md` at the project root, plus `./CLAUDE.local.md` for anything project-specific you don't want shared with the rest of the team.
- **Layer 3 (Project Memory)** → the auto memory system, a set of files Claude itself writes as it works with you. Nobody has to author these by hand.

The rest of this guide covers each of those in turn, then how to keep them healthy.

---

## The CLAUDE.md Hierarchy

Claude Code reads CLAUDE.md files from four levels, most specific last, and they combine rather than override wholesale:

1. **Managed policy** (organisation-wide): `/etc/claude-code/CLAUDE.md` on Linux, `/Library/Application Support/ClaudeCode/CLAUDE.md` on macOS, or set via registry policy on Windows. This is for team or company-wide rules pushed by an admin, not something you'll touch on a personal project. Worth knowing it exists if you ever roll Claude Code out for work rather than yourself.
2. **User memory**: `~/.claude/CLAUDE.md`. Yours, applies everywhere. This is where the `Writing Voice` import and the general `Communication Style` rules for this setup live.
3. **Project memory**: `./CLAUDE.md` in the repository root. Checked into git, shared with anyone else working on the project. This is Layer 2 proper.
4. **Local memory**: `./CLAUDE.local.md`, gitignored, for a personal override on a shared repo. Worth a caveat: this pattern is being phased out in favour of a gitignored file pulled in with `@import` (see below), because a bare `.local.md` file has caused merge friction for some teams. Either approach works; the import version is just more explicit about what's happening.

If you're working alone, in practice you'll mostly live in levels 2 and 3.

---

## Writing a CLAUDE.md

The useful frame is **WHAT, WHY, HOW**:

- **WHAT**: tech stack, versions, project structure.
- **WHY**: the architectural decisions and the reasoning behind them, not just the outcome.
- **HOW**: commands, workflow rules, procedures.

Include:

- Specific versions ("Entity Framework Core 10", not "EF Core")
- Project structure, mapped, not just named
- Build, test, run, deploy commands
- Conventions you follow, and just as usefully, patterns you deliberately don't use
- Domain terminology particular to the project
- Repository workflow conventions (branching, commit style, PR expectations)

Exclude:

- Secrets, credentials, connection strings, obviously
- Style rules a linter already enforces, don't duplicate `.editorconfig`
- Anything a competent engineer would already know about the framework
- Long-form documentation, link to it instead of pasting it in
- Historical context nobody needs to act on today

Anthropic's own guidance is to keep each file under roughly 200 lines. Longer files get skimmed, not followed. If a project genuinely needs more than that, split it: a `.claude/rules/` directory holds files scoped to specific paths via frontmatter, so detail only loads when it's relevant.

```
---
paths:
  - src/Modules/Identity/**
  - tests/**/Identity*
---
# Identity Module Rules
```

That file stays out of context entirely unless Claude is actually touching something under `src/Modules/Identity/`.

A few things that reliably make a CLAUDE.md worse, worth checking your own against:
- Using it as a linter substitute instead of pointing at the linter
- Leaving in whatever `/init` generated without trimming it down
- Letting it drift as the codebase changes underneath it
- Restating documentation that already exists elsewhere, rather than linking to it

---

## The `@import` Syntax

A CLAUDE.md can pull in another file:

```
@path/to/file.md
```

Paths resolve relative to the file doing the importing. `~/path` works too. Imports go four hops deep at most, and expand when Claude Code launches, so they don't save you any context budget, they just save you from copy-pasting the same content into several files.

You've already seen this in practice: the `Writing Voice` section of `~/.claude/CLAUDE.md` for this setup is a single line, `@MPA_writing-style-guide.md`, pulling in a separate style document rather than inlining it. One source of truth, one place to edit it.

One practical note: importing a file from outside the current project (an absolute path, or something under a different repo) triggers an approval prompt the first time it's used in a session. That's expected, not a bug.

---

## Auto Memory: Layer 3, Automatic

This is the piece that didn't exist when the rest of this framework was written, and it changes the Layer 3 story for this platform specifically.

Everywhere else, Layer 3 means the Rule of Three: notice friction, wait for it to repeat, write the memory instruction yourself. On Claude Code, recent versions do most of that loop for you. Claude keeps its own notes, separate from CLAUDE.md, under `~/.claude/projects/<project>/memory/`. An always-loaded `MEMORY.md` acts as the index; individual topic files load only when they're relevant, the same on-demand pattern as the `.claude/rules/` directory above. It's machine-local, it doesn't follow you to a different computer.

The notes fall into four kinds:

- **User**: who you are, your role, how you like to work
- **Feedback**: corrections and confirmations about approach, both what to avoid and what worked
- **Project**: decisions, deadlines, context specific to what's being built
- **Reference**: pointers to where the real information lives (a Linear project, a Slack channel, a dashboard)

You still have a hand in it. Say "remember this" and it gets captured immediately, no waiting for a third occurrence. You can open and edit the files directly if something's wrong. But the default path, correction happens, pattern recognised, memory written, now runs without you doing the writing.

Keep `memory-guide.md`'s Rule of Three as the mental model for *how* memory should evolve (don't over-capture single occurrences, keep it lean, remove what's stopped being useful), it still applies here. What's different on this platform is who's holding the pen.

---

## Maintaining It: the `claude-md-management` Plugin

Two tools ship in this plugin, and they cover the two maintenance jobs a CLAUDE.md actually needs.

**`/claude-md-management:revise-claude-md`** looks back over the current session and asks what context was missing, then proposes concise, targeted additions to the right file (shared `CLAUDE.md` versus a local/gitignored one), shows you the diff, and only applies it once you say yes. Use it at the end of a session where you had to explain something Claude should already have known.

**`/claude-md-management:claude-md-improver`** is the audit pass. It finds every CLAUDE.md in the repo, scores each one against a rubric (commands documented, architecture clarity, non-obvious patterns captured, conciseness, currency, actionability), and produces a quality report before touching anything. Run this monthly, or whenever a project has drifted enough that Claude keeps making the same wrong assumption.

Both work the same way: report first, diff second, nothing applied without your say-so.

There's also a faster path for small additions mid-session: press `#` and whatever you type gets folded into the appropriate CLAUDE.md directly, no separate command needed.

---

## AGENTS.md

`AGENTS.md` is an emerging cross-tool standard, an attempt at one instructions file multiple AI coding tools can read, rather than every tool wanting its own. Claude Code doesn't read it natively, it reads `CLAUDE.md`. If a project already has an `AGENTS.md` for other tooling, don't duplicate its contents, import it:

```
@AGENTS.md
```

then add anything Claude-specific below the import. This is a young enough convention that it's worth revisiting as it matures rather than building deep tooling around it now.

Worth knowing while we're here: a project-root `CLAUDE.md` survives context compaction, when a long session compacts, Claude re-reads it from disk and re-injects it. Anything said only in conversation doesn't survive that. If an instruction matters for the rest of a long session, it belongs in the file, not just in what you typed.

---

## Related Documents

- **[memory-guide.md](memory-guide.md)**: the platform-agnostic Rule of Three, still the right mental model for how memory should evolve
- **[project-context-guide.md](project-context-guide.md)**: Layer 2 in general, this guide is the Claude Code-specific implementation of it
- **[GLOSSARY.md](../GLOSSARY.md)**: CLAUDE.md, auto memory, and `@import` are defined there alongside the rest of the framework's terms
