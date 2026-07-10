---
term: "Operational Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0006
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0006
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0005
    - KID-GLS-0013
  authority_reference:
    - KID-OIN-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "Operational intelligence is the practice of aggregating normalized security data into explainable prioritization—helping teams decide where to focus operational attention now."
---

# Operational Intelligence

## Definition

**Operational intelligence** is the practice of aggregating normalized security data into **explainable prioritization**—ranked attention with reason codes—so teams know **where to focus now**. It bridges raw findings from many tools and the decisions investigations and remediation require.

It differs from threat intelligence (external CTI focus) and from pure compliance reporting (static posture snapshots).

## SentriScope Usage

SentriScope operational intelligence capability: `KID-OIN-0001`. Platform layer context: `KID-PLT-0003`.

## Related Terms

- [Threat Intelligence](./THREAT_INTELLIGENCE.md) — `KID-GLS-0005`
- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`

## Related Knowledge

- [From Alerts to Decisions](../knowledge/FROM_ALERTS_TO_DECISIONS.md) — `KID-CON-0008`
- [SER-006 Operational Intelligence](../knowledge/SERIES_006_OPERATIONAL_INTELLIGENCE.md)
- [SER-007 Security Intelligence](../knowledge/SERIES_007_SECURITY_INTELLIGENCE.md)
- [FAQ: What is operational intelligence?](../faq/FAQ_WHAT_IS_OPERATIONAL_INTELLIGENCE.md) — `KID-FAQ-0003`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INTELLIGENCE.md` | Attention-point concept (sanitized) |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
