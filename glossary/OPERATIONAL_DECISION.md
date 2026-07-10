---
term: "Operational Decision"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0040
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0040
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0023
    - KID-GLS-0028
    - KID-GLS-0027
    - KID-GLS-0041
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "An operational decision is a recurring security judgment—prioritize, defer, escalate, or coordinate—made under uncertainty using Security Intelligence, not a one-time incident command or tool default."
---

# Operational Decision

## Definition

An **operational decision** is a **recurring security judgment**—such as prioritizing a queue item, deferring work, escalating for investigation, or coordinating across functions—made during daily operations under uncertainty, using [Security Intelligence](./SECURITY_INTELLIGENCE.md) and entity context as [decision support](./DECISION_SUPPORT.md).

Operational decisions differ from incident command decisions: they happen continuously across shifts, apply intelligence to routine queues, and must remain explainable when conditions change. They are not tool defaults, severity sorts, or playbook steps executed without reasoning.

## SentriScope Usage

SentriScope surfaces operational decision context—exposure, correlation, entity linkage, and intelligence overlays—so analysts can document **why** a queue rank or deferral changed. This entry defines the term only.

## Related terms

- [Decision Support](./DECISION_SUPPORT.md) — `KID-GLS-0023`
- [Security Intelligence](./SECURITY_INTELLIGENCE.md) — `KID-GLS-0028`
- [Operational Context](./OPERATIONAL_CONTEXT.md) — `KID-GLS-0027`
- [Operational Feedback](./OPERATIONAL_FEEDBACK.md) — `KID-GLS-0041`

## Related Knowledge

- [Understanding Security Operations](../knowledge/UNDERSTANDING_SECURITY_OPERATIONS.md) — `KID-CON-0130`
- [Operational Decision Cycles](../knowledge/OPERATIONAL_DECISION_CYCLES.md) — `KID-CON-0131`
- [FAQ: What is Security Operations?](../faq/FAQ_WHAT_IS_SECURITY_OPERATIONS.md) — `KID-FAQ-0066`
- [SER-013 Security Operations](../knowledge/SERIES_013_SECURITY_OPERATIONS.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-013) |
