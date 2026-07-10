---
term: "Disposition"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0019
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0019
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-GLS-0008
    - KID-GLS-0002
  related_to:
    - KID-GLS-0001
  authority_reference:
    - KID-INV-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Disposition is the recorded handling outcome for an alert or finding—distinct from the investigation outcome or final security conclusion."
---

# Disposition

## Definition

**Disposition** is the **recorded handling outcome** for an alert, ticket, or finding—such as closed benign, closed resolved, escalated, or deferred.

Disposition describes **workflow state**. It is **not** identical to **investigation outcome** (whether the underlying security question was answered) or **risk acceptance**.

An alert may be dispositioned "closed" while the investigation outcome remains open—a common quality failure.

## SentriScope Usage

Investigation workflows distinguish alert handling from investigation conclusions. Reference: `KID-INV-0001`.

## Related Terms

- [Finding](./FINDING.md) — `KID-GLS-0008`
- [Investigation](./INVESTIGATION.md) — `KID-GLS-0002`
- [Evidence](./EVIDENCE.md) — `KID-GLS-0001`

## Related Knowledge

- [Investigation Documentation](../knowledge/INVESTIGATION_DOCUMENTATION.md) — `KID-CON-0026`
- [Investigation Decisions](../knowledge/INVESTIGATION_DECISIONS.md) — `KID-CON-0023`
- [From Alerts to Decisions](../knowledge/FROM_ALERTS_TO_DECISIONS.md) — `KID-CON-0008`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority — SER-002 |
