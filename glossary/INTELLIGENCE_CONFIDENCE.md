---
term: "Intelligence Confidence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0024
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0024
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0005
    - KID-GLS-0015
  explains:
    - KID-CON-0053
  authority_reference:
    - KID-TIN-0001
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Intelligence confidence expresses how much trust practitioners should place in a threat assessment—based on source quality, corroboration, freshness, and relevance—not on classification alone."
---

# Intelligence Confidence

## Definition

**Intelligence confidence** is the degree of **trust** practitioners assign to a threat assessment or indicator—based on **source quality**, **corroboration**, **freshness**, and **relevance** to the environment.

High confidence does not eliminate the need for internal validation. Low confidence does not mean ignore—it means investigate before escalating.

Distinct from [Evidence Confidence](./EVIDENCE_CONFIDENCE.md) (`KID-GLS-0015`), which applies to internal evidentiary artifacts.

## Usage in threat intelligence decisions

| Factor | Confidence effect |
|--------|-------------------|
| Multiple independent sources | Raise |
| Vendor / ISAC tier-1 reporting | Raise (with relevance check) |
| Stale or retracted indicator | Lower |
| No asset overlap | Lower relevance (may lower effective confidence) |

## Related terms

- [Threat Intelligence](./THREAT_INTELLIGENCE.md) — `KID-GLS-0005`
- [Evidence Confidence](./EVIDENCE_CONFIDENCE.md) — `KID-GLS-0015`

## Related knowledge

- [Context Matters in Threat Intelligence](../knowledge/CONTEXT_MATTERS_IN_THREAT_INTELLIGENCE.md) — `KID-CON-0053`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-005) |
