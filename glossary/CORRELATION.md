---
term: "Correlation"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0013
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0013
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0012
    - KID-GLS-0005
    - KID-GLS-0006
    - KID-GLS-0003
  authority_reference:
    - KID-PLT-0003
    - KID-OIN-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "Correlation links related security signals—findings, assets, identities, threat intel—into unified context so analysts see patterns instead of isolated alerts."
---

# Correlation

## Definition

**Correlation** is the process of linking **related security signals**—findings, assets, identities, threat intelligence, incidents—into unified context. Effective correlation answers: *Do these items belong to the same story?* *Does external threat activity touch internal exposures?*

Correlation reduces duplicate work and surfaces patterns invisible in single-tool views.

## SentriScope Usage

Intelligence correlation layer: `KID-PLT-0003`. Operational and threat intelligence capabilities: `KID-OIN-0001`, `KID-TIN-0001`.

## Related Terms

- [Canonical Data](./CANONICAL_DATA.md) — `KID-GLS-0012`
- [Threat Intelligence](./THREAT_INTELLIGENCE.md) — `KID-GLS-0005`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`

## Related Knowledge

- [Why Correlation Matters](../knowledge/WHY_CORRELATION_MATTERS.md) — `KID-CON-0009`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
