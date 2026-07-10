---
term: "Chain of Custody"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0016
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0016
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-GLS-0014
  related_to:
    - KID-GLS-0017
  authority_reference:
    - KID-INV-0001
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "Chain of custody is the chronological record of who collected, handled, transferred, and stored security evidence—supporting integrity and legal defensibility."
---

# Chain of Custody

## Definition

**Chain of custody** is the **chronological record** documenting who collected, accessed, transferred, analyzed, and stored a piece of evidence—and when each action occurred.

It extends [Provenance](./PROVENANCE.md) with explicit **custodian accountability**, critical for legal, regulatory, and high-severity incident scenarios.

## SentriScope Usage

Routine SOC investigations may use lightweight provenance; legal hold or forensic escalation increases chain-of-custody rigor. Investigation governance: `KID-INV-0001`.

## Related Terms

- [Provenance](./PROVENANCE.md) — `KID-GLS-0014`
- [Evidence Integrity](./EVIDENCE_INTEGRITY.md) — `KID-GLS-0017`
- [Evidence](./EVIDENCE.md) — `KID-GLS-0001`

## Related Knowledge

- [Evidence Lifecycle](../knowledge/EVIDENCE_LIFECYCLE.md) — `KID-CON-0015`
- [Evidence in Audit and Compliance](../knowledge/EVIDENCE_IN_AUDIT_AND_COMPLIANCE.md) — `KID-CON-0018`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
