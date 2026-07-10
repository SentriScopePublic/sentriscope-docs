---
term: "Relationship"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0039
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0039
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0009
    - KID-GLS-0010
    - KID-GLS-0011
    - KID-GLS-0013
    - KID-GLS-0038
    - KID-GLS-0022
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A security relationship is a decision-relevant link between entities—asset, identity, application, exposure, or path—that changes how observations should be interpreted, prioritized, or investigated."
---

# Relationship

## Definition

In security decision support, a **relationship** is a **decision-relevant link** between entities—assets, identities, applications, exposures, attack paths, or other security objects—that changes how observations should be interpreted, prioritized, or investigated.

Relationships answer questions such as: *What can be reached from here?* *Who can access this?* *Which exposures compound?* *Which path includes this node?* They supply **context through structure**, not merely records in a graph database or network diagram.

This term describes **semantic linkage for judgment**. It is not a graph database product concept, topology discovery output, or visualization layer by itself.

## Relationship types (decision lens)

| Type | Decision question |
|------|-------------------|
| **Asset-to-asset** | What can be reached from this resource? |
| **Identity-to-asset** | Who can touch the exposed or affected resource? |
| **Application-to-service** | What capability depends on this condition? |
| **Exposure-to-path** | Which attack paths include this weakness? |
| **Entity-to-intelligence** | Does external knowledge apply to this entity now? |

## Related terms

- [Asset](./ASSET.md) — `KID-GLS-0009`
- [Identity](./IDENTITY.md) — `KID-GLS-0010`
- [Attack Path](./ATTACK_PATH.md) — `KID-GLS-0011`
- [Correlation](./CORRELATION.md) — `KID-GLS-0013`
- [Blast Radius](./BLAST_RADIUS.md) — `KID-GLS-0022`
- [Canonical Understanding](./CANONICAL_UNDERSTANDING.md) — `KID-GLS-0038`

## Related Knowledge

- [Context Through Relationships](../knowledge/CONTEXT_THROUGH_RELATIONSHIPS.md) — `KID-CON-0124`
- [SER-012 Correlation & Canonical Understanding](../knowledge/SERIES_012_CORRELATION_AND_CANONICAL_UNDERSTANDING.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-012) |
