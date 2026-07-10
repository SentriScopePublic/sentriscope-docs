---
term: "Operational Context"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0027
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0027
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0003
    - KID-GLS-0006
  explains:
    - KID-CON-0063
  authority_reference:
    - KID-ARC-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Operational context is the live internal state—assets, controls, coverage, queue pressure—that shapes how operational intelligence ranks attention at a point in time."
---

# Operational Context

## Definition

**Operational context** is the **live internal state** of the security program at a point in time—asset posture, control effectiveness, identity state, coverage gaps, queue pressure, and data freshness—that shapes how [operational intelligence](./OPERATIONAL_INTELLIGENCE.md) ranks attention.

It **extends** [security context](./SECURITY_CONTEXT.md) (`KID-GLS-0003`) with **operational tempo**—what is true in the SOC **now**, not only in the CMDB baseline.

## Usage

| Context element | Decision effect |
|-----------------|-----------------|
| Control degradation | Raise related items |
| Maintenance window | Lower transient noise |
| Staffing constraint | Adjust depth expectations |
| Stale inventory | Lower confidence |

## Related terms

- [Security Context](./SECURITY_CONTEXT.md) — `KID-GLS-0003`
- [Operational Intelligence](./OPERATIONAL_INTELLIGENCE.md) — `KID-GLS-0006`

## Related knowledge

- [Why Context Changes Operational Decisions](../knowledge/WHY_CONTEXT_CHANGES_OPERATIONAL_DECISIONS.md) — `KID-CON-0063`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-006) |
