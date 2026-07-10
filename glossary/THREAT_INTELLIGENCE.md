---
term: "Threat Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0005
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0005
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0006
    - KID-GLS-0013
  authority_reference:
    - KID-TIN-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md
publication_phase: phase_2
website_slug: glossary-threat-intelligence
last_updated: 2026-07-07
next_review: 2027-01-07
llm_summary: "Threat intelligence is validated information about threats—actors, campaigns, indicators, and techniques—used to enrich prioritization and investigation when correlated with internal context."
---

# Threat Intelligence

## Definition

**Threat intelligence** (often **CTI**—cyber threat intelligence) is validated information about threats: actors, campaigns, indicators, techniques, and active exploitation context. Its operational value appears when intelligence is **correlated** with internal assets, exposures, and investigations—not when consumed as isolated feed volume.

Lifecycle stages in mature programs typically include ingest, validate, enrich, correlate, and consume in workflows.

## SentriScope Usage

SentriScope threat intelligence capability and lifecycle: `KID-TIN-0001`. Entity concept: `KID-ARC-0001`.

## Related Terms

- [Operational Intelligence](./OPERATIONAL_INTELLIGENCE.md) — `KID-GLS-0006`
- [Correlation](./CORRELATION.md) — `KID-GLS-0013`

## Related Knowledge

- [Understanding Threat Intelligence](../knowledge/UNDERSTANDING_THREAT_INTELLIGENCE.md) — `KID-CON-0050`
- [SER-005 Threat Intelligence](../knowledge/SERIES_005_THREAT_INTELLIGENCE.md)
- [SER-007 Security Intelligence](../knowledge/SERIES_007_SECURITY_INTELLIGENCE.md)
- [Why Correlation Matters](../knowledge/WHY_CORRELATION_MATTERS.md) — `KID-CON-0009`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md` | CTI lifecycle (sanitized) |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
