---
term: "Tenant"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0043
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0043
knowledge_lifecycle: validated
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_TENANT.md
related_documents:
  - docs/public/security/TENANT_ISOLATION.md
  - docs/public/glossary/GLOSSARY_INDEX.md
publication_phase: phase_2
website_slug: glossary-tenant
last_updated: 2026-07-07
next_review: 2027-01-07
llm_summary: "In SentriScope, a tenant is an isolated customer organization boundary—scoped data, users, connectors, and audit context—within the multi-tenant SaaS platform."
knowledge_tags:
  - glossary
  - tenant
  - multi-tenancy
  - foundation
---

# Tenant

## Definition

In SentriScope, a **tenant** is an **isolated customer organization boundary** within the multi-tenant platform. Security data, connector sessions, user memberships, investigations, and audit records are **scoped to a tenant**. Tenants do not share operational data with one another.

A tenant typically represents one customer organization or a defined organizational partition agreed in contract.

## SentriScope Usage

Multi-tenancy is an **architectural foundation** (implemented). Users work inside a tenant context after authentication. See [Tenant isolation](../security/TENANT_ISOLATION.md) for the security model.

## Related Terms

- [Canonical data](./CANONICAL_DATA.md) — `KID-GLS-0012`
- [Provenance](./PROVENANCE.md) — `KID-GLS-0014`

## Related Knowledge

- [Tenant isolation](../security/TENANT_ISOLATION.md)
- [Platform security boundaries](../security/PLATFORM_SECURITY_BOUNDARIES.md)
- [What is SentriScope?](../platform/WHAT_IS_SENTRISCOPE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-07 | Phase 2 glossary foundation entry |
