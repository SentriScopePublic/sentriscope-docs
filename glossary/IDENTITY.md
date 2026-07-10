---
term: "Identity"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0010
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0010
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0009
    - KID-GLS-0011
  authority_reference:
    - KID-ARC-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_DATA.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "A security identity is a user or service account from directory or identity provider sources—often a pivot point in investigations and attack paths due to privilege and access."
---

# Identity

## Definition

A **security identity** is a **user or service account** represented in directory, identity provider, or HR-aligned sources. Identities are frequent **pivot points** in investigations and attack paths because privilege, credential exposure, and access relationships amplify impact.

Identity is distinct from an asset (a resource) though identities access assets.

## SentriScope Usage

Identity is a canonical entity: `KID-ARC-0001`. Identity sources: `KID-INT-0001`.

## Related Terms

- [Asset](./ASSET.md) — `KID-GLS-0009`
- [Attack Path](./ATTACK_PATH.md) — `KID-GLS-0011`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
