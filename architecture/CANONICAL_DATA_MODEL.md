---
title: "Canonical Data Model"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Product Governance"
technical_reviewer: pending
security_reviewer: n/a
ip_reviewer: pending
knowledge_id: KID-ARC-0001
knowledge_domain: architecture
knowledge_object: architecture
authority_tier: T3
is_authority: true
authority_document: KID-ARC-0001
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_DATA.md
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
related_documents:
  - docs/public/platform/WHAT_IS_SENTRISCOPE.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
  - docs/public/platform/PRODUCT_MATURITY.md
knowledge_relationships:
  depends_on:
    - KID-PLT-0001
    - KID-PLT-0003
  explains: []
  supersedes: []
  related_to:
    - KID-PLT-0004
  implements: []
  introduces: []
  deprecates: []
  expands:
    - KID-PLT-0003
navigation:
  personas: [engineer, partner, evaluator]
  learning_paths: [LP-001, LP-004]
  prerequisites:
    - KID-PLT-0001
    - KID-PLT-0003
  recommended_reading_order: 4
documentation_health:
  assessed: 2026-07-02
  completeness: 92
  evidence_coverage: 95
  review_completion: 0
  publication_readiness: 72
  review_score: conditional
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md
publication_phase: phase-1
website_slug: canonical-data-model
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "SentriScope normalizes security data into canonical concepts—asset, identity, application, exposure, vulnerability, incident, threat intelligence, evidence, and risk—with tenant scope and provenance, without requiring analysts to reconcile proprietary source formats."
knowledge_tags:
  - architecture
  - data-model
  - canonical
---

# Canonical Data Model

## Executive Summary

SentriScope structures security information into **canonical concepts**—shared entity types that represent assets, identities, applications, exposures, vulnerabilities, incidents, threat intelligence, evidence, and risk—regardless of which connector or tool produced the original data. Every canonical entity is **tenant-scoped** and designed to carry **provenance** so analysts understand where data originated. This document describes **concepts only**, not database schemas or field definitions.

## Purpose

Readers need a stable vocabulary for how SentriScope represents security data publicly—especially for LLM grounding, partner integration discussions, and technical due diligence—without exposure of internal schema design.

## Problem Statement

Security tools export incompatible formats. Analysts manually map "the same" asset or vulnerability across scanners, CMDB records, and incident tickets. Without normalization, prioritization and investigation remain source-specific and error-prone.

## Industry Context

Canonical models appear in many domains: configuration management databases, vulnerability management platforms, and security data lakes all attempt entity resolution and normalization. Effective models separate **what the entity means** from **how a vendor formatted the export**.

## SentriScope Perspective

SentriScope is designed as a **Cyber Risk Intelligence Platform**, not merely a vulnerability aggregator (implemented). Data from scanners, identity systems, threat feeds, ITSM tools, and other connectors is normalized into layered canonical concepts.

### Core entity concepts

| Concept | Public definition |
|---------|-------------------|
| **Asset** | A physical, virtual, or cloud resource relevant to security analysis |
| **Identity** | A user or service identity from directory, identity provider, or HR-aligned sources |
| **Application** | A business application with optional business-impact context |
| **Exposure** | A security finding linking an asset (or related entity) to a vulnerability or exposure condition |
| **Vulnerability** | A normalized vulnerability record (for example CVE-aligned or vendor-specific identifiers) |
| **Incident** | A normalized security incident or major event from operational tools |
| **Threat intelligence** | Indicators, actors, campaigns, or enrichment context from CTI sources |
| **Control** | A security control definition and its implementation/coverage against assets |
| **Evidence** | Material supporting an investigation conclusion, with governance and provenance |
| **Risk** | Prioritized risk outcomes derived deterministically from canonical inputs |

### Conceptual relationships (not a schema)

At a high level:

- **Assets** and **identities** anchor much of the model.
- **Applications** provide business context for assets and identities.
- **Vulnerabilities** and **exposures** connect findings to assets.
- **Incidents** and **threat intelligence** provide operational and CTI context.
- **Controls** describe defensive coverage.
- **Evidence** supports **investigation** workflows.
- **Risk** summarizes prioritized outcomes for decision support.

Exact relationship cardinality and internal representation are **not** part of public documentation.

### Architectural layers (conceptual)

Public-safe layering mirrors the internal data architecture at concept level only:

| Layer | Concepts (examples) |
|-------|---------------------|
| Foundation | Tenant scope, access, audit |
| Asset and identity | Asset, identity, application, business context |
| Threat and assessment | Assessment findings, incidents, monitoring events |
| Control and coverage | Control, implementation, coverage |
| Exposure | Vulnerability, exposure, credential leak records |
| Threat actor | Threat actors, campaigns, indicators |
| Ingestion | Connector sessions (governed), source provenance |
| Risk | Risk snapshots, explainability outputs |
| Intelligence | Threat intel items, feeds, enrichment |

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Canonical normalization across connectors | Implemented | Multiple entity types normalized from governed ingestion |
| Tenant-scoped entities | Implemented | All business entities attributed to a tenant |
| Provenance on canonical data | Implemented | Source lineage concepts supported |
| Deterministic risk over canonical data | Implemented | Scoring uses canonical inputs |
| Business impact context | Implemented | Applications and business units supported conceptually |
| Reference data (CVE, MITRE, etc.) | Implemented | Platform-shared reference datasets |
| Schema-grounded LLM queries | Implemented | Read-only queries over canonical data |

## Current Limitations

- This document **does not** define tables, fields, JSON schemas, or API payloads.
- **SBOM components** exist in the data model at some depth; **operator-facing SBOM UI** is partially implemented.
- Not every connector populates every entity type; population depends on source capability.
- **Evidence** governance includes advanced quality and trust dimensions in the product; public documentation of every evidence subtype is **not yet complete**.
- Entity resolution edge cases (duplicate assets across sources) require analyst and system governance; perfect automatic merging is **not** claimed.

## Frequently Asked Questions

### Is the canonical model the same as a CMDB?

No. The canonical model is optimized for **security risk and investigation context**, not full IT asset management. CMDB connectors may **feed** asset data.

### Does SentriScope store raw vendor data?

SentriScope normalizes data into canonical concepts while retaining provenance to sources. Raw retention policies are **not** described in public documentation.

### Can partners extend the canonical model?

Partner integrations typically use governed connector and API patterns. Extension mechanics are **partner-classification** topics, not covered in this public page.

## Related Articles

- [What is SentriScope?](WHAT_IS_SENTRISCOPE.md)
- [Platform overview](../platform/PLATFORM_OVERVIEW.md)
- [Product maturity](../platform/PRODUCT_MATURITY.md)
- Planned: `connector-architecture`, `risk-scoring-approach`, `supported-data-sources` (see [INDEX.md](../INDEX.md))

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Layer purposes and entity concepts (sanitized) |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Pillar 1 proof points and safe boundaries |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Product Governance | Initial public draft |
