---
term: "Operational Feedback"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0041
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0041
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0040
    - KID-GLS-0023
    - KID-GLS-0026
    - KID-GLS-0019
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Operational feedback is structured learning from daily security decisions—outcomes, deferrals, and rank changes—that improves future prioritization and intelligence use without replacing investigation or audit."
---

# Operational Feedback

## Definition

**Operational feedback** is **structured learning from daily security decisions**—including outcomes of prioritization, deferrals, coordination handoffs, and rank changes—that improves how teams apply [Security Intelligence](./SECURITY_INTELLIGENCE.md) and make future [operational decisions](./OPERATIONAL_DECISION.md).

Feedback captures what happened after a judgment (was the deferral justified? did intelligence shift rank?) and feeds the next operational cycle. It is not incident post-mortem alone, compliance checkboxing, or metric dashboards without decision context.

## SentriScope Usage

SentriScope supports operational feedback by linking decision rationale to entity and intelligence context so teams can review whether past judgments remain defensible when conditions change. This entry defines the term only.

## Related terms

- [Operational Decision](./OPERATIONAL_DECISION.md) — `KID-GLS-0040`
- [Decision Support](./DECISION_SUPPORT.md) — `KID-GLS-0023`
- [Operational Signal](./OPERATIONAL_SIGNAL.md) — `KID-GLS-0026`
- [Disposition](./DISPOSITION.md) — `KID-GLS-0019`

## Related Knowledge

- [Operational Feedback](../knowledge/OPERATIONAL_FEEDBACK.md) — `KID-CON-0136`
- [Operational Decision Cycles](../knowledge/OPERATIONAL_DECISION_CYCLES.md) — `KID-CON-0131`
- [FAQ: What is operational feedback?](../faq/FAQ_WHAT_IS_OPERATIONAL_FEEDBACK.md) — `KID-FAQ-0070`
- [SER-013 Security Operations](../knowledge/SERIES_013_SECURITY_OPERATIONS.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-013) |
