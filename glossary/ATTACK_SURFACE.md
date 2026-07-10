---
term: "Attack Surface"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0036
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0036
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0007
    - KID-GLS-0035
    - KID-GLS-0037
    - KID-GLS-0011
    - KID-GLS-0009
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Attack surface is the aggregate of reachable, exposure-relevant entry points—interfaces, services, identities, and paths—an organization must reason about when prioritizing reduction."
---

# Attack Surface

## Definition

**Attack surface** is the **aggregate of reachable, exposure-relevant entry points** an organization must reason about when understanding and reducing security exposure.

It includes interfaces, services, identities, network paths, and configuration states that could be reached or abused—not a raw count of open ports or a scanner inventory alone. Attack surface is a **decision lens**: which entry points matter **now**, given [exposure context](./EXPOSURE_CONTEXT.md), relationships, and operational significance.

Attack surface differs from a vulnerability list by emphasizing **where adversaries could interact** with the environment, not merely what weaknesses exist in isolation.

## SentriScope Usage

SentriScope relates attack surface to canonical assets, applications, exposures, and [attack paths](./ATTACK_PATH.md) (`KID-ARC-0001`) so teams can explain which reachable entry points drive prioritization—not just how many findings exist. This entry defines the term only.

## Related terms

- [Exposure](./EXPOSURE.md) — `KID-GLS-0007`
- [Exposure Context](./EXPOSURE_CONTEXT.md) — `KID-GLS-0035`
- [Attack Exposure](./ATTACK_EXPOSURE.md) — `KID-GLS-0037`
- [Attack Path](./ATTACK_PATH.md) — `KID-GLS-0011`
- [Asset](./ASSET.md) — `KID-GLS-0009`

## Related Knowledge

- [Exposure Relationships](../knowledge/EXPOSURE_RELATIONSHIPS.md) — `KID-CON-0114`
- [SER-011 Exposure Management](../knowledge/SERIES_011_EXPOSURE_MANAGEMENT.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-011) |
