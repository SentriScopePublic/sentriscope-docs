---
title: "Governed Ingestion"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Integrations PM"
technical_reviewer: pending
security_reviewer: pending
ip_reviewer: pending
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_CONNECTORS.md
  - docs/current/architecture/ARCHITECTURE_DATA.md
related_documents:
  - docs/public/integrations/CONNECTOR_ARCHITECTURE.md
  - docs/public/integrations/SUPPORTED_DATA_SOURCES.md
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
  - docs/public/glossary/PROVENANCE.md
publication_phase: phase_2
website_slug: governed-ingestion
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "Governed ingestion in SentriScope means security data enters the platform through authorized connector sessions with tenant scope, credential protection, provenance, and health visibility—not uncontrolled imports or manual spreadsheet uploads as the primary model."
knowledge_tags:
  - integrations
  - ingestion
  - governance
  - provenance
---

# Governed Ingestion

## Executive Summary

**Governed ingestion** is how security data enters SentriScope: through **authorized connector sessions** that enforce tenant scope, protect credentials, normalize records into the canonical model, and preserve **provenance**. Governed ingestion is the primary path for operational data (implemented). Ad hoc imports, where available, follow separate controls and are not the default enterprise pattern.

## Purpose

Distinguish SentriScope's ingestion philosophy from informal data loading—helping teams understand why governance, provenance, and health matter for trustworthy prioritization and investigations.

## Problem Statement

Uncontrolled imports produce duplicate assets, untraceable findings, and stale intelligence. Without governance, analysts cannot answer basic audit questions: *Who authorized this data?* *When was it last synced?* *Which source should we trust when records conflict?*

## Industry Context

Security data lakes often accumulate exports without normalization. Operational platforms increasingly require **idempotent upsert**, **source attribution**, and **operational visibility** as prerequisites for risk programs—not optional nice-to-haves.

## SentriScope Perspective

Governed ingestion principles in SentriScope:

| Principle | Meaning |
|-----------|---------|
| **Authorization** | Only configured connector sessions with valid credentials ingest data |
| **Tenant scope** | Ingested records belong to one tenant |
| **Normalization** | Source formats map to canonical entity concepts |
| **Provenance** | Origin source and sync context are retained for analysis |
| **Health visibility** | Administrators monitor success, failure, and staleness |
| **Idempotent behavior** | Repeated syncs refine state rather than uncontrolled duplication (conceptual—per connector behavior) |

Governed ingestion supports **downstream correlation**, **risk prioritization**, and **investigations** because records are explainable. It does **not** imply SentriScope validates every finding as true—source quality still matters.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Connector-based primary ingestion | Implemented | Standard path for vulnerability, endpoint, identity, and related sources |
| Provenance on canonical records | Implemented | Analysts can reason about source origin |
| Import frameworks for structured loads | Partial | Additional import paths may exist for specific domains; connector sessions remain primary |
| Health and error surfacing | Implemented | Session status visible to administrators |
| Tenant-isolated credential storage | Implemented | Integration secrets protected per tenant |

## Current Limitations

- **Manual CSV uploads**, if supported for specific modules, are not equivalent to full connector governance unless documented for that workflow.
- SentriScope does **not** automatically resolve all cross-source conflicts; analysts may need to reconcile contradictory upstream data.
- **Historical backfill depth** depends on upstream API retention and connector configuration.
- Ingestion does **not** include unauthorized scanning of customer networks—customers must provision access.
- Real-time vs batch latency varies; governed does not always mean instantaneous.

## Frequently Asked Questions

### Can I email exports to SentriScope for ingestion?

Operational ingestion is designed around **connector sessions** and governed import paths—not informal email channels.

### Does governed ingestion deduplicate assets automatically?

Normalization and upsert semantics reduce uncontrolled duplication, but conflicting identifiers across sources may still require analyst review depending on upstream quality.

### How does ingestion relate to threat intelligence?

Base connectors feed canonical operational data. **Threat intelligence enrichment** follows related lifecycle patterns described in [Threat intelligence](../intelligence/THREAT_INTELLIGENCE.md).

### Is ingestion audited?

Security-relevant configuration and operational actions are recorded under the platform audit model. See [Platform security boundaries](../security/PLATFORM_SECURITY_BOUNDARIES.md).

## Related Articles

- [Connector architecture](CONNECTOR_ARCHITECTURE.md)
- [Supported data sources](SUPPORTED_DATA_SOURCES.md)
- [Canonical data model](../architecture/CANONICAL_DATA_MODEL.md)
- [Glossary: Provenance](../glossary/PROVENANCE.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_CONNECTORS.md` | Ingestion governance (sanitized) |
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Canonical entity normalization |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | Integrations PM | Phase 2 initial draft |
