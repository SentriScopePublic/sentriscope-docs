---
term: "Asset"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0009
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0009
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0010
    - KID-GLS-0007
    - KID-GLS-0003
  authority_reference:
    - KID-ARC-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_DATA.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "A security asset is a physical, virtual, or cloud resource relevant to analysis—servers, endpoints, cloud resources, and similar—often enriched with business and identity context."
---

# Asset

## Definition

In security analysis, an **asset** is a physical, virtual, or cloud **resource** relevant to protection and investigation: servers, endpoints, containers, databases, network devices, and similar entities. Assets anchor many findings, exposures, and attack paths.

Asset inventories from CMDB, EDR, cloud APIs, and scanners often disagree; normalization and provenance matter.

## SentriScope Usage

Asset is a canonical entity: `KID-ARC-0001`. Ingestion sources: `KID-INT-0001`.

## Related Terms

- [Identity](./IDENTITY.md) — `KID-GLS-0010`
- [Exposure](./EXPOSURE.md) — `KID-GLS-0007`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
