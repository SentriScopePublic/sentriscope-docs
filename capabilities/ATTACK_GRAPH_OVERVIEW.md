---
title: "Attack Graph Overview"
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
knowledge_id: KID-AGR-0001
knowledge_domain: attack-graph
knowledge_object: capability
authority_tier: T5
is_authority: true
authority_document: KID-AGR-0001
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_ATTACK_PATH_INTELLIGENCE.md
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
  - docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md
related_documents:
  - docs/public/investigations/INVESTIGATION_WORKSPACE.md
  - docs/public/intelligence/THREAT_INTELLIGENCE.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
knowledge_relationships:
  depends_on:
    - KID-PLT-0001
    - KID-ARC-0001
    - KID-INV-0001
  explains: []
  supersedes: []
  related_to:
    - KID-TIN-0001
    - KID-OIN-0001
  implements: []
  introduces: []
  deprecates: []
  expands:
    - KID-PLT-0003
navigation:
  personas: [analyst, engineer, ciso]
  learning_paths: [LP-002]
  prerequisites:
    - KID-PLT-0001
    - KID-ARC-0001
    - KID-INV-0001
  next_reading:
    - KID-TIN-0001
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md#kid-agr-0001--attack-graph-overview
publication_phase: stream-a
website_slug: attack-graph-overview
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "SentriScope attack path intelligence helps analysts understand multi-hop relationships among assets, identities, exposures, and threat context—ranking paths and entities for investigation support without autonomous detection or replacing deterministic risk scoring."
knowledge_tags:
  - attack-graph
  - attack-path
  - intelligence
  - capability
---

# Attack Graph Overview

## Industry Problem

Security teams see thousands of vulnerabilities and alerts but struggle to answer structural questions: *If this entry point is compromised, what can be reached?* *Which identity or asset connects two critical systems?* *Is this finding part of a plausible attack chain?*

Point-in-time severity scores alone do not expose **relationship context**—how exposures, identities, applications, and threat indicators connect across the environment.

## Why the Problem Exists

Security data arrives from siloed tools with incompatible relationship models. Manual graphing in spreadsheets or generic diagramming tools does not scale, lacks provenance, and falls out of date after the next scan cycle.

Attack path analysis emerged to model **feasible movement** through an environment using assets, identities, network reachability, vulnerabilities, and controls—but products vary widely in whether they show pretty graphs or actionable, explainable prioritization.

## Traditional Approaches

| Approach | Limitation |
|----------|------------|
| CVSS-only prioritization | Ignores reachability and business context |
| Manual attack trees | Not maintained at scale |
| Generic graph visualization | Often lacks tenant governance and evidence linkage |
| Penetration test reports | Point-in-time; not continuous |
| Threat intel feeds alone | Indicators without environmental placement |

Effective programs combine **deterministic relationship analysis** with **analyst-led investigation**—paths support decisions; they do not replace them.

## SentriScope Perspective

SentriScope provides **attack path intelligence** as an investigation and prioritization capability (implemented). Public documentation uses *attack graph* language for familiarity; the product emphasis is **paths, entities, and explainability**—not unbounded graph exploration as an end in itself.

Design center questions the capability helps answer:

| Question | Role of attack path intelligence |
|----------|----------------------------------|
| Which entities matter most in this snapshot? | Priority lists and high-risk entity context |
| What multi-hop chains exist between entities? | Path traversal with confidence thresholds |
| What could be reached from a compromise? | Blast radius and reachability summaries |
| Why is this path ranked highly? | Explainability tied to canonical inputs |
| What should I investigate first? | Feeds investigation workspace context—not autonomous closure |

**Important boundaries:**

- Attack path intelligence **does not** implement a second proprietary risk engine; deterministic risk scoring remains separate. See [KID-PLT-0001](../platform/WHAT_IS_SENTRISCOPE.md).
- Paths provide **evidence for investigation** within [KID-INV-0001](../investigations/INVESTIGATION_WORKSPACE.md); this document **does not define** investigation methodology.
- Threat intelligence correlation enriches context; traversal rules differ for certain intelligence edge types. Detail: [KID-TIN-0001](../intelligence/THREAT_INTELLIGENCE.md).
- Longer-term **scenario-centric prioritization** themes are on the product roadmap—not all are generally available. Status: [KID-PLT-0004](../platform/PRODUCT_MATURITY.md).

Entity types referenced are canonical concepts—assets, identities, applications, exposures, vulnerabilities, incidents, and threat intelligence indicators—defined in [KID-ARC-0001](../architecture/CANONICAL_DATA_MODEL.md).

## Current Product Capability

| Capability | State | Summary |
|------------|-------|---------|
| Snapshot-based relationship analysis | Implemented | Point-in-time view aligned with risk calculation cycles |
| Multi-hop path discovery | Implemented | Configurable confidence thresholds for traversable steps |
| Priority lists and high-risk entity context | Implemented | Supports operator triage entry points |
| Blast radius and reachability summaries | Implemented | Structural impact narrative for investigation |
| Path explainability | Implemented | Deterministic explanations over canonical inputs |
| Investigation UI integration | Implemented | Attack intelligence on key entity types during investigation |
| Read-only natural language query over paths | Implemented | Guardrailed assistance; not in scoring path |
| Scenario-centric primary queue | Planned / progressive | Longer-term prioritization evolution |
| Autonomous attack detection | Not available | Analyst interpretation required |

## Current Limitations

- Analysis is **snapshot-bound**—results reflect materialization time, not live network state.
- Path confidence and traversal rules produce **hypotheses**, not proof of exploitation.
- Not every relationship type in the environment may be populated; connector coverage affects graph completeness. See [KID-INT-0001](../integrations/SUPPORTED_DATA_SOURCES.md).
- Advanced scenario intelligence capabilities are **planned or in progressive rollout**; public documentation of scenario queues is incomplete.
- This overview intentionally omits graph construction algorithms, internal edge taxonomies, and API contracts.

## Common Questions

### Is the attack graph a standalone visualization product?

No. It supports investigation and prioritization within SentriScope's intelligence and decision workflow—not generic graph drawing.

### Does SentriScope prove attackers can traverse a path?

No. Paths are deterministic analyses over integrated data with stated confidence. Analysts validate relevance during investigation.

### How does this relate to MITRE ATT&CK?

MITRE ATT&CK provides a technique framework; SentriScope correlates environmental relationships and canonical findings. Public technique mapping depth varies by deployment data.

### Does attack path intelligence replace vulnerability scanning?

No. Scanners and assessments feed exposures; attack path intelligence contextualizes relationships among normalized findings.

## Related Concepts

### Prerequisites

- [What is SentriScope?](../platform/WHAT_IS_SENTRISCOPE.md) — `KID-PLT-0001`
- [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md) — `KID-ARC-0001`
- [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md) — `KID-INV-0001`

### See also

- [Threat Intelligence](../intelligence/THREAT_INTELLIGENCE.md) — `KID-TIN-0001`
- [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md) — `KID-OIN-0001`

### Planned (Stream B)

- `KID-CON-0002` Understanding Attack Paths
- `KID-GLS-0003` Attack path
- `KID-GLS-0004` Attack scenario

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_ATTACK_PATH_INTELLIGENCE.md` | Product capability scope, operator questions, maturity (sanitized) |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Messaging boundaries |
| `docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md` | Implemented vs planned alignment |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Intelligence PM | Initial domain authority (Stream A) |
