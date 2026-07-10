---
term: "Finding"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0008
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0008
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0007
    - KID-GLS-0001
  authority_reference:
    - KID-ARC-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_DATA.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "A finding is a reported security condition from a tool or assessment—raw input that may become evidence after validation and contextualization, not a finished conclusion."
---

# Finding

## Definition

A **finding** is a reported security condition from a scanner, assessment, monitor, or manual review. Findings are **inputs** to analysis. They become **evidence** when validated, contextualized, and linked to an investigation or decision with provenance.

High finding volume does not equal high risk; many findings are duplicates, low context, or benign in specific environments.

## SentriScope Usage

Findings normalize into exposures and related canonical entities (`KID-ARC-0001`). Investigation treatment: `KID-INV-0001`.

## Related Terms

- [Exposure](./EXPOSURE.md) — `KID-GLS-0007`
- [Evidence](./EVIDENCE.md) — `KID-GLS-0001`

## Related Knowledge

- [Why Security Tools Generate Too Many Findings](../knowledge/WHY_SECURITY_TOOLS_GENERATE_TOO_MANY_FINDINGS.md) — `KID-CON-0004`
- [FAQ: Alert vs evidence](../faq/FAQ_ALERT_VS_EVIDENCE.md) — `KID-FAQ-0001`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
