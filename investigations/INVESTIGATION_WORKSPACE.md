---
title: "Investigation Workspace"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Investigation PM"
technical_reviewer: pending
security_reviewer: pending
ip_reviewer: pending
knowledge_id: KID-INV-0001
knowledge_domain: investigation
knowledge_object: capability
authority_tier: T5
is_authority: true
authority_document: KID-INV-0001
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INVESTIGATION_SESSION_PLATFORM.md
  - docs/current/architecture/ARCHITECTURE_INVESTIGATION_EVIDENCE_WORKSPACE.md
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
related_documents:
  - docs/public/platform/WHAT_IS_SENTRISCOPE.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
  - docs/public/capabilities/ATTACK_GRAPH_OVERVIEW.md
knowledge_relationships:
  depends_on:
    - KID-PLT-0001
    - KID-PLT-0003
    - KID-ARC-0001
  explains: []
  supersedes: []
  related_to:
    - KID-AGR-0001
    - KID-OIN-0001
  implements: []
  introduces: []
  deprecates: []
  expands:
    - KID-PLT-0003
navigation:
  personas: [analyst, engineer]
  learning_paths: [LP-002]
  prerequisites:
    - KID-PLT-0001
    - KID-PLT-0003
    - KID-ARC-0001
  next_reading:
    - KID-AGR-0001
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md#kid-inv-0001--investigation-workspace
publication_phase: stream-a
website_slug: investigation-workspace
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "SentriScope investigation workspace is an analyst-led, session-based environment that preserves scope, evidence, hypotheses, findings, and context across modules—requiring human validation and never replacing deterministic intelligence engines."
knowledge_tags:
  - investigation
  - evidence
  - analyst
  - capability
---

# Investigation Workspace

## Industry Problem

Security investigations rarely finish in a single sitting. Analysts switch between vulnerability data, identity context, threat intelligence, tickets, and collaboration tools. Each switch loses layout state, open entities, partial conclusions, and the reasoning chain that connects evidence to decisions.

Without a persistent investigation context, teams duplicate work, contradict earlier conclusions, and struggle to explain *why* a decision was made weeks later during audit or handoff.

## Why the Problem Exists

Enterprise security platforms historically optimized for **lists and dashboards**, not for **long-lived analytical work**. SIEM consoles focus on events; vulnerability tools focus on findings; ITSM focuses on tickets. None treats the investigation itself as a durable object that spans tools and time.

Analysts compensate with spreadsheets, notes, screenshots, and tribal knowledge—none of which inherit governance, provenance, or tenant isolation by default.

## Traditional Approaches

| Approach | Limitation |
|----------|------------|
| Ad hoc notes and documents | No provenance; hard to audit |
| Ticket-only workflows | Captures outcome, not reasoning |
| Static dashboards | No session continuity |
| SOAR playbooks | Automate response; rarely preserve analyst reasoning |
| Shared drives / wikis | Outside security governance boundaries |

Mature programs aim for **evidence-first investigation**: every conclusion traceable to integrated sources, with analyst validation explicit in the workflow.

## SentriScope Perspective

SentriScope treats an **investigation session** as a first-class operational object (implemented). The investigation workspace is the analyst-facing surface where that session lives—not a generic dashboard, and not an autonomous agent.

Core design principles:

- **Investigation-first** — The session outlives any single page or module visit.
- **Analyst in control** — Conclusions and governed decisions require human validation.
- **Evidence-driven** — Findings link to supporting and contradictory evidence; see [KID-ARC-0001](../architecture/CANONICAL_DATA_MODEL.md) for the evidence concept.
- **Deterministic intelligence remains authoritative** — Risk scores, graph traversal, and enrichment outputs are consumed; the workspace records what the analyst selected and why.
- **Tenant-scoped and auditable** — All session data respects tenant boundaries and security-relevant actions are logged.

Analytical lineage the platform preserves (conceptually):

```text
Evidence → Hypothesis → Finding → Recommendation draft → Decision → Outcome
```

The workspace integrates notebook-style analyst knowledge, structured findings and hypotheses, curated evidence packages, bookmarks, timeline position, and navigation history—without replacing the canonical data layer described in global authorities [KID-PLT-0001](../platform/WHAT_IS_SENTRISCOPE.md) and [KID-PLT-0003](../platform/PLATFORM_OVERVIEW.md).

## Current Product Capability

| Capability | State | Summary |
|------------|-------|---------|
| Investigation session persistence | Implemented | Pause and resume investigations with scope and context |
| Workspace layout and navigation state | Implemented | Panels, filters, open entities, cross-module continuity |
| Findings and hypotheses | Implemented | Structured reasoning with severity, confidence, relationships |
| Evidence workspace (curated packages) | Implemented | Analyst-assembled evidence collections with provenance |
| Recommendation drafts from findings | Implemented | Conversion path; does not auto-create governed recommendations |
| Attack graph state within session | Implemented | Supports investigation-oriented path context |
| AI conversation memory (investigation) | Implemented | Assistive; read-only with respect to critical evidence paths |
| Collaboration and replay | Implemented | Multi-analyst collaboration and session replay capabilities |
| Autonomous investigation closure | Not available | Analyst validation required |

For platform-wide maturity qualifiers, see [KID-PLT-0004](../platform/PRODUCT_MATURITY.md)—the sole authority for implemented vs partial vs planned status.

## Current Limitations

- SentriScope **does not** autonomously close investigations or approve decisions without analyst action.
- Investigation depth varies by integrated data sources; empty or stale connectors reduce session value.
- Not every evidence subtype has complete public documentation yet; advanced evidence quality dimensions exist in the product but are not fully described publicly.
- The investigation workspace **complements** SIEM, SOAR, and ticketing tools—it does not replace them. See [KID-PLT-0002](../platform/WHAT_SENTRISCOPE_IS_NOT.md).
- Organizational intelligence themes may extend investigation context progressively; not all are generally available.

## Common Questions

### Is the investigation workspace the same as a SOAR case?

No. The workspace preserves analyst reasoning and evidence within SentriScope's tenant-scoped model. SOAR cases orchestrate response across external tools. Integration may exist; replacement is not the design center.

### Does AI run investigations automatically?

No. AI assistance supports analysis workflows and may consume curated evidence packages. It does not replace analyst validation or deterministic scoring paths. See [KID-PLT-0002](../platform/WHAT_SENTRISCOPE_IS_NOT.md).

### What entities can investigations reference?

Investigations operate over canonical concepts—assets, identities, exposures, incidents, threat intelligence, and related entities—defined authoritatively in [KID-ARC-0001](../architecture/CANONICAL_DATA_MODEL.md). This document does not redefine those entities.

### Can investigations be reused as organizational knowledge?

Yes (implemented). Sessions are designed to convert investigation outcomes into reusable organizational knowledge over time, subject to tenant governance.

## Related Concepts

### Prerequisites (authority)

- [What is SentriScope?](../platform/WHAT_IS_SENTRISCOPE.md) — `KID-PLT-0001`
- [Platform Overview](../platform/PLATFORM_OVERVIEW.md) — `KID-PLT-0003`
- [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md) — `KID-ARC-0001`

### See also

- [Attack Graph Overview](../capabilities/ATTACK_GRAPH_OVERVIEW.md) — `KID-AGR-0001`
- [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md) — `KID-OIN-0001`

### Planned (Stream B — education)

- `KID-CON-0001` Evidence-Based Investigation
- `KID-GLS-0001` Investigation session
- `KID-GLS-0002` Evidence workspace

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INVESTIGATION_SESSION_PLATFORM.md` | Session model, components, maturity |
| `docs/current/architecture/ARCHITECTURE_INVESTIGATION_EVIDENCE_WORKSPACE.md` | Evidence package and provenance concepts |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Safe public messaging boundaries |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Investigation PM | Initial domain authority (Stream A) |
