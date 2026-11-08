# Product brief

**Owner:** Dave Holmes-Kinsella

**Created:** 2026-11-07

**Status:** Discovery

## Product promise

Know what I worked on, where I worked on it, where I left off, and how it
connects to earlier thinking without manually maintaining a second record of
every AI session.

## Problem

Work and its context are scattered across AI sessions and tools. Finding where
an idea originated, what was decided, and what remains open can require
reconstructing the history by hand. A summary that mistakes suggestions or
discussion for decisions or completed work would be misleading.

## Primary user and context

The primary user works across ChatGPT, Claude, Perplexity, and Muse, including
Muse on desktop, web, and iPhone. A daily batch is sufficient; availability of
unattended exports or complete cross-device capture is not assumed.

## Questions the product should answer

- What did I work on today, and in which source tools and sessions?
- Where did each project leave off, and what questions remain unresolved?
- Where did an artifact or assertion come from?
- How does a concept connect to earlier work across sessions?
- What did I decide or complete, as distinct from suggestions and discussion?

## Desired outcomes

- A source-linked daily work log.
- Project state and unresolved questions with traceable evidence.
- Artifact provenance and links between concepts across sessions.
- Clear separation of user decisions from assistant suggestions, and discussion
  from completed work.

## Initial scope

Investigate capture and daily synthesis of representative sessions from all
four tools. Preserve raw records alongside normalized records, and make derived
views rebuildable from those records. Test provenance and incremental updates
before expanding the scope.

## Non-goals

- Replacing source clients or providing real-time sync.
- Autonomous actions in source tools.
- Building a general-purpose platform.

## Constraints

Capture must respect access permissions and privacy, with manual effort and
cost made visible. MCP must not be a prerequisite. Do not assume unattended
account export or complete coverage across devices; establish what is possible
through evidence and testing.

## Candidate approaches

File-first storage and Markdown/Obsidian are candidates for inspectable records
and views. Nexus importer, LLMnesia, and Graphiti/Zep are candidates to
investigate, not selected dependencies or verified capabilities. Google Drive
or iCloud Drive are acceptable candidates for a common archive; neither is
selected.

## Assumptions and open questions

- Which permitted capture methods are available for each tool, and what manual
  steps do they require?
- Can Muse sessions from desktop, web, and iPhone be captured with adequate
  coverage?
- Which identifiers, timestamps, links, roles, and attachments survive capture
  and support provenance and updated-thread deduplication?
- Which synthesis and retrieval methods help without inventing decisions or
  completion?
- What privacy, cost, and operational burdens are acceptable?

## Initial success criteria

- Evaluate representative sessions from all four tools, including tested Muse
  cross-device coverage; report gaps rather than assume completeness.
- Trace derived assertions to their sources and demonstrate idempotent
  incremental updates, including changed threads.
- In an evaluated sample, fabricate no completed work or user decisions.
- Measure manual effort and cost, and document privacy constraints.

Numeric thresholds are to be determined from discovery, not commitments.

## Next decision

Decide whether available capture and provenance can support a trustworthy daily
ledger at acceptable effort, cost, and privacy, based on the
[discovery plan](discovery-plan.md).
