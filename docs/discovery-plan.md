# Discovery plan

The first milestone is a trustworthy daily ledger from a representative
sample, not deploying a graph. Experiments should use permitted data and record
gaps and uncertainty rather than imply completeness.

## Decision-led investigations

### Source capture and permissions

- **Question:** What permitted capture methods exist for each of the four tools,
  without requiring MCP or assuming unattended exports?
- **Evidence:** First-party documentation, permissions, and observed manual
  steps and access limitations.
- **Experiment:** Capture a representative sample from each tool using available
  methods.
- **Deliverable:** Capture matrix with permissions, steps, and gaps.
- **Decision gate:** Proceed only if a usable sample can be captured lawfully
  and at an acceptable burden; otherwise revise scope or capture approach.

### Export fidelity

- **Question:** Which timestamps, IDs, URLs, roles, and attachments survive
  capture and can support source traceability?
- **Evidence:** Comparison of captured records with their source sessions.
- **Experiment:** Inspect representative exports for each field and attachment,
  including missing or ambiguous values.
- **Deliverable:** Fidelity matrix and provenance gaps.
- **Decision gate:** Choose only records and assertions whose provenance can be
  traced sufficiently; flag or exclude unsupported assertions.

### Updated-thread deduplication

- **Question:** Can repeated captures and changed threads be incorporated
  without duplicate or lost records?
- **Evidence:** Record identities and differences across successive captures.
- **Experiment:** Capture the same thread twice, then capture it after an
  update; repeat the incremental update.
- **Deliverable:** Reconciliation findings and idempotence results.
- **Decision gate:** Pilot only if repeat runs are idempotent and updates remain
  traceable; otherwise revisit identity and reconciliation.

### Muse cross-device coverage

- **Question:** What coverage can be obtained for Muse activity on desktop,
  web, and iPhone?
- **Evidence:** Sessions created or updated on each device and their captured
  counterparts.
- **Experiment:** Compare a representative cross-device sample with captured
  records, noting omissions.
- **Deliverable:** Coverage findings and device-specific limitations.
- **Decision gate:** Decide whether observed coverage is adequate for the
  pilot or requires a narrower claim or different capture method.

### Synthesis quality

- **Question:** Can a daily ledger distinguish decisions, suggestions,
  discussion, and completed work without fabrication?
- **Evidence:** Source-linked assertions and an evaluation against source
  sessions.
- **Experiment:** Produce and review a ledger from the sample, checking every
  evaluated decision and completion claim.
- **Deliverable:** Error and provenance assessment with examples.
- **Decision gate:** Do not rely on the ledger if the evaluated sample
  fabricates decisions or completed work; revise and retest.

### Retrieval usefulness

- **Question:** Do daily, project, and concept views help answer real questions
  and connect earlier thinking?
- **Evidence:** Representative questions, retrieved sources, and user review of
  usefulness and omissions.
- **Experiment:** Try the questions against pilot views and compare answers
  with source records.
- **Deliverable:** Retrieval evaluation and remaining gaps.
- **Decision gate:** Consider graph or agent access only if retrieval evidence
  justifies it over simpler views.

### Operational burden and privacy

- **Question:** Are manual effort, cost, and privacy constraints acceptable?
- **Evidence:** Measured capture and review time, observed costs, data
  handling, permissions, and exposure risks.
- **Experiment:** Run a representative daily cycle and review where raw and
  derived data would be stored and accessed.
- **Deliverable:** Effort and cost measurements and privacy assessment.
- **Decision gate:** Continue only if the user accepts the measured burden and
  privacy risks; otherwise change or stop the approach.

## Provisional sequence

- **Now:** Validate capture and provenance.
- **Next:** Pilot nightly ledger, project, and concept views if the evidence
  supports them.
- **Later:** Evaluate graph or agent access if retrieval evidence justifies it.

See the [product brief](product-brief.md) and
[edited origin record](sources/2026-11-07-origin-conversation.md).
