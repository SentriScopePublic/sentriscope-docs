---
title: "Operational Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Intelligence PM"
technical_reviewer: pending
security_reviewer: pending
ip_reviewer: pending
knowledge_id: KID-OIN-0001
knowledge_domain: operational-intelligence
knowledge_object: capability
authority_tier: T5
is_authority: true
authority_document: KID-OIN-0001
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md
  - docs/current/architecture/ARCHITECTURE_OPERATIONAL_INTELLIGENCE.md
  - docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md
related_documents:
  - docs/public/intelligence/THREAT_INTELLIGENCE.md
  - docs/public/investigations/INVESTIGATION_WORKSPACE.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
knowledge_relationships:
  depends_on:
    - KID-PLT-0001
    - KID-PLT-0003
    - KID-ARC-0001
  explains: []
  supersedes: []
  related_to:
    - KID-TIN-0001
    - KID-INV-0001
    - KID-AGR-0001
  implements: []
  introduces: []
  deprecates: []
  expands:
    - KID-PLT-0003
navigation:
  personas: [ciso, analyst]
  learning_paths: [LP-002]
  prerequisites:
    - KID-PLT-0001
    - KID-PLT-0003
  next_reading:
    - KID-TIN-0001
    - KID-INV-0001
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md#kid-oin-0001--operational-intelligence
publication_phase: stream-a
website_slug: operational-intelligence
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "Operational intelligence in SentriScope aggregates canonical security data into ranked attention points and CISO-oriented summaries using deterministic prioritization—helping teams decide where to focus without replacing investigation or autonomous response."
knowledge_tags:
  - operational-intelligence
  - dashboard
  - prioritization
  - capability
---

# Operational Intelligence

## Industry Problem

Security operations produce more signal than any team can manually triage. Analysts open multiple consoles—vulnerability management, identity, exposure, threat feeds, ITSM—and mentally correlate which issues matter *today* for *their* environment.

Leaders ask a different question: *Where should we focus limited people and budget right now?* Dashboards that only count open findings without business context, threat relevance, or control coverage fail both operators and executives.

## Why the Problem Exists

Data fragmentation creates **attention fragmentation**. Each tool optimizes its own queue. Risk scores from one product rarely incorporate active threat campaigns, missing controls, and business criticality in a single, explainable ranking.

Without operational intelligence, teams either over-react to noisy alerts or under-react to correlated conditions that no single tool surfaces prominently.

## Traditional Approaches

| Approach | Limitation |
|----------|------------|
| SIEM rule queues | Event-centric; not always business-aligned |
| Vulnerability SLA dashboards | Volume-focused; weak threat and coverage context |
| Executive PDF reports | Static; stale on arrival |
| Manual weekly triage meetings | Does not scale; tacit knowledge |
| Generic BI on security data | Often lacks security-specific explainability |

Mature **operational intelligence** combines continuous data integration, deterministic prioritization, and explainable reason codes so humans can trust and audit the queue.

## SentriScope Perspective

In SentriScope, **operational intelligence** is the capability that helps teams **decide where to focus** by aggregating normalized canonical data into ranked, explainable attention surfaces (implemented).

It sits in the intelligence correlation layer described in [KID-PLT-0003](../platform/PLATFORM_OVERVIEW.md)—above governed ingestion and canonical normalization, and alongside—not replacing—investigation and decision support.

Public-safe framing:

| Concept | Meaning in SentriScope |
|---------|------------------------|
| **Attention point** | A ranked item explaining why something needs focus now |
| **Reason codes** | Deterministic explanations (for example coverage gap, long-lived exposure, threat relevance) |
| **Evidence references** | Pointers to canonical entities supporting the attention point |
| **Recommended action** | Suggested next step—often investigation or remediation—not autonomous execution |

**Deterministic prioritization:** Critical attention-point computation does **not** rely on LLM scoring. AI may assist read-only analysis elsewhere; see [KID-PLT-0002](../platform/WHAT_SENTRISCOPE_IS_NOT.md).

SentriScope also evolves **operational intelligence specialists**—domain reasoning over platform signals with structured, non-destructive outputs (partial / pilot maturity). These interpret deterministic services; they do not replace risk engines, evidence governance, or analyst approval. Full maturity: [KID-PLT-0004](../platform/PRODUCT_MATURITY.md).

Operational intelligence **feeds** [KID-INV-0001](../investigations/INVESTIGATION_WORKSPACE.md); it does not define investigation procedures.

## Current Product Capability

| Capability | State | Summary |
|------------|-------|---------|
| Global intelligence dashboard | Implemented | Consolidated prioritization entry point for operators |
| Deterministic attention-point ranking | Implemented | Explainable priority with reason codes |
| Technology + threat + coverage context | Implemented | Aggregates canonical vulnerability, asset, and intel data |
| CISO-oriented summaries | Implemented | Executive visibility without replacing detail modules |
| Intelligence insights contract | Implemented | Structured insight emission from attention surfaces |
| Operational intelligence specialists / mission control themes | Partial / progressive | Reasoning layer and advanced mission themes not all generally available |
| Autonomous remediation from attention queue | Not available | Human-in-the-loop decisions required |
| SOAR replacement | Not available | See [KID-PLT-0002](../platform/WHAT_SENTRISCOPE_IS_NOT.md) |

## Current Limitations

- Attention quality depends on connector coverage and data freshness—see [KID-INT-0001](../integrations/SUPPORTED_DATA_SOURCES.md).
- Operational intelligence **does not** replace list and detail views for every domain; it prioritizes entry.
- Advanced workforce and mission-control experiences are **partially implemented** or on progressive rollout.
- No public performance benchmarks (for example triage reduction percentages) are claimed.
- Reason-code catalog and specialist behaviors may evolve; `next_review` applies.

## Common Questions

### Is operational intelligence the same as a SIEM?

No. It prioritizes correlated canonical security context for human decisions. SIEMs focus on log and event detection pipelines. SentriScope may complement SIEM data via integrations.

### Does SentriScope automatically fix what the dashboard highlights?

No. Recommended actions suggest next steps; governed decisions and optional integrations handle execution—with analyst validation.

### How is this different from threat intelligence?

Threat intelligence emphasizes external CTI lifecycle and indicator correlation—[KID-TIN-0001](../intelligence/THREAT_INTELLIGENCE.md). Operational intelligence **consumes** threat context among other signals to rank operational attention.

### Can executives rely on this instead of detailed reports?

Executives gain a governed summary; due diligence still requires detail modules, maturity context [KID-PLT-0004](../platform/PRODUCT_MATURITY.md), and investigation where needed.

## Related Concepts

### Prerequisites

- [What is SentriScope?](../platform/WHAT_IS_SENTRISCOPE.md) — `KID-PLT-0001`
- [Platform Overview](../platform/PLATFORM_OVERVIEW.md) — `KID-PLT-0003`
- [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md) — `KID-ARC-0001`

### See also

- [Threat Intelligence](../intelligence/THREAT_INTELLIGENCE.md) — `KID-TIN-0001`
- [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md) — `KID-INV-0001`
- [Attack Graph Overview](../capabilities/ATTACK_GRAPH_OVERVIEW.md) — `KID-AGR-0001`

### Planned (Stream B)

- `KID-CON-0003` Operational Intelligence Explained
- `KID-GLS-0005` Operational intelligence
- `KID-GLS-0006` Attention point

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md` | Dashboard, attention points, deterministic scoring |
| `docs/current/architecture/ARCHITECTURE_OPERATIONAL_INTELLIGENCE.md` | Reasoning layer and specialist concepts (sanitized) |
| `docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md` | Maturity alignment |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Intelligence PM | Initial domain authority (Stream A) |
