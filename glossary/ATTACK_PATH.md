---
term: "Attack Path"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0011
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0011
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0002
    - KID-GLS-0009
    - KID-GLS-0010
    - KID-GLS-0013
  authority_reference:
    - KID-AGR-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_ATTACK_PATH_INTELLIGENCE.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "An attack path is a plausible multi-step sequence linking entities—assets, identities, exposures—showing how compromise could propagate; structural analysis, not proof of active attack."
---

# Attack Path

## Definition

An **attack path** is a plausible **multi-step sequence** linking entities—assets, identities, exposures, and related objects—showing how compromise could propagate through an environment. Paths support investigation and prioritization; they are **structural hypotheses**, not proof that an attack occurred.

Attack paths differ from generic network diagrams by incorporating security relationships and findings relevant to feasibility.

## SentriScope Usage

Attack path intelligence capability: `KID-AGR-0001`. Used within investigation context: `KID-INV-0001`.

## Related Terms

- [Investigation](./INVESTIGATION.md) — `KID-GLS-0002`
- [Correlation](./CORRELATION.md) — `KID-GLS-0013`

## Related Knowledge

- [Understanding Attack Paths](../knowledge/UNDERSTANDING_ATTACK_PATHS.md) — `KID-CON-0040`
- [Attack Paths as Decision Support](../knowledge/ATTACK_PATHS_AS_DECISION_SUPPORT.md) — `KID-CON-0049`
- [SER-004 Attack Paths](../knowledge/SERIES_004_ATTACK_PATHS.md)
- [FAQ: What is an attack path?](../faq/FAQ_WHAT_IS_AN_ATTACK_PATH.md) — `KID-FAQ-0002`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_ATTACK_PATH_INTELLIGENCE.md` | Path concept (sanitized) |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.1 | 2026-07-03 | SER-004 series links |
| 1.0 | 2026-07-02 | Initial glossary authority |
