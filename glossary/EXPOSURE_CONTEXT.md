---
term: "Exposure Context"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0035
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0035
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0007
    - KID-GLS-0003
    - KID-GLS-0009
    - KID-GLS-0036
    - KID-GLS-0037
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Exposure context is the layered situational information—asset, environment, reachability, and business significance—that changes how an exposure should be interpreted and prioritized."
---

# Exposure Context

## Definition

**Exposure context** is the **layered situational information** that changes how an [exposure](./EXPOSURE.md) should be interpreted and prioritized in security decisions.

Context includes where the weakness applies ([asset](./ASSET.md), application, identity), how it is reachable, what business or operational function is affected, and how [security context](./SECURITY_CONTEXT.md) shifts significance over time. The same weakness can warrant different urgency depending on these layers—not because severity scores are wrong, but because **decisions are environment-specific**.

## SentriScope Usage

SentriScope enriches canonical exposures with context from assets, applications, attack paths, and intelligence layers (`KID-ARC-0001`) so prioritization and investigations can explain **why** the same finding ranks differently across environments. This entry defines the term only.

## Related terms

- [Exposure](./EXPOSURE.md) — `KID-GLS-0007`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`
- [Attack Surface](./ATTACK_SURFACE.md) — `KID-GLS-0036`
- [Attack Exposure](./ATTACK_EXPOSURE.md) — `KID-GLS-0037`

## Related Knowledge

- [Exposure Context](../knowledge/EXPOSURE_CONTEXT.md) — `KID-CON-0112`
- [FAQ: Why does exposure context matter?](../faq/FAQ_WHY_DOES_EXPOSURE_CONTEXT_MATTER.md) — `KID-FAQ-0060`
- [SER-011 Exposure Management](../knowledge/SERIES_011_EXPOSURE_MANAGEMENT.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-011) |
