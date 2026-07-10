---
title: "What is evidence in a security investigation?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0009
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0010
  - KID-CON-0001
  - KID-GLS-0001
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
    - KID-CON-0010
  explains:
    - KID-GLS-0001
  authority_reference:
    - KID-INV-0001
website_slug: faq-what-is-evidence-in-investigation
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "In a security investigation, evidence is validated, provenance-bearing information that supports or contradicts a specific hypothesis—not raw alerts or unverified claims."
---

# What is evidence in a security investigation?

## Short answer

In an investigation, **evidence** is validated information—with provenance—that **supports or contradicts** a specific hypothesis or conclusion you are testing.

## Explanation

Investigations start from questions or signals; evidence answers whether the hypothesis holds.

| Investigation stage | Evidence role |
|--------------------|---------------|
| Hypothesis formation | Defines what evidence would confirm/refute |
| Collection | Gathers candidate items with provenance |
| Analysis | Weighs supporting vs contradictory evidence |
| Conclusion | States outcome with confidence |

Term authority: [Evidence](../glossary/EVIDENCE.md) (`KID-GLS-0001`). Methodology: [Evidence-Based Investigation](../knowledge/EVIDENCE_BASED_INVESTIGATION.md) (`KID-CON-0001`).

## Common mistake

Closing investigations when alerts are cleared without documenting evidentiary basis.

## Related

- [What Is Security Evidence?](../knowledge/WHAT_IS_SECURITY_EVIDENCE.md) — `KID-CON-0010`
- [Alert vs evidence](./FAQ_ALERT_VS_EVIDENCE.md) — `KID-FAQ-0001`

## Authority references

- `KID-INV-0001` — [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial FAQ — SER-001 |
