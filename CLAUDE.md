# CLAUDE.md

This file provides guidance to Claude Code when working with code in this
repository.

## What this is

Tiro is a narrowly scoped service that figures out conversations. It takes in
transcripts and notes from many capture tools, matches each to a calendar
event, merges duplicate events, asks the owner about anomalies (a meeting that
may not have happened, one that may have been cut short, a recording with no
event or with two candidate events), and records confirmed participants,
summaries and action items. It exposes this as an MCP server. wingman is a
client; Tiro never calls wingman.

The one idea that matters most: **raw sources are stored verbatim; anything a
model drafted (summary, action items, participants) is stored only after the
owner confirms it.** Participants are never inferred from transcript content.

## Workflow Rules

**All work in this repo must go through branches and PRs.**

- Never commit directly to `main`
- Every task starts with a GitHub issue
- Every issue gets its own branch (`feat/`, `fix/`, `chore/`, `docs/` prefix)
- Every branch gets a PR before merging
- PRs should reference the issue they close (`Closes #N`)

## Architecture

See `docs/design/0001-tiro.md`. In short: source adapters → `Source` records
(immutable, verbatim) → matching to calendar events → `Conversation` with
anomalies → owner confirmation → MCP read API for clients.

## Commands

```bash
# none yet. The stack is undecided.
```

## Conventions

- **No real data in the repo.** No transcripts, summaries, meeting titles or
  third-party names, in code, fixtures, docs or commit messages. Use
  synthetic fixtures with role names ("contact A").
- Evidence tiers follow wingman RFC-073: `observed` (verbatim) and `endorsed`
  (model draft the owner confirmed). Unconfirmed drafts are never persisted
  as anything but `proposed`.
- Identity crosses to clients by email only.

## Notes for next session

- Stack: Python, SQLite, runs on lobster. Code is paused pending a
  market-fit review (design §12).
