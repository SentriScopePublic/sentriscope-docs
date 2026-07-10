---
term: "Attack Exposure"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0037
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0037
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0007
    - KID-GLS-0035
    - KID-GLS-0036
    - KID-GLS-0011
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Attack exposure is exposure interpreted through adversary reachability and path context—how a weakness could be reached and chained—used to prioritize reduction and investigation."
---

# Attack Exposure

## Definition

**Attack exposure** is [exposure](./EXPOSURE.md) viewed through **adversary reachability and path context** for prioritization and reduction decisions.

It connects a weakness or misconfiguration to **how** it could be reached—network position, identity access, [attack paths](./ATTACK_PATH.md), and [attack surface](./ATTACK_SURFACE.md) relationships—not the catalog severity of the flaw alone. Two exposures with similar scores can differ sharply in attack exposure when one sits on a reachable path to critical assets and the other does not.

Attack exposure supports **explainable prioritization**: which exposures to reduce first because adversaries could realistically leverage them, given current [exposure context](./EXPOSURE_CONTEXT.md).

## SentriScope Usage

SentriScope combines exposure records with path and reachability context (`KID-ARC-0001`) so analysts can rank work by **attack exposure**, not flat severity lists. This entry defines the term only.

## Related terms

- [Exposure](./EXPOSURE.md) — `KID-GLS-0007`
- [Exposure Context](./EXPOSURE_CONTEXT.md) — `KID-GLS-0035`
- [Attack Surface](./ATTACK_SURFACE.md) — `KID-GLS-0036`
- [Attack Path](./ATTACK_PATH.md) — `KID-GLS-0011`

## Related Knowledge

- [Exposure Prioritization](../knowledge/EXPOSURE_PRIORITIZATION.md) — `KID-CON-0113`
- [Exposure Relationships](../knowledge/EXPOSURE_RELATIONSHIPS.md) — `KID-CON-0114`
- [SER-011 Exposure Management](../knowledge/SERIES_011_EXPOSURE_MANAGEMENT.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-011) |
