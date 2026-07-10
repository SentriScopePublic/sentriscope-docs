---
title: "What is SentriScope?"
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
knowledge_id: KID-PLT-0001
knowledge_domain: platform
knowledge_object: reference
authority_tier: T0
is_authority: true
authority_document: KID-PLT-0001
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_SYSTEM.md
  - docs/current/architecture/ARCHITECTURE_INDEX.md
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
  - docs/current/operations/manual/operator/pages/RUNBOOK_OPERATOR_WHAT_IS_SENTRISCOPE.md
related_documents:
  - docs/public/platform/WHAT_SENTRISCOPE_IS_NOT.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
  - docs/public/platform/PRODUCT_MATURITY.md
knowledge_relationships:
  depends_on: []
  explains: []
  supersedes: []
  related_to:
    - KID-PLT-0002
    - KID-PLT-0003
    - KID-ARC-0001
    - KID-PLT-0004
  implements: []
  introduces: []
  deprecates: []
  expands: []
navigation:
  personas: [evaluator, engineer, analyst, llm, public]
  learning_paths: [LP-001]
  recommended_reading_order: 1
documentation_health:
  assessed: 2026-07-02
  completeness: 95
  evidence_coverage: 95
  review_completion: 0
  publication_readiness: 78
  review_score: conditional
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md
publication_phase: phase-1
website_slug: what-is-sentriscope
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "SentriScope is a multi-tenant security intelligence platform that normalizes security data from governed connectors, correlates risk and threat context, and supports analyst-led investigation and decision workflows with evidence-driven, read-only AI assistance."
knowledge_tags:
  - platform
  - overview
  - product
---

# What is SentriScope?

## Executive Summary

SentriScope is a **security intelligence platform** for enterprise security teams. It consolidates security data from multiple sources into a **canonical data model**, supports **deterministic risk prioritization**, and provides **investigation and intelligence workflows** where analysts remain in control. The platform is **multi-tenant by design**, with tenant isolation, role-based access, and audit logging as architectural foundations. AI assistance is **read-only**, schema-grounded, and **not** used in the deterministic risk-scoring path.

## Purpose

This document defines SentriScope for engineers, analysts, partners, investors, and automated systems that need an accurate, evidence-based description of the platform without implementation detail.

## Problem Statement

Security teams operate across many tools—vulnerability scanners, endpoint detection, identity systems, threat intelligence feeds, and IT service management platforms. Each tool uses its own data format and context. Analysts spend significant time reconciling sources, prioritizing findings, and building investigation context before they can act. SentriScope addresses fragmentation by normalizing data and supporting governed analysis in one tenant-scoped environment.

## Industry Context

Modern security operations rely on correlated visibility across assets, vulnerabilities, identities, exposures, incidents, and threat intelligence. Industry frameworks such as MITRE ATT&CK and common prioritization inputs (for example CVSS, EPSS, and known-exploited vulnerability catalogs) help teams reason about risk, but tools rarely present a unified, tenant-governed model for analysis and decision support.

## SentriScope Perspective

SentriScope is designed as a **Cyber Risk Intelligence Platform** (implemented). It provides:

- **Canonical data normalization** — Security telemetry from connectors is normalized into shared entity concepts regardless of source (implemented).
- **Risk-based prioritization** — Deterministic, explainable risk scoring over canonical data (implemented).
- **Intelligence-driven correlation** — Attack path analysis, threat intelligence correlation, and assessment-related workflows (implemented; some advanced scenario capabilities remain on a longer-term roadmap).
- **AI-augmented query** — Natural language querying over canonical data with validation and guardrails (implemented; tenant-configurable).
- **Connector ecosystem** — Governed ingestion from vulnerability scanners, endpoint platforms, identity sources, CMDB/ITSM, and threat intelligence enrichment providers (implemented).

SentriScope is **analyst-assisted**, not autonomous. Investigations, conclusions, and governance decisions require human validation.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Multi-tenant SaaS platform | Implemented | Tenant-scoped data and access; shared or dedicated database deployment options for enterprise tenants |
| Canonical data normalization | Implemented | Assets, vulnerabilities, identities, exposures, controls, incidents, and threat intelligence represented in a unified model |
| Governed connector ingestion | Implemented | Connector sessions with health monitoring and encrypted credential references |
| Deterministic risk scoring | Implemented | Explainable prioritization; LLM is not in the critical scoring path |
| Intelligence dashboard and CTI correlation | Implemented | Threat intelligence enrichment and correlation capabilities |
| Attack path analysis | Implemented | Supports investigation-oriented path analysis; analyst interpretation required |
| Investigation and evidence workflows | Implemented | Evidence-first investigation support |
| Natural language query (guardrailed) | Implemented | Read-only assistance over canonical data |
| Tamper-evident audit logging | Implemented | Security-relevant actions recorded |
| Public knowledge publishing platform | Implemented | Governed public documentation workflow (certified) |

## Current Limitations

- SentriScope **does not** autonomously detect or respond to all security events; analyst validation remains required.
- SentriScope **is not** a replacement for a SIEM, SOAR platform, or dedicated vulnerability scanner—see [WHAT_SENTRISCOPE_IS_NOT.md](WHAT_SENTRISCOPE_IS_NOT.md).
- **SBOM-related ingestion** exists at the data layer; dedicated SBOM user interface capabilities are **partially implemented**.
- **ITSM ticket creation** integrations exist but may be **disabled by default** per tenant configuration.
- Some **advanced scenario and organizational intelligence** capabilities are **planned** or in progressive rollout—not all are generally available.
- SentriScope is **not open source**.
- This public knowledge library is **published progressively**; not every capability has a public page yet.

## Frequently Asked Questions

### Is SentriScope a SIEM?

No. SentriScope normalizes and correlates security data and supports analyst-led investigation and risk decisions. It may complement SIEM and other tools rather than replace them. See [WHAT_SENTRISCOPE_IS_NOT.md](WHAT_SENTRISCOPE_IS_NOT.md).

### Does SentriScope use AI to score risk automatically?

Risk scoring is **deterministic**. AI assistance supports read-only querying and analysis workflows and is **not** in the critical risk-scoring path.

### Is SentriScope multi-tenant?

Yes. Multi-tenancy and tenant isolation are architectural foundations (implemented).

### Who is SentriScope for?

Security operations, vulnerability management, threat intelligence, and risk teams that need consolidated, tenant-governed visibility and investigation support.

## Related Articles

- [What SentriScope is not](WHAT_SENTRISCOPE_IS_NOT.md)
- [Platform overview](PLATFORM_OVERVIEW.md)
- [Canonical data model](../architecture/CANONICAL_DATA_MODEL.md)
- [Product maturity](PRODUCT_MATURITY.md)
- Planned: `llm-guardrails`, `ai-limitations` (see [INDEX.md](../INDEX.md))

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_SYSTEM.md` | Platform purpose, capability areas, multi-tenant design |
| `docs/current/architecture/ARCHITECTURE_INDEX.md` | Domain map confirmation |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Messaging pillars and safe boundaries |
| `docs/current/operations/manual/operator/pages/RUNBOOK_OPERATOR_WHAT_IS_SENTRISCOPE.md` | High-level operator workflow alignment |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Product Governance | Initial public draft |
