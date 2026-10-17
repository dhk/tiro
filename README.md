# Tiro

Figures out your conversations.

Conversations get captured all over the place: Wispr Flow, Gemini notes in
Gmail, Zoom, Otter and Teams recaps, iPhone voice memos, the odd ChatGPT
session. Tiro gathers all of them, ties each one to the calendar event it
belongs to, and works out with you **whether it happened, who was really
there, what was said, and who owes what**. It asks you only when something
looks off. It keeps each source's raw text verbatim and stores nothing a model
drafted until you confirm it.

Named for Marcus Tullius Tiro, Cicero's secretary, who is credited with the
Roman shorthand (*notae Tironianae*) used to take down speech as it happened.

## Status

Design only. No code yet.

- [x] Design doc: [docs/design/0001-tiro.md](docs/design/0001-tiro.md)
- [x] One-week read-only pilot over calendar, Wispr Flow and Gmail: [docs/snapshots/2026-10-17-pilot-week.md](docs/snapshots/2026-10-17-pilot-week.md)
- [ ] Wispr Flow adapter
- [ ] Gemini (Gmail + Doc) adapter
- [ ] Calendar matching, duplicate-event merging, anomaly questions
- [ ] MCP server
- [ ] wingman client
- [ ] Zoom, voice memo, vendor-recap and ChatGPT adapters

## Why this exists

Meeting notetakers (Granola, Fireflies, Otter, Fathom) each pull together the
recordings *they* made, then sync them to a CRM. None found takes in another
tool's output (a Gemini email, a Wispr transcript, a voice memo) and files it
against one calendar event. And none answers the questions the pilot showed
matter most: did this meeting actually happen, and who was actually on the
call (the invite list is not the attendee list).

Tiro does only that. Interpreting the record, such as relationship history,
briefs and follow-up drafts, belongs to clients like
[wingman](https://github.com/dhk/wingman).

## Quickstart

Nothing to run yet.

## Stack

| Layer | Choice |
|---|---|
| Interface | MCP server |
| Language / storage | Undecided; see the design doc's open questions |

## Key files

| File | Purpose |
|---|---|
| `docs/design/0001-tiro.md` | Scope, data model, matching and anomaly rules, interface, wingman boundary |
| `docs/snapshots/2026-10-17-pilot-week.md` | The pilot findings the rules came from |
| `HANDOFF.md` | Current state and next step |

## Known issues / watch points

- **Transcripts contain other people's words.** Never commit real
  transcripts, summaries or third-party names. Test fixtures must be synthetic.
- **Never assign a participant from transcript content.** The pilot's one
  content-based guess was wrong; matching on calendar timing was right.

## License

[MIT](LICENSE)
