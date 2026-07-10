---
title: "Tenant Isolation"
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
  - docs/current/architecture/ARCHITECTURE_TENANT.md
  - docs/current/architecture/ARCHITECTURE_SYSTEM.md
related_documents:
  - docs/public/security/PLATFORM_SECURITY_BOUNDARIES.md
  - docs/public/security/ROLE_BASED_ACCESS_CONTROL.md
  - docs/public/platform/WHAT_IS_SENTRISCOPE.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
publication_phase: phase_2
website_slug: tenant-isolation
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "SentriScope is multi-tenant by design: each customer organization operates in a tenant-scoped boundary where data access, connector sessions, and analyst workflows are isolated from other tenants."
knowledge_tags:
  - security
  - multi-tenancy
  - isolation
  - platform
---

# Tenant Isolation

## Executive Summary

SentriScope is a **multi-tenant** security intelligence platform. Each customer organization operates within a **tenant boundary** where security data, connector sessions, user access, and audit records are scoped to that tenant. Tenant isolation is an **architectural foundation** (implemented), not an optional configuration. This document explains the isolation model at a conceptual level without implementation or deployment detail.

## Purpose

Help security evaluators, engineers, and procurement stakeholders understand how SentriScope separates customer environments and why isolation matters for SaaS security programs.

## Problem Statement

Shared SaaS platforms must prevent one customer from accessing another customer's data, configuration, or operational context. Without clear tenant boundaries, connector credentials, vulnerability findings, investigations, and audit trails could leak across organizational lines—undermining trust and compliance.

## Industry Context

Enterprise SaaS buyers expect logical isolation between tenants, role-governed access within each tenant, and evidence that isolation is enforced consistently across APIs, background jobs, and user interfaces. Regulatory and contractual obligations often require demonstrable separation of customer data.

## SentriScope Perspective

SentriScope treats **tenant isolation as mandatory** (implemented). Every business record in the platform is associated with a tenant context. Analysts, connectors, intelligence correlation, and audit events operate within that scope.

Isolation applies across:

- **Data plane** — Canonical entities, findings, investigations, and intelligence records are tenant-scoped.
- **Access plane** — Users authenticate into a tenant context; cross-tenant access is not part of the product model.
- **Integration plane** — Connector sessions and credentials belong to a single tenant.
- **Audit plane** — Security-relevant actions are recorded with tenant attribution.

Enterprise deployment options may include dedicated database configurations; isolation principles remain the same regardless of hosting model.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Tenant-scoped data model | Implemented | Business entities are created and queried within tenant context |
| Tenant-scoped connector sessions | Implemented | Ingestion credentials and sync state are per tenant |
| Tenant-scoped user membership | Implemented | Users belong to tenants through governed membership |
| Tenant-scoped audit logging | Implemented | Security-relevant actions record tenant context |
| Public host vs portal host separation | Implemented | Customer operations use separate host boundaries from the public marketing site |

## Current Limitations

- This document does **not** describe physical infrastructure, encryption key management, or penetration-test results.
- **Custom isolation attestations** (for example customer-specific compliance reports) require separate engagement and are **not** self-service on the public website.
- **Cross-tenant analytics** for platform operators follow separate internal governance; customers do not browse other tenants.
- Isolation does **not** replace customer responsibility for identity hygiene, credential rotation, or endpoint security within their organization.

## Frequently Asked Questions

### Does every SentriScope customer share one database?

SentriScope supports **shared** and **dedicated** database deployment models for enterprise tenants. In all models, **logical tenant isolation** is enforced at the application layer.

### Can a user belong to multiple tenants?

Users may hold membership in more than one tenant when invited, but each session operates in **one active tenant context** at a time. Switching tenants requires explicit context change—not silent cross-tenant browsing.

### Is tenant isolation the same as role-based access control?

No. **Isolation** separates customers; **RBAC** governs what authorized users can do within a tenant. Both are required. See [Role-Based Access Control](ROLE_BASED_ACCESS_CONTROL.md).

### Does tenant isolation guarantee compliance certifications?

Isolation is a **technical control**. Compliance outcomes depend on your program, contracts, and how you configure and operate the platform.

## Related Articles

- [Platform security boundaries](PLATFORM_SECURITY_BOUNDARIES.md)
- [Role-based access control](ROLE_BASED_ACCESS_CONTROL.md)
- [What is SentriScope?](../platform/WHAT_IS_SENTRISCOPE.md)
- [Platform overview](../platform/PLATFORM_OVERVIEW.md)
- [Glossary: Tenant](../glossary/TENANT.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_TENANT.md` | Tenant isolation architecture (sanitized) |
| `docs/current/architecture/ARCHITECTURE_SYSTEM.md` | Multi-tenant platform context |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | Security Governance | Phase 2 initial draft |
