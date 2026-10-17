# Handoff

**Last updated:** 2026-10-17
**Active branch:** `docs/1-bootstrap-tiro`

Read this fully before doing anything. Then read `CLAUDE.md` for technical
detail.

This file is overwritten every session — it always reflects *now*, not
history. For a permanent record of a design decision or pivot, write to
`docs/snapshots/YYYY-MM-DD-<topic>.md` instead and leave this file pointing
at the current state.

## Current state

Design only. The repo has been set up from repo-template; the design doc and
pilot snapshot are written. No code.

## What's next

1. **Paused for a design / market-fit review** (design §12). Do not start
   code until the owner says the review has landed. Stack is decided:
   Python, SQLite, running on lobster.
2. Wispr Flow adapter. Wispr is the richest source and usually carries a
   calendar link already.
3. Gemini adapter: Gmail `from:gemini-notes@google.com` plus the "Notes by
   Gemini" Doc attached to the calendar event.

## Known issues / watch points

1. **Duplicate calendar events are normal, not an error.** The owner blocks
   time; the other party sends their own invite with the link. Merge
   automatically (design §6).
2. **Speaker labels in vendor summaries mix up who owes what.** Every action
   item's owner needs confirming before it can leave `proposed`.

## Open questions

See `docs/design/0001-tiro.md` §12.
