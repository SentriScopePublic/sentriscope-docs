---
term: "Provenance"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0014
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0014
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
  related_to:
    - KID-GLS-0016
    - KID-GLS-0017
  authority_reference:
    - KID-INV-0001
    - KID-ARC-0001
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_INVESTIGATION_EVIDENCE_WORKSPACE.md
last_updated: 2026-07-02
next_review: 2027-01-02
llm_summary: "Provenance is the documented origin and handling history of security evidence—source system, collection time, method, and transformations—enabling validation and audit."
---

# Provenance

## Definition

**Provenance** is the documented **origin and handling history** of a piece of security evidence: which system produced it, when it was collected, how it was obtained, and what transformations (filtering, enrichment, export) were applied.

Without provenance, information cannot be fully validated or reproduced.

## SentriScope Usage

SentriScope treats provenance as a first-class attribute of evidence in investigation workflows. Product behavior is defined in `KID-INV-0001` and entity modeling in `KID-ARC-0001`. This entry is the term authority—product documents reference this KID.

## Related Terms

- [Evidence](./EVIDENCE.md) — `KID-GLS-0001`
- [Chain of Custody](./CHAIN_OF_CUSTODY.md) — `KID-GLS-0016`
- [Evidence Integrity](./EVIDENCE_INTEGRITY.md) — `KID-GLS-0017`

## Related Knowledge

- [Evidence Provenance](../knowledge/EVIDENCE_PROVENANCE.md) — `KID-CON-0011`
- [FAQ: What is evidence provenance?](../faq/FAQ_WHAT_IS_EVIDENCE_PROVENANCE.md) — `KID-FAQ-0007`

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_INVESTIGATION_EVIDENCE_WORKSPACE.md` | Evidence provenance concepts |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial glossary authority |
