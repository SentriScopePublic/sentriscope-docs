---
title: "Platform Overview"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Product Governance"
technical_reviewer: pending
security_reviewer: pending
ip_reviewer: pending
knowledge_id: KID-PLT-0003
knowledge_domain: platform
knowledge_object: architecture
authority_tier: T2
is_authority: true
authority_document: KID-PLT-0003
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_SYSTEM.md
  - docs/current/architecture/ARCHITECTURE_INDEX.md
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
related_documents:
  - docs/public/platform/WHAT_IS_SENTRISCOPE.md
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
  - docs/public/platform/PRODUCT_MATURITY.md
knowledge_relationships:
  depends_on:
    - KID-PLT-0001
  explains: []
  supersedes: []
  related_to:
    - KID-PLT-0002
    - KID-ARC-0001
    - KID-PLT-0004
  implements: []
  introduces: []
  deprecates: []
  expands: []
navigation:
  personas: [engineer, evaluator, analyst]
  learning_paths: [LP-001, LP-004]
  prerequisites:
    - KID-PLT-0001
  next_reading:
    - KID-ARC-0001
  recommended_reading_order: 3
documentation_health:
  assessed: 2026-07-02
  completeness: 94
  evidence_coverage: 93
  review_completion: 0
  publication_readiness: 77
  review_score: conditional
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md
publication_phase: phase-1
website_slug: platform-overview
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "SentriScope is organized conceptually into ingestion, canonical normalization, intelligence correlation, investigation workflows, and decision support—all tenant-scoped with governance, audit, and read-only AI assistance."
knowledge_tags:
  - platform
  - architecture
  - overview
---

# Platform Overview

## Executive Summary

SentriScope is organized as a **multi-tenant security intelligence platform** with five conceptual layers: **data ingestion**, **canonical normalization**, **intelligence correlation**, **investigation**, and **decision support**. Each layer is **tenant-scoped**. Governance, access control, and auditability apply across the platform. AI assistance operates as a **read-only**, validated layer over existing canonical data—not as an autonomous decision engine.

## Purpose

This document provides a conceptual map of the SentriScope platform for technical readers who need to understand **how capabilities relate** without implementation or internal component detail.

## Problem Statement

Enterprise security platforms are difficult to evaluate when described only as feature lists. A stable conceptual model helps teams understand where ingestion, analysis, investigation, and decision support fit—and where human analysts remain accountable.

## Industry Context

Security platforms typically span ingestion, normalization, analytics, workflow, and reporting. Mature programs expect **tenant isolation**, **auditability**, and **explainable prioritization**—not opaque scores or ungoverned automation.

## SentriScope Perspective

The following **conceptual layers** describe SentriScope at a public-safe level of abstraction (D1). They are **not** internal service names or deployment diagrams.

```text
┌─────────────────────────────────────────────────────────┐
│              Decision Support & Governance               │
│   Risk decisions, overrides, audit, explainability       │
└───────────────────────────┬─────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────┐
│              Investigation & Analyst Workspace           │
│   Evidence, sessions, attack path analysis, collaboration │
└───────────────────────────┬─────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────┐
│              Intelligence Correlation                    │
│   Threat intel, dashboards, CTI enrichment, context      │
└───────────────────────────┬─────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────┐
│              Canonical Normalization                     │
│   Assets, identities, exposures, controls, incidents     │
└───────────────────────────┬─────────────────────────────┘
                            │
┌───────────────────────────▼─────────────────────────────┐
│              Governed Data Ingestion                     │
│   Connectors, health, credential references, provenance  │
└─────────────────────────────────────────────────────────┘
```

### Layer 1 — Governed data ingestion (implemented)

External security sources connect through **governed connector sessions**. Data arrives with operational state tracking and credential handling designed to avoid plaintext secret storage in application data.

### Layer 2 — Canonical normalization (implemented)

Ingested data is normalized into **shared entity concepts**—assets, identities, vulnerabilities, exposures, controls, incidents, and threat intelligence—so analysts work across sources in one tenant-scoped model. See [CANONICAL_DATA_MODEL.md](../architecture/CANONICAL_DATA_MODEL.md).

### Layer 3 — Intelligence correlation (implemented)

Threat intelligence enrichment, dashboard summaries, and correlation capabilities provide context for prioritization and investigation. Specific correlation depth varies by data source and tenant configuration.

### Layer 4 — Investigation and analyst workspace (implemented)

Investigation workflows emphasize **evidence** and analyst-led analysis, including attack path analysis support. Conclusions require human validation.

### Layer 5 — Decision support and governance (implemented)

Deterministic risk prioritization, explainability, override governance, and tamper-evident audit logging support accountable decisions. AI assistance does **not** replace this layer's deterministic scoring.

### Cross-cutting foundations (implemented)

| Foundation | Role |
|------------|------|
| Multi-tenant isolation | Data and access scoped per tenant |
| Role-based access control | Platform and tenant role boundaries |
| Audit logging | Security-relevant actions recorded |
| Read-only AI assistance | Validated queries over canonical data |

## Current Capabilities

| Domain | State | Public summary |
|--------|-------|----------------|
| Connector ingestion | Implemented | Governed sessions from vulnerability, EDR, identity, CMDB/ITSM, and CTI enrichment sources |
| Canonical model | Implemented | Unified entities with provenance |
| Risk prioritization | Implemented | Deterministic scoring with explainability |
| Intelligence dashboard | Implemented | CISO-oriented summaries and CTI context |
| Attack path analysis | Implemented | Investigation support; not autonomous detection |
| Investigation workspace | Implemented | Evidence-first workflows |
| Decision intelligence | Implemented | Risk decision objects and governance |
| Natural language query | Implemented | Guardrailed, read-only |
| Public website knowledge platform | Implemented | Governed publishing workflow (certified) |

## Current Limitations

- This overview is **conceptual**. It intentionally omits deployment topology, internal services, and scaling design.
- **Not every domain** has equal maturity; see [PRODUCT_MATURITY.md](PRODUCT_MATURITY.md).
- **SBOM** data ingestion is supported in part; **dedicated SBOM UI** is partially implemented.
- **Advanced scenario intelligence** and some organizational intelligence themes are **planned** or in progressive rollout.
- **Operational intelligence** and **workforce automation** capabilities exist in the product roadmap with varying maturity—not all are described in this overview.
- Connector count and supported sources should be taken from the **registered connector catalog**, not static marketing figures.

## Frequently Asked Questions

### How is SentriScope deployed?

SentriScope is offered as **multi-tenant SaaS**. Enterprise tenants may use dedicated database isolation depending on plan and configuration (implemented). Deployment internals are not part of public documentation.

### Where does AI fit in the platform?

AI provides **read-only assistance**—primarily natural language querying over canonical data with validation. It does **not** drive deterministic risk scores.

### Does the platform include a public and tenant-facing surface?

Yes. SentriScope separates **public website**, **platform portal**, and **tenant** access surfaces. Only approved public information appears on the public website.

## Related Articles

- [What is SentriScope?](WHAT_IS_SENTRISCOPE.md)
- [What SentriScope is not](WHAT_SENTRISCOPE_IS_NOT.md)
- [Canonical data model](../architecture/CANONICAL_DATA_MODEL.md)
- [Product maturity](PRODUCT_MATURITY.md)
- Planned: `tenant-isolation`, `connector-architecture`, `investigation-workspace` (see [INDEX.md](../INDEX.md))

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_SYSTEM.md` | Platform domains and responsibilities |
| `docs/current/architecture/ARCHITECTURE_INDEX.md` | Domain inventory |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Messaging pillars |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Product Governance | Initial public draft |
