---
title: "Supported Data Sources"
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
knowledge_id: KID-INT-0001
knowledge_domain: integrations
knowledge_object: reference
authority_tier: T5
is_authority: true
authority_document: KID-INT-0001
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_CONNECTORS.md
  - docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md
  - docs/current/architecture/ARCHITECTURE_DATA.md
related_documents:
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
  - docs/public/intelligence/THREAT_INTELLIGENCE.md
knowledge_relationships:
  depends_on:
    - KID-PLT-0001
    - KID-ARC-0001
    - KID-PLT-0003
  explains: []
  supersedes: []
  related_to:
    - KID-TIN-0001
  implements: []
  introduces: []
  deprecates: []
  expands:
    - KID-PLT-0003
navigation:
  personas: [engineer, partner, evaluator]
  learning_paths: [LP-004]
  prerequisites:
    - KID-PLT-0003
    - KID-ARC-0001
  next_reading:
    - KID-TIN-0001
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md#kid-int-0001--supported-data-sources
publication_phase: stream-a
website_slug: supported-data-sources
last_updated: 2026-07-02
next_review: 2026-09-02
llm_summary: "SentriScope ingests security data through governed connector sessions across vulnerability, endpoint, identity, CMDB, network, and ratings sources—normalizing into canonical entities with provenance; CTI enrichment providers are cataloged separately from base connectors."
knowledge_tags:
  - integrations
  - connectors
  - data-sources
  - reference
---

# Supported Data Sources

## Industry Problem

Security programs operate dozens of tools—each exporting different formats, identifiers, and update cadences. Without governed ingestion, analysts manually reconcile the same asset, vulnerability, or identity across scanners, CMDB records, EDR consoles, and threat feeds.

Inconsistent ingestion also breaks downstream prioritization, investigation, and audit: teams cannot explain which source produced a finding or whether re-sync duplicated records.

## Why the Problem Exists

Vendors optimize for their own data models. Enterprise architecture rarely enforces a single normalization layer before analysis. Ad hoc scripts and point integrations lack tenant isolation, credential governance, health monitoring, and idempotent upsert semantics required for multi-tenant SaaS.

## Traditional Approaches

| Approach | Limitation |
|----------|------------|
| Manual CSV imports | No continuous sync; weak provenance |
| Custom ETL per tool | Expensive to maintain; inconsistent validation |
| SIEM-only aggregation | Event-centric; weak CMDB and exposure semantics |
| API scripts without governance | Credential risk; no audit standard |
| Flat file threat feeds | Indicators without asset linkage |

Mature platforms use **governed connector sessions**: registered source types, encrypted credential handling, health status, validation guardrails, and canonical upsert with provenance.

## SentriScope Perspective

SentriScope ingests external security data through **governed connector sessions** (implemented)—the ingestion layer in [KID-PLT-0003](../platform/PLATFORM_OVERVIEW.md). Data normalizes into canonical concepts in [KID-ARC-0001](../architecture/CANONICAL_DATA_MODEL.md).

Public-safe ingestion principles:

| Principle | Meaning |
|-----------|---------|
| **Tenant scope** | All ingested business data attributed to a tenant |
| **Provenance** | Source system and external identifiers preserved conceptually |
| **Validation** | Payloads validated before canonical write |
| **Idempotency** | Re-sync safe—duplicate external records do not multiply entities |
| **Health monitoring** | Connector operational state visible to operators |
| **Credential governance** | Secrets referenced securely—not stored as plaintext application data |

**Outputs:** Populated canonical entities (assets, exposures, identities, incidents, and related concepts) consumed by operational intelligence [KID-OIN-0001](../intelligence/OPERATIONAL_INTELLIGENCE.md), threat intelligence [KID-TIN-0001](../intelligence/THREAT_INTELLIGENCE.md), investigation [KID-INV-0001](../investigations/INVESTIGATION_WORKSPACE.md), and attack path analysis [KID-AGR-0001](../capabilities/ATTACK_GRAPH_OVERVIEW.md).

This document is the **authority for which source categories SentriScope supports publicly**. It does not redefine canonical entities or platform boundaries.

## Current Product Capability

### Registered connector categories (implemented)

As of internal registry evidence (2026-07-02), SentriScope registers **15 governed connector types** across:

| Category | Examples (vendor families) | Canonical concepts fed |
|----------|---------------------------|------------------------|
| CMDB / ITSM assets | ServiceNow CMDB, Jira Service Management Assets | Assets, applications, relationships |
| Vulnerability management | Tenable, Qualys | Assets, exposures, vulnerabilities |
| Endpoint detection & response | Microsoft Defender, CrowdStrike, SentinelOne, Cortex XDR, Trellix | Assets, incidents, exposures |
| Cloud / CSPM | Palo Alto Cortex Cloud (Prisma) | Assets, exposures, vulnerabilities |
| Network / segmentation / OT | Akamai Guardicore, Nozomi | Assets, flows, segmentation context |
| Identity | Microsoft Entra ID | Identities, credential metadata, auth events |
| Security ratings & DRP | SecurityScorecard, Tempest Prospero | Assets, exposures, credential leak records |

Exact availability may vary by tenant plan and configuration. The **live integrations catalog** on the public website is authoritative over static copy.

### CTI enrichment (related, separate catalog)

**Threat intelligence enrichment providers** are registered **separately** from the 15 base connector types. Internal assessment records **14 CTI enrichment providers** with runtime implementations. Public marketing must not combine counts without explicit qualification.

See [KID-TIN-0001](../intelligence/THREAT_INTELLIGENCE.md) for CTI consumption—not redefined here.

### Connector governance (implemented)

| Capability | State |
|------------|-------|
| Connector type registry | Implemented |
| Session health and sync status | Implemented |
| Governed validation on ingest | Implemented |
| Audit of data create/update from connectors | Implemented |
| ITSM ticket creation from decisions | Partial — may be disabled by default |

Full implementation status matrix: [KID-PLT-0004](../platform/PRODUCT_MATURITY.md).

## Current Limitations

- **Not every connector populates every canonical entity type**—depends on source capability.
- Connector count **changes** as new types register; this document requires periodic review (`next_review` 90 days).
- Static marketing claims such as "20+ connectors" **overstate** the base connector registry if evaluated literally; use dynamic catalog or qualified language (15 base connectors + separate CTI enrichment providers).
- SentriScope **does not** perform native network scanning as a primary function—see [KID-PLT-0002](../platform/WHAT_SENTRISCOPE_IS_NOT.md).
- Ingestion architecture, trust tiers, and API contracts are **not** described in this public page.
- Partner-specific integration depth is **partner-classification** content.

## Common Questions

### How many data sources does SentriScope support?

Use the registered connector catalog (15 base types at last assessment) plus separate CTI enrichment providers. Do not rely on outdated static marketing numbers.

### Does SentriScope store vendor credentials?

Connector sessions use governed credential references designed to avoid plaintext secret storage in application data. Operational security details are not public documentation.

### Can new connectors be added?

Yes (implemented). Connector types register in the platform catalog; availability follows product and partner processes—not public roadmap dates.

### Is CMDB required?

No. SentriScope operates with vulnerability, EDR, identity, and threat sources; CMDB connectors **enhance** business and asset context when present.

## Related Concepts

### Prerequisites

- [Platform Overview](../platform/PLATFORM_OVERVIEW.md) — `KID-PLT-0003`
- [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md) — `KID-ARC-0001`

### See also

- [Threat Intelligence](../intelligence/THREAT_INTELLIGENCE.md) — `KID-TIN-0001`

### Planned

- CONNECTOR_ARCHITECTURE (ingestion governance detail)
- `KID-FAQ-0004` Supported data sources FAQ
- `KID-GLS-0009` Governed connector

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_CONNECTORS.md` | Connector categories and governance (sanitized) |
| `docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md` | Registry counts, marketing alignment |
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Canonical concepts fed by ingestion |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Integrations PM | Initial domain authority (Stream A) |
