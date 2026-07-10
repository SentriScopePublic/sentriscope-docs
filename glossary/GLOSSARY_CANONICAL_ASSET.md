---
title: "Glossary: Canonical Asset"
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
knowledge_id: KID-GLS-0042
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0042
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_DATA.md
related_documents:
  - docs/public/glossary/ASSET.md
  - docs/public/glossary/CANONICAL_DATA.md
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
publication_phase: phase_2
website_slug: glossary-canonical-asset
last_updated: 2026-07-07
next_review: 2027-01-07
llm_summary: "A canonical asset is a normalized security resource record in SentriScope—unified across ingestion sources with provenance—serving as an anchor for exposures, risk context, and investigations."
knowledge_tags:
  - glossary
  - asset
  - canonical
  - foundation
---

# Glossary: Canonical Asset

## Executive Summary

A **canonical asset** is a **normalized** representation of a security-relevant resource—server, endpoint, cloud workload, device, or similar—within SentriScope's shared data model. Canonical assets reconcile disagreeing inventories from scanners, CMDB systems, and cloud APIs while retaining **provenance** so analysts know which source contributed each attribute.

## Purpose

Provide a public-safe foundation definition for how SentriScope uses **asset** in the **canonical** sense—distinct from raw vendor export rows.

## Problem Statement

The same physical system may appear under multiple names, IDs, and classifications across tools. Without canonical assets, prioritization and investigations fragment across duplicate records.

## Industry Context

Security programs refer to assets, configuration items, and resources interchangeably. Canonical modeling aligns terminology for correlation, exposure linkage, and risk context.

## SentriScope Perspective

In SentriScope (implemented):

- Assets are **canonical entities** ingested through governed connectors.
- Assets anchor **exposures**, **identities**, and **attack path** relationships.
- **Unknown or incomplete assets** remain an operational reality—normalization improves over time with ingestion quality.
- Canonical assets are described further in [Canonical data model](../architecture/CANONICAL_DATA_MODEL.md).

This entry complements glossary authorities [Asset](ASSET.md) and [Canonical data](CANONICAL_DATA.md).

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Canonical asset entity | Implemented | Normalized resource records per tenant |
| Multi-source ingestion | Implemented | Connectors contribute asset attributes with provenance |
| Asset criticality context | Partial | Business and security context enrichment varies by data availability |
| Unknown asset handling | Implemented | Gaps surfaced for analyst remediation programs |

## Current Limitations

- Canonical assets reflect **ingested truth**, not guaranteed physical completeness.
- **CMDB quality** directly affects asset accuracy.
- This glossary entry does **not** define internal matching algorithms.
- Not every IT asset type may be modeled with equal depth.

## Frequently Asked Questions

### Is a canonical asset the same as a CMDB CI?

Often related. Canonical assets **normalize** CMDB and non-CMDB sources into a security-oriented model.

### Can one canonical asset map to multiple source records?

Yes. Provenance tracks contributing sources; reconciliation is an ongoing operational concern.

### Where do exposures attach?

Exposures link assets (or related entities) to vulnerability or misconfiguration context—see [Glossary: Exposure](EXPOSURE.md).

## Related Articles

- [Asset](ASSET.md)
- [Canonical data](CANONICAL_DATA.md)
- [Canonical data model](../architecture/CANONICAL_DATA_MODEL.md)
- [Supported data sources](../integrations/SUPPORTED_DATA_SOURCES.md)
- [Glossary: Exposure](EXPOSURE.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Canonical asset concept (sanitized) |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-07 | Phase 2 glossary foundation entry |
