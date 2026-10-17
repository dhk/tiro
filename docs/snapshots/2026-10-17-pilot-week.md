# 2026-10-17 — pilot week

A read-only pass over 2026-10-10..17: Google Calendar, Wispr Flow
(`search_meetings`, `get_meeting`) and Gmail (search for Gemini, Zoom, Otter,
Teams and Fathom recaps). Nothing was written anywhere. Third parties are
anonymized.

## Scope

Excluded: solo time blocks (reminders, journaling) and a recurring nightly
household check-in. That left **14 conversations** with other people.

## Coverage

| Outcome | Count |
|---|---|
| Captured by Wispr, linked to a calendar event | 2 |
| Captured by Gemini (summary email + Doc on the event) | 1 |
| Captured by Wispr, not linked, overlapping 2 events | 1 |
| Video call, nothing captured | 7 (2 Zoom, 5 Meet) |
| In person, nothing captured (expected) | 3 |
| Captured with no calendar event at all | 1 extra (not in the 14) |

No Zoom, Otter, Teams or Fathom recap emails arrived that week.

## Findings

1. **Duplicate events.** One call existed as the owner's own time block (no
   attendees) plus the guest's Zoom invite 15 minutes later. The owner says
   this pattern is routine. → auto-merge rule (design §6).
2. **Ambiguous recording.** An unlinked 17-minute Wispr recording overlapped
   a loose-fitting event (50 min, started 18 min earlier) and a tight-fitting
   one (25 min, started 3 min earlier, created that morning). The assistant
   ignored both and named a third person, based on what the summary said.
   The owner corrected it: the tight-fitting event was right. → closest-fit
   scoring plus owner confirmation, and no participant inference from content
   (design §5).
3. **Misattributed action items.** One vendor summary assigned every next step
   to a speaker label, contradicting its own body. Another assigned an ask
   to the wrong side. → action items stay `proposed` until owners are
   confirmed (design §7, `owner_unclear`).
4. **Cut short / no-show.** No case appeared this week, but the owner reports
   both happen. → `maybe_no_show`, `maybe_cut_short` anomalies (design §7).
5. **Coverage is the bottleneck.** 4 of 14 captured. Better summaries do not
   help a call nobody recorded.
