---
title: "Connector Architecture"
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
  - docs/public/integrations/SUPPORTED_DATA_SOURCES.md
  - docs/public/integrations/GOVERNED_INGESTION.md
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
publication_phase: phase_2
website_slug: connector-architecture
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "SentriScope connectors are governed integration sessions that ingest security data from authorized sources into the canonical model—scoped per tenant with health monitoring, credential protection, and provenance."
knowledge_tags:
  - integrations
  - connectors
  - architecture
  - ingestion
---

# Connector Architecture

## Executive Summary

**Connectors** are SentriScope's governed integration layer between external security and IT systems and the platform's **canonical data model**. Each connector session belongs to a **single tenant**, uses protected credentials, synchronizes on a defined schedule or trigger, and records **provenance** so analysts know which source produced each record. Connector architecture is **implemented**; the catalog of supported sources evolves over time.

## Purpose

Explain the conceptual connector model—sessions, sources, normalization, and health—so engineers and architects can evaluate integration fit without internal class names, queue topology, or credential storage mechanics.

## Problem Statement

Point-to-point scripts and ad hoc API pulls do not scale for multi-tenant security platforms. Teams need repeatable ingestion with tenant isolation, credential governance, failure visibility, and idempotent normalization into shared entity concepts.

## Industry Context

Modern security data platforms integrate vulnerability scanners, endpoint agents, identity providers, CMDB systems, cloud APIs, and threat intelligence feeds. Buyers evaluate connector breadth, sync reliability, and how ingestion supports prioritization—not just raw API checklists.

## SentriScope Perspective

SentriScope connector architecture has four conceptual layers:

| Layer | Role |
|-------|------|
| **Connector type** | Defines what category of external system can be integrated (for example vulnerability assessment, endpoint, identity) |
| **Connector session** | Tenant-specific configured instance with credentials, scope, and sync behavior |
| **Ingestion pipeline** | Transforms source records into canonical entities with provenance |
| **Health and operations** | Surfaces sync status, errors, and staleness for administrators |

Connectors feed the canonical model described in [Canonical data model](../architecture/CANONICAL_DATA_MODEL.md). They do **not** replace upstream tools—they **normalize and govern** their outputs for analysis within SentriScope.

Threat intelligence **enrichment** providers may follow related but distinct catalog patterns; see [Supported data sources](SUPPORTED_DATA_SOURCES.md).

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Multi-category connector catalog | Implemented | Vulnerability, endpoint, identity, CMDB, network, and related source types |
| Per-tenant connector sessions | Implemented | Isolated configuration and credentials |
| Encrypted credential references | Implemented | Secrets not stored in plaintext in application data |
| Sync health monitoring | Implemented | Administrators can observe session status |
| Canonical normalization on ingest | Implemented | Source records mapped to shared entity concepts |
| Provenance on ingested records | Implemented | Origin source attributable in analysis workflows |
| Dynamic public catalog counts | Implemented | Marketing and documentation use registry-backed counts |

## Current Limitations

- **Not every enterprise system** has a first-class connector; gaps may require roadmap prioritization or custom engagement.
- **Bi-directional ITSM automation** may be partial or disabled by default per tenant.
- This document does **not** specify sync frequency guarantees, rate limits, or retry algorithms.
- Connectors ingest **authorized** data only—customers must permit API access in upstream systems.
- **Real-time streaming** vs scheduled batch behavior varies by connector type.

## Frequently Asked Questions

### Is a connector the same as a data source?

In public documentation, **connector session** is the tenant-configured integration; **data source** describes the upstream system category or vendor pattern. See [Supported data sources](SUPPORTED_DATA_SOURCES.md).

### Do connectors run in my network or in SentriScope cloud?

Deployment topology depends on your edition and connector type. This page describes the logical model, not hosting diagrams.

### Can one connector session serve multiple tenants?

No. Sessions are **tenant-scoped** for isolation and auditability.

### What happens when a sync fails?

Health monitoring surfaces failures for administrator review. Downstream analysis may reflect stale data until sync succeeds.

## Related Articles

- [Supported data sources](SUPPORTED_DATA_SOURCES.md)
- [Governed ingestion](GOVERNED_INGESTION.md)
- [Canonical data model](../architecture/CANONICAL_DATA_MODEL.md)
- [Tenant isolation](../security/TENANT_ISOLATION.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_CONNECTORS.md` | Connector domain model (sanitized) |
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Canonical normalization context |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | Integrations PM | Phase 2 initial draft |
