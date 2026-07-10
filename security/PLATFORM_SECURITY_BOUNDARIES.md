---
title: "Platform Security Boundaries"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Security Governance"
technical_reviewer: pending
security_reviewer: pending
ip_reviewer: pending
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_SYSTEM.md
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
related_documents:
  - docs/public/security/TENANT_ISOLATION.md
  - docs/public/security/ROLE_BASED_ACCESS_CONTROL.md
  - docs/public/ai/LLM_GUARDRAILS.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
publication_phase: phase_2
website_slug: platform-security-boundaries
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "SentriScope separates public marketing surfaces from tenant operations, enforces tenant-scoped access, and applies guardrails to AI assistance—defining clear security boundaries without exposing implementation detail."
knowledge_tags:
  - security
  - boundaries
  - platform
  - governance
---

# Platform Security Boundaries

## Executive Summary

SentriScope defines **security boundaries** between what is public, what is tenant-operational, and what remains internal to platform operations. The public marketing website, customer tenant workspaces, and platform operator consoles are **separate surfaces** with distinct access models. AI assistance, connector ingestion, and audit logging each operate within governed boundaries described here at a conceptual level.

## Purpose

Clarify for evaluators and security architects where SentriScope draws lines between public information, customer data, user permissions, and automated assistance—without disclosing hardening internals or operational runbooks.

## Problem Statement

Security platforms combine marketing content, customer data, third-party integrations, and AI features. Without explicit boundaries, teams may assume the wrong trust model—for example treating public documentation as operational guidance, or assuming AI can mutate production security state.

## Industry Context

Mature SaaS security programs document trust zones: public internet presence, authenticated application tiers, integration credentials, and administrative operations. Buyers increasingly ask how AI features respect the same boundaries as traditional APIs.

## SentriScope Perspective

SentriScope organizes the platform into conceptual zones:

| Zone | Audience | Boundary summary |
|------|----------|------------------|
| **Public web** | Prospects, researchers, LLM crawlers (governed) | Marketing pages and **published** knowledge articles only; no tenant data |
| **Tenant workspace** | Customer security teams | Authenticated, tenant-scoped operations on canonical data |
| **Platform operations** | SentriScope operators | Internal governance; not exposed on the public host |
| **Connector integrations** | Customer-authorized systems | Governed ingestion channels scoped per tenant |
| **AI assistance** | Authorized tenant users | Read-only, schema-grounded assistance within tenant context |

**Host separation** between the public marketing site and customer portal or tenant hosts is **implemented**—public URLs do not serve tenant application routes.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Public vs operational host separation | Implemented | Marketing and tenant application hosts are distinct |
| Published-only public knowledge | Implemented | CMS workflow governs what appears on the public site |
| Tenant-scoped operational data | Implemented | Customer security data is not mixed across tenants |
| Governed connector credential handling | Implemented | Integration secrets are stored with encryption references, not exposed in UI or public docs |
| Read-only AI assistance boundary | Implemented | AI does not autonomously change security records |
| Tamper-evident audit logging | Implemented | Security-relevant actions are recorded |
| Quality gates before public publish | Implemented | Internal references and unsafe content are blocked from publication |

## Current Limitations

- This document does **not** enumerate network diagrams, key rotation procedures, or incident response playbooks.
- **Feature flags** may enable or disable specific modules per tenant; boundaries apply to shipped modules, but not every tenant has every module enabled.
- **Third-party connector security** depends partly on customer configuration of upstream systems.
- Public knowledge articles, including this one, are **progressively published**—absence of a page does not imply absence of a control.

## Frequently Asked Questions

### Can I access my tenant data from the public marketing website?

No. The public site provides product and knowledge content. **Tenant data** requires authenticated access on the appropriate operational host.

### Does the public API expose customer security data?

The public read-only knowledge API exposes **published** public content types only—not tenant canonical records.

### Where do LLM features run relative to tenant data?

AI assistance operates **within authorized tenant sessions** and is constrained by guardrails described in [LLM Guardrails](../ai/LLM_GUARDRAILS.md). It does not replace tenant isolation or RBAC.

### Are operator actions visible to customers?

Customer-visible **audit logs** cover tenant-scoped security-relevant activity. Platform operator procedures are governed internally and are **not** described in public documentation.

## Related Articles

- [Tenant isolation](TENANT_ISOLATION.md)
- [Role-based access control](ROLE_BASED_ACCESS_CONTROL.md)
- [LLM guardrails](../ai/LLM_GUARDRAILS.md)
- [Governed ingestion](../integrations/GOVERNED_INGESTION.md)
- [Platform overview](../platform/PLATFORM_OVERVIEW.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_SYSTEM.md` | Platform zones and capability map (sanitized) |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Public vs operational content boundaries |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | Security Governance | Phase 2 initial draft |
