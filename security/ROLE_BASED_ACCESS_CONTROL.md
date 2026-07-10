---
title: "Role-Based Access Control"
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
  - docs/current/architecture/ARCHITECTURE_TENANT.md
related_documents:
  - docs/public/security/TENANT_ISOLATION.md
  - docs/public/security/PLATFORM_SECURITY_BOUNDARIES.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
publication_phase: phase_2
website_slug: role-based-access-control
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "SentriScope uses role-based access control within each tenant so administrators can grant least-privilege access to security data, connectors, investigations, and configuration—complementing tenant isolation."
knowledge_tags:
  - security
  - rbac
  - access-control
  - governance
---

# Role-Based Access Control

## Executive Summary

Within each tenant, SentriScope applies **role-based access control (RBAC)** so administrators can grant **least-privilege** access to security data, workflows, and configuration. RBAC complements **tenant isolation**: isolation separates customers; RBAC governs what authorized users can view or change inside their tenant. RBAC is **implemented** as a platform foundation.

## Purpose

Help security and IT stakeholders evaluate how SentriScope limits user capabilities across modules such as investigations, connectors, intelligence, and administration—without naming internal permission tables or policy engines.

## Problem Statement

Even with strong tenant isolation, overly broad user permissions create insider risk, accidental data exposure, and audit gaps. Security platforms need granular roles that map to real team functions—analyst, engineer, administrator—without custom per-user exceptions at scale.

## Industry Context

Enterprise buyers expect RBAC integrated with identity providers, separation of duties for administrative actions, and auditable permission changes. RBAC is typically evaluated alongside MFA, session management, and tenant membership controls.

## SentriScope Perspective

SentriScope RBAC operates **inside the tenant boundary** (implemented):

- **Membership** — Users are invited to a tenant with a defined role or role set.
- **Module permissions** — Capabilities such as viewing canonical data, managing connectors, running investigations, or changing tenant settings map to permission checks.
- **Administrative separation** — Sensitive configuration changes are restricted to roles with explicit administrative authority.
- **Audit alignment** — Security-relevant actions are recorded with actor attribution.

RBAC applies to **human users** and governs UI and API access within tenant sessions. It does **not** grant cross-tenant visibility.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Tenant membership with roles | Implemented | Users access tenant resources through assigned roles |
| Permission checks on tenant routes | Implemented | Views and APIs enforce authorization before data access |
| Administrative role distinction | Implemented | Configuration and governance actions require elevated roles |
| Identity provider integration options | Partial | Enterprise SSO patterns are supported; exact IdP features depend on tenant configuration |
| Audit logging of security-relevant actions | Implemented | Actor and action context recorded for governance |

## Current Limitations

- This document does **not** list every permission code or role matrix—those evolve with product modules.
- **Custom per-resource ACLs** beyond the RBAC model are **not** a general-purpose feature unless documented for a specific module.
- **Break-glass** or emergency access patterns, if used operationally, are governed internally and are **not** self-service customer features.
- RBAC does **not** automatically remediate findings or approve investigations—it controls **who** can perform actions.

## Frequently Asked Questions

### Is RBAC the same as tenant isolation?

No. **Tenant isolation** prevents cross-customer access. **RBAC** limits what users can do **within** a tenant. Both are required.

### Can I integrate corporate SSO?

SentriScope supports enterprise identity integration patterns for tenant authentication. Specific protocols and provisioning features depend on your edition and configuration.

### Does RBAC apply to AI features?

Yes. Users must be authorized within the tenant to access modules that expose AI assistance. AI remains **read-only** with respect to mutating security records regardless of role.

### Can auditors have read-only access?

Read-oriented roles can be modeled for stakeholders who need visibility without configuration authority. Exact role names and scopes are configured per tenant.

## Related Articles

- [Tenant isolation](TENANT_ISOLATION.md)
- [Platform security boundaries](PLATFORM_SECURITY_BOUNDARIES.md)
- [Platform overview](../platform/PLATFORM_OVERVIEW.md)
- [Read-only AI assistance](../ai/READ_ONLY_AI_ASSISTANCE.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_SYSTEM.md` | Authorization and platform modules (sanitized) |
| `docs/current/architecture/ARCHITECTURE_TENANT.md` | Tenant membership context |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | Security Governance | Phase 2 initial draft |
