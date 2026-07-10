---
title: "Intelligence Correlation"
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
  - docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md
  - docs/current/architecture/ARCHITECTURE_DATA.md
related_documents:
  - docs/public/intelligence/THREAT_INTELLIGENCE.md
  - docs/public/intelligence/OPERATIONAL_INTELLIGENCE.md
  - docs/public/intelligence/RISK_SCORING_APPROACH.md
  - docs/public/glossary/CORRELATION.md
publication_phase: phase_2
website_slug: intelligence-correlation
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "Intelligence correlation in SentriScope links threat and operational context to canonical assets, exposures, and investigations—so analysts prioritize and investigate with environmental relevance, not isolated feed volume."
knowledge_tags:
  - intelligence
  - correlation
  - threat-intelligence
  - operational-intelligence
---

# Intelligence Correlation

## Executive Summary

**Intelligence correlation** connects threat intelligence, operational signals, and canonical security entities—assets, exposures, identities, and investigations—within a tenant boundary. Correlation answers whether intelligence **matters here**, not merely whether an indicator exists globally. Correlation capabilities are **implemented** with analyst validation expected for high-impact decisions.

## Purpose

Describe how SentriScope relates external and internal intelligence to environmental context—supporting evaluation of CTI programs, SOC workflows, and prioritization without exposing correlation algorithms or internal graph storage.

## Problem Statement

Threat feeds and alert streams grow faster than validation capacity. Without correlation to owned assets and active exposures, intelligence becomes noise. Without operational linkage, threat reports rarely change daily triage outcomes.

## Industry Context

Effective intelligence programs emphasize **lifecycle management** (ingest, validate, enrich, correlate, consume) and **fusion** with vulnerability and asset context. Correlation is distinct from aggregation: fusion requires entity resolution and provenance.

## SentriScope Perspective

SentriScope correlation layers include:

| Input | Correlation intent |
|-------|-------------------|
| **Threat intelligence** | Indicators, actors, campaigns linked to tenant entities when validated |
| **Operational intelligence** | Security operations context that informs prioritization and response readiness |
| **Canonical exposures** | Environmental placement of vulnerabilities and misconfigurations |
| **Investigations** | Active analyst context where intelligence supports hypotheses |

Correlation is **tenant-scoped** and **provenance-aware**. It supports [risk scoring](RISK_SCORING_APPROACH.md) and [investigation workflows](../investigations/INVESTIGATION_WORKSPACE.md) but does **not** autonomously block traffic or close incidents.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Threat intelligence lifecycle and fusion | Implemented | Governed CTI states with asset and exposure linkage |
| Operational intelligence modules | Implemented | Operational context for security decisions |
| Canonical entity linkage | Implemented | Intelligence related to normalized assets and exposures |
| Intelligence dashboard views | Implemented | Analyst-facing correlation surfaces |
| Enrichment provider catalog | Implemented | Separate from base connector catalog where applicable |
| Analyst validation workflows | Implemented | Human judgment required for consequential actions |

## Current Limitations

- Correlation quality depends on **ingestion completeness** and upstream data accuracy.
- **False positives** remain possible when indicators are stale or context is incomplete.
- Not every global campaign automatically maps to your environment.
- **Autonomous blocking** based on correlated intelligence is **not** the default product posture.
- Advanced scenario modeling may be **partial** or on a longer-term roadmap.

## Frequently Asked Questions

### Is correlation the same as a SIEM correlation rule?

SIEM rules often pattern-match events. SentriScope correlation emphasizes **canonical entity linkage** and intelligence lifecycle integration across security data domains—not replacing SIEM.

### Does correlation replace threat intelligence analysts?

No. Analysts validate relevance, tune sources, and decide operational response.

### How does correlation affect prioritization?

Correlated threat context may **influence deterministic prioritization** when governed rules include intelligence signals. See [Risk scoring approach](RISK_SCORING_APPROACH.md).

### What is the difference between threat and operational intelligence?

See [Threat intelligence](THREAT_INTELLIGENCE.md) and [Operational intelligence](OPERATIONAL_INTELLIGENCE.md).

## Related Articles

- [Threat intelligence](THREAT_INTELLIGENCE.md)
- [Operational intelligence](OPERATIONAL_INTELLIGENCE.md)
- [Risk scoring approach](RISK_SCORING_APPROACH.md)
- [Attack path analysis](ATTACK_PATH_ANALYSIS.md)
- [Glossary: Correlation](../glossary/CORRELATION.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md` | Intelligence correlation domain (sanitized) |
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Canonical linkage concepts |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | Intelligence PM | Phase 2 initial draft |
