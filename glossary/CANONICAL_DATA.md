---
term: "Canonical Data"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0012
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0012
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0009
    - KID-GLS-0013
  authority_reference:
    - KID-ARC-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_DATA.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "Canonical data is security information normalized into shared entity types and provenance regardless of source format—enabling correlation without manual reconciliation across tools."
---

# Canonical Data

## Definition

**Canonical data** is security information **normalized** into shared entity types—assets, identities, exposures, incidents, threat intelligence, and related concepts—regardless of which vendor or tool produced the original export. Canonical models carry **provenance** so analysts know the origin of each record.

Canonical data enables correlation across tools without manually mapping proprietary formats for every analysis.

## SentriScope Usage

SentriScope canonical entity definitions: `KID-ARC-0001`. Ingestion into canonical form: `KID-INT-0001`, platform layers: `KID-PLT-0003`.

## Related Terms

- [Correlation](./CORRELATION.md) — `KID-GLS-0013`
- [Asset](./ASSET.md) — `KID-GLS-0009`

## Related Knowledge

- [Why Correlation Matters](../knowledge/WHY_CORRELATION_MATTERS.md) — `KID-CON-0009`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
