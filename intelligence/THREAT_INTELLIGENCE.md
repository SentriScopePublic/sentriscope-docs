---
title: "Threat Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Intelligence PM"
technical_reviewer: pending
security_reviewer: pending
ip_reviewer: pending
knowledge_id: KID-TIN-0001
knowledge_domain: threat-intelligence
knowledge_object: capability
authority_tier: T5
is_authority: true
authority_document: KID-TIN-0001
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md
  - docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
related_documents:
  - docs/public/intelligence/OPERATIONAL_INTELLIGENCE.md
  - docs/public/capabilities/ATTACK_GRAPH_OVERVIEW.md
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
knowledge_relationships:
  depends_on:
    - KID-PLT-0001
    - KID-ARC-0001
  explains: []
  supersedes: []
  related_to:
    - KID-OIN-0001
    - KID-AGR-0001
    - KID-INT-0001
  implements: []
  introduces: []
  deprecates: []
  expands:
    - KID-PLT-0003
navigation:
  personas: [analyst, ciso, engineer]
  learning_paths: [LP-002, LP-004]
  prerequisites:
    - KID-PLT-0001
    - KID-ARC-0001
  next_reading:
    - KID-OIN-0001
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md#kid-tin-0001--threat-intelligence
publication_phase: stream-a
website_slug: threat-intelligence
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "SentriScope threat intelligence normalizes CTI items through a governed lifecycle, correlates indicators and actors with tenant assets and exposures, and enriches prioritization—without autonomous blocking or replacing analyst validation."
knowledge_tags:
  - threat-intelligence
  - cti
  - enrichment
  - capability
---

# Threat Intelligence

## Industry Problem

Threat intelligence feeds deliver indicators, actor profiles, and campaign reports faster than teams can validate relevance. Raw IOC lists without environmental context produce false positives; ignoring feeds misses active exploitation against owned assets.

Analysts need **lifecycle-managed intelligence**—ingested, validated, enriched, correlated to internal entities, and consumed in prioritization and investigation—not another unread RSS stream.

## Why the Problem Exists

CTI vendors optimize for breadth. Internal vulnerability and asset tools optimize for depth. Without a normalization and correlation layer, teams manually answer: *Does this indicator touch our environment?* *Is this CVE actively exploited in our sector?* *Which campaign overlaps our exposures?*

Threat intelligence that stays external to the operational model rarely changes daily triage outcomes.

## Traditional Approaches

| Approach | Limitation |
|----------|------------|
| Standalone TIP platforms | Often weak asset and exposure linkage |
| Feed aggregation only | No governed lifecycle or tenant scope |
| Block-list automation | High false positive risk; policy friction |
| Manual analyst spreadsheets | Not auditable at scale |
| News-only consumption | Awareness without correlation |

Effective programs use a **CTI lifecycle**: ingest → validate → enrich → correlate → consume in risk and investigation workflows—with provenance preserved.

## SentriScope Perspective

SentriScope provides **threat intelligence** as part of its intelligence correlation layer (implemented)—normalizing CTI into tenant-scoped canonical concepts and linking intelligence to assets, identities, and exposures defined in [KID-ARC-0001](../architecture/CANONICAL_DATA_MODEL.md).

Public lifecycle states (conceptual):

| State | Meaning |
|-------|---------|
| New | Ingested; not yet validated |
| Validated | Analyst confirmed relevance |
| Enriched | Additional context applied (for example actor, campaign, IOC correlation) |
| Correlated | Linked to internal canonical entities |
| Consumed | Used in prioritization, investigation, or decision support |

**Inputs:** External feeds, enrichment providers, tenant subscriptions, and reference data (for example CVE catalogs)—ingested under governed connector patterns described in [KID-INT-0001](../integrations/SUPPORTED_DATA_SOURCES.md).

**Outputs:** Enriched threat context in operational queues [KID-OIN-0001](../intelligence/OPERATIONAL_INTELLIGENCE.md), investigation sessions [KID-INV-0001](../investigations/INVESTIGATION_WORKSPACE.md), and attack path context [KID-AGR-0001](../capabilities/ATTACK_GRAPH_OVERVIEW.md)—with explainable linkage, not opaque scores.

**Boundaries:**

- Threat intelligence **does not** autonomously block traffic or execute response.
- Deterministic prioritization paths do **not** use LLM as the critical scoring engine for attention points.
- CTI enrichment provider count is distinct from connector count; public counts must not conflate the two without qualification.

## Current Product Capability

| Capability | State | Summary |
|------------|-------|---------|
| CTI item normalization and lifecycle | Implemented | Tenant-scoped threat intel records with states |
| Threat actor and campaign concepts | Implemented | Profiles linked to intelligence items |
| IOC correlation to canonical entities | Implemented | Links indicators to environmental context |
| Intelligence enrichment providers | Implemented | Multiple enrichment sources (separate from base connector catalog) |
| Threat intel feed subscriptions | Implemented | Platform feed with tenant subscription model |
| Intelligence dashboard integration | Implemented | CTI context in operational prioritization |
| Influence on deterministic prioritization | Implemented | Threat relevance in attention-point reason codes |
| Autonomous threat blocking | Not available | Human validation and governance required |

Enrichment provider and connector counts: see [KID-INT-0001](../integrations/SUPPORTED_DATA_SOURCES.md) and [KID-PLT-0004](../platform/PRODUCT_MATURITY.md).

## Current Limitations

- Feed quality and lag vary by provider; stale intelligence reduces correlation value.
- False positive IOC matches require analyst validation—SentriScope does not claim zero false positives.
- Not every enrichment or feed type populates all lifecycle stages for all tenants.
- Public documentation does not enumerate every provider contract or partner integration depth.
- Advanced scenario conjunction of campaigns with paths is **planned or progressive** for some themes.

## Common Questions

### Is SentriScope a threat intelligence platform (TIP)?

SentriScope integrates CTI into a broader **security intelligence** platform—normalization, risk, investigation, and decision support—rather than offering a standalone TIP-only product boundary.

### Does threat intelligence automatically change risk scores?

Threat context influences **deterministic prioritization** through governed rules and canonical linkage. It does not introduce unaudited LLM scoring on critical paths.

### How many enrichment sources are supported?

The platform registers multiple CTI enrichment providers in addition to base data connectors. Exact counts should be taken from the live integrations catalog, not static marketing copy. Evidence: internal assessment of registry counts.

### Can threat intelligence drive investigations?

Yes (implemented). Correlated intelligence feeds investigation context; analysts remain accountable for conclusions in [KID-INV-0001](../investigations/INVESTIGATION_WORKSPACE.md).

## Related Concepts

### Prerequisites

- [What is SentriScope?](../platform/WHAT_IS_SENTRISCOPE.md) — `KID-PLT-0001`
- [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md) — `KID-ARC-0001`

### See also

- [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md) — `KID-OIN-0001`
- [Attack Graph Overview](../capabilities/ATTACK_GRAPH_OVERVIEW.md) — `KID-AGR-0001`
- [Supported Data Sources](../integrations/SUPPORTED_DATA_SOURCES.md) — `KID-INT-0001`

### Planned (Stream B)

- `KID-CON-0004` Threat Intelligence Lifecycle
- `KID-GLS-0007` Threat intelligence lifecycle
- `KID-GLS-0008` CTI enrichment

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md` | CTI lifecycle, dashboard integration, feeds |
| `docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md` | Provider counts, implemented status |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Messaging boundaries |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Intelligence PM | Initial domain authority (Stream A) |
