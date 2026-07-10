---
term: "Evidence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0001
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0001
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-ARC-0001
  explains: []
  related_to:
    - KID-GLS-0002
    - KID-GLS-0008
  authority_reference:
    - KID-INV-0001
    - KID-ARC-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INVESTIGATION_EVIDENCE_WORKSPACE.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "Security evidence is verifiable information from integrated sources that supports or contradicts an analytical conclusion, with provenance—not an alert, score, or opinion by itself."
---

# Evidence

## Definition

**Evidence** is verifiable information drawn from integrated sources that supports or contradicts a security conclusion. Evidence carries **provenance** (where it came from, when it was observed) and is subject to analyst evaluation—not synonymous with an alert, a severity score, or an unsubstantiated claim.

Evidence may be supporting or contradictory. Mature investigation practices treat both as first-class inputs.

## SentriScope Usage

SentriScope models evidence as a canonical concept with governance and provenance. Investigation workflows are evidence-driven; product boundaries are defined in `KID-INV-0001` and entity definitions in `KID-ARC-0001`. This entry does not redefine those authorities.

## Related Terms

- [Investigation](./INVESTIGATION.md) — `KID-GLS-0002`
- [Finding](./FINDING.md) — `KID-GLS-0008`

## Related Knowledge

- [Evidence-Based Investigation](../knowledge/EVIDENCE_BASED_INVESTIGATION.md) — `KID-CON-0001`
- [FAQ: Alert vs evidence](../faq/FAQ_ALERT_VS_EVIDENCE.md) — `KID-FAQ-0001`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INVESTIGATION_EVIDENCE_WORKSPACE.md` | Evidence package and provenance concepts |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
