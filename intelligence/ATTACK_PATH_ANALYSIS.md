---
title: "Attack Path Analysis"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Intelligence PM"
technical_reviewer: pending
security_reviewer: n/a
ip_reviewer: pending
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_ATTACK_PATH_INTELLIGENCE.md
  - docs/current/architecture/ARCHITECTURE_ATTACK_GRAPH.md
related_documents:
  - docs/public/capabilities/ATTACK_GRAPH_OVERVIEW.md
  - docs/public/intelligence/INTELLIGENCE_CORRELATION.md
  - docs/public/investigations/INVESTIGATION_WORKSPACE.md
  - docs/public/glossary/ATTACK_PATH.md
publication_phase: phase_2
website_slug: attack-path-analysis
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "Attack path analysis in SentriScope models plausible multi-hop relationships among assets, identities, exposures, and threat context to support investigation and prioritization—without autonomous exploitation or replacing deterministic risk scoring."
knowledge_tags:
  - attack-path
  - investigation
  - prioritization
  - intelligence
---

# Attack Path Analysis

## Executive Summary

**Attack path analysis** helps security teams understand how an adversary might move through an environment by relating assets, identities, exposures, network reachability, and threat context. SentriScope provides **attack path intelligence** as **investigation and prioritization support** (implemented)—not autonomous penetration testing or unsupervised blocking. Analysts interpret paths; the platform surfaces explainable relationships.

## Purpose

Clarify what attack path analysis means in SentriScope, how it differs from vulnerability lists alone, and what outcomes teams should expect—complementing [Attack graph overview](../capabilities/ATTACK_GRAPH_OVERVIEW.md) with Phase 2 public knowledge framing.

## Problem Statement

Individual critical vulnerabilities do not reveal **structural** risk: reachable identities, lateral movement options, or choke points between an entry exposure and a critical asset. Teams need relationship-aware analysis that stays current as ingestion updates the environment.

## Industry Context

Attack path analysis emerged from graph-based security modeling, red team reporting, and exposure management programs. Products vary between visualization-heavy graphs and actionable, ranked paths tied to remediation workflows. Mature use ties paths to **evidence** and **human validation**.

## SentriScope Perspective

SentriScope attack path analysis focuses on:

| Theme | Description |
|-------|-------------|
| **Multi-hop relationships** | Paths connect entities across hops—not isolated findings |
| **Environmental grounding** | Paths use tenant canonical data ingested through governed connectors |
| **Threat context** | Intelligence correlation may inform which paths matter now |
| **Explainability** | Analysts can reason about why a path is surfaced |
| **Investigation alignment** | Paths support hypotheses in investigation workspaces |
| **Non-autonomous** | No unattended exploitation or response actions |

Public documentation may use **attack graph** language for familiarity; product emphasis is **paths, entities, and decision support**.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Attack path intelligence module | Implemented | Relationship analysis for prioritization and investigation |
| Entity relationship context | Implemented | Assets, identities, exposures linked in analysis views |
| Integration with investigations | Implemented | Paths support analyst-led workflows |
| Threat intelligence linkage | Partial | Depth varies with correlated intelligence quality |
| Advanced attack scenarios | Planned / progressive | Some scenario capabilities on longer-term roadmap |
| Autonomous exploitation | Not offered | Analysis only |

## Current Limitations

- Paths reflect **modeled relationships** from available data—not guaranteed real-world exploit chains.
- **Incomplete asset or identity inventory** produces incomplete paths.
- **Network topology accuracy** depends on ingested network and cloud context.
- Graph visualization can **overwhelm** without prioritization filters—analyst judgment required.
- Attack path analysis does **not** replace formal penetration tests or red team engagements.

## Frequently Asked Questions

### Is attack path analysis the same as attack surface management?

Related but distinct. Attack surface management emphasizes reachable exposures; path analysis emphasizes **chains** and **movement** between entities.

### Does SentriScope automatically hack my systems to validate paths?

No. Analysis is **data-driven** from authorized ingestion—not live exploitation.

### How do paths interact with risk scores?

Paths inform **context** for prioritization and investigation. Deterministic scoring remains separate; see [Risk scoring approach](RISK_SCORING_APPROACH.md).

### Where should I start learning more?

See [Attack graph overview](../capabilities/ATTACK_GRAPH_OVERVIEW.md) and [Investigation workspace](../investigations/INVESTIGATION_WORKSPACE.md).

## Related Articles

- [Attack graph overview](../capabilities/ATTACK_GRAPH_OVERVIEW.md)
- [Intelligence correlation](INTELLIGENCE_CORRELATION.md)
- [Risk scoring approach](RISK_SCORING_APPROACH.md)
- [Investigation workspace](../investigations/INVESTIGATION_WORKSPACE.md)
- [Glossary: Attack path](../glossary/ATTACK_PATH.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_ATTACK_PATH_INTELLIGENCE.md` | Attack path capability scope (sanitized) |
| `docs/current/architecture/ARCHITECTURE_ATTACK_GRAPH.md` | Graph and path concepts (sanitized) |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | Intelligence PM | Phase 2 initial draft |
