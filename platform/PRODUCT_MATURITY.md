---
title: "Product Maturity"
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
knowledge_id: KID-PLT-0004
knowledge_domain: maturity
knowledge_object: maturity
authority_tier: T4
is_authority: true
authority_document: KID-PLT-0004
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/certification/CERTIFICATION_PUBLIC_WEBSITE_PHASE3A.md
  - docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md
  - docs/current/architecture/ARCHITECTURE_SYSTEM.md
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
related_documents:
  - docs/public/platform/WHAT_IS_SENTRISCOPE.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
  - docs/public/platform/WHAT_SENTRISCOPE_IS_NOT.md
knowledge_relationships:
  depends_on:
    - KID-PLT-0001
    - KID-PLT-0003
  explains: []
  supersedes: []
  related_to:
    - KID-PLT-0002
    - KID-ARC-0001
  implements: []
  introduces: []
  deprecates: []
  expands: []
navigation:
  personas: [investor, evaluator, ciso]
  learning_paths: [LP-001]
  prerequisites:
    - KID-PLT-0001
  recommended_reading_order: 5
documentation_health:
  assessed: 2026-07-02
  completeness: 96
  evidence_coverage: 100
  review_completion: 0
  publication_readiness: 78
  review_score: conditional
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md
publication_phase: phase-1
website_slug: product-maturity
last_updated: 2026-07-02
next_review: 2026-09-02
llm_summary: "SentriScope is a production multi-tenant security intelligence platform with broad implemented capabilities, honestly partial areas including SBOM UI and some ITSM defaults, a certified public knowledge publishing platform, and progressive public documentation."
knowledge_tags:
  - platform
  - maturity
  - investors
---

# Product Maturity

## Executive Summary

SentriScope is a **production-grade, multi-tenant security intelligence platform** with substantial implemented capability across canonical data normalization, connector ingestion, risk prioritization, threat intelligence, attack path analysis, investigation workflows, and guardrailed AI assistance. Maturity is **not uniform** across every module: some areas are **partially implemented** or **disabled by default**, and public documentation is **being published progressively**. The **public website knowledge publishing platform** has completed Phase 3A certification. This document does **not** claim market leadership, customer counts, revenue, or unsupported performance benchmarks.

## Purpose

Investors, partners, and technical evaluators need an **honest maturity statement** aligned with evidence—not marketing superlatives.

## Problem Statement

Due diligence fails when maturity is overstated. Teams need a single public reference for what is **implemented**, **partial**, or **planned**, and what evidence supports those statements.

## Industry Context

Enterprise security platforms typically ship incrementally: core data models and integrations mature first; specialized UIs and advanced automation follow. Transparent maturity reporting is expected in technical evaluations even when marketing pages emphasize breadth.

## SentriScope Perspective

### Platform maturity — overall (implemented)

SentriScope operates as a **multi-tenant SaaS** platform with tenant isolation, role-based access control, audit logging, and governed connector ingestion (implemented). Core domains include canonical data, intelligence dashboards, decision intelligence, attack path analysis, LLM-assisted read-only query, and investigation support (implemented).

### Public knowledge publishing platform (implemented, certified)

The Public Website Intelligence Platform—the governed system for publishing public knowledge—**passed Phase 3A certification** with full category scores across architecture, governance, security, provenance, public API, and AI pipeline boundaries (implemented). This supports the progressive publication of the public knowledge library described in this repository.

**Evidence summary:** Internal certification report records PASSED status and production-readiness recommendation for Phase 3B foundation work—not a claim about overall company revenue or customer scale.

### Capability maturity matrix

| Area | Maturity | Notes |
|------|----------|-------|
| Multi-tenant platform and isolation | Implemented | Architectural foundation |
| Canonical data normalization | Implemented | Broad entity coverage |
| Governed connector ingestion | Implemented | Registered connector types in platform catalog |
| Deterministic risk prioritization | Implemented | CVSS/EPSS/KEV/SSVC-related inputs supported conceptually |
| Threat intelligence and CTI enrichment | Implemented | Multiple enrichment providers |
| Attack path analysis | Implemented | Investigation support; some graph automation triggers remain operational improvements |
| Investigation and evidence workflows | Implemented | Evidence-first design |
| Guardrailed natural language query | Implemented | Read-only; not in scoring path |
| Decision intelligence and overrides | Implemented | Governed risk decisions |
| Public knowledge library (content) | In progress | Repository foundation and Phase 1 drafts; website publication follows review |
| SBOM operator experience | Partial | Data layer capabilities exist; dedicated SBOM UI limited |
| ITSM ticket creation from decisions | Partial | Capability exists; **disabled by default** in typical tenant configuration |
| Credential leak → incident automation | Partial | Related automation **off by default** in typical configuration |
| Advanced scenario intelligence themes | Planned / progressive | Longer-term roadmap themes—not all generally available |
| Organizational intelligence themes | Planned / progressive | Phased platform evolution |
| Mobile application | Not claimed | Not described as available |

### Documentation maturity (in progress)

- Internal architecture documentation is extensive and authoritative for engineering.
- **Public knowledge** in `docs/public/` is **new** and **progressive**—starting with foundational pages in Phase 1.
- Legacy static marketing pages may contain statements **under review** for alignment with evidence (for example unsupported performance statistics).

### Validation and certification (selective public summary)

| Item | Public statement |
|------|------------------|
| Public Website Phase 3A certification | PASSED — publishing platform certified |
| Investigation intelligence certification | Internal engineering artifact — **not** summarized here in detail |
| SOC 2 certification | **Not** claimed as completed; security posture described as enterprise-oriented with readiness activities |

Current public documentation does not provide sufficient evidence to support a statement that SentriScope holds a completed third-party SOC 2 Type II certification.

## Current Capabilities

See [WHAT_IS_SENTRISCOPE.md](WHAT_IS_SENTRISCOPE.md) and [PLATFORM_OVERVIEW.md](PLATFORM_OVERVIEW.md) for capability detail. This maturity page adds **honest scope boundaries** only.

Implemented highlights supported by internal assessment:

- Broad tenant-facing modules for assets, vulnerabilities, intelligence, and decisions
- Dynamic connector type registration on public integrations surfaces
- Free trial signup and plan catalogue (implemented)

## Current Limitations

- **No customer counts, logos, revenue, or valuation** are stated in this document.
- **No performance benchmarks** (for example "50% triage reduction") are claimed; prior static marketing stats **under review** for removal or replacement with measured methodology.
- **Partial features** must not be presented as fully mature without qualification (SBOM UI, ITSM defaults).
- **Roadmap themes** are not delivery commitments and carry **no dates** in public documentation.
- Maturity assessment here reflects **2026-07-02** evidence; modules evolve—see `next_review` on each public page.

## Frequently Asked Questions

### Is SentriScope production-ready?

The core multi-tenant platform is **implemented and operated as production SaaS**. Individual modules vary in maturity; see the matrix above.

### Is the public documentation complete?

**No.** Documentation is **published progressively**. This repository and the public website will expand under governed review.

### Does certification mean every feature is finished?

**No.** Phase 3A certification applies to the **public website publishing platform**, not every product module.

### Can we rely on marketing pages today?

Technical evaluators should prefer **this knowledge library** and linked pages over legacy static copy where they diverge. Known alignment gaps are tracked internally.

## Related Articles

- [What is SentriScope?](WHAT_IS_SENTRISCOPE.md)
- [What SentriScope is not](WHAT_SENTRISCOPE_IS_NOT.md)
- [Platform overview](PLATFORM_OVERVIEW.md)
- Planned: `public-roadmap-themes`, `investor-technical-overview` (see [INDEX.md](../INDEX.md))

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/certification/CERTIFICATION_PUBLIC_WEBSITE_PHASE3A.md` | Public website platform certification PASSED |
| `docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md` | Implemented vs partial vs marketing gaps |
| `docs/current/architecture/ARCHITECTURE_SYSTEM.md` | Platform domain scope |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Messaging alignment |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Product Governance | Initial public draft |
