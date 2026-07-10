---
term: "Decision Support"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-GLS-0023
knowledge_domain: glossary
knowledge_object: glossary
is_authority: true
authority_document: KID-GLS-0023
knowledge_lifecycle: validated
documentation_maturity: D1
knowledge_relationships:
  related_to:
    - KID-GLS-0011
    - KID-GLS-0018
  explains:
    - KID-CON-0049
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Decision support provides structured context—such as attack paths or risk analysis—to help practitioners choose actions; it informs judgment rather than replacing it."
---

# Decision Support

## Definition

**Decision support** is **structured context** that helps practitioners choose security actions with clearer rationale. It **informs judgment**; it does not replace human accountability or operational policy.

Examples in this library: attack path models, risk context layers, investigation hypotheses.

## What decision support is not

| Not decision support | Why |
|---------------------|-----|
| Automated verdict | Removes accountability |
| Raw data dump | No prioritization logic |
| Compliance checkbox | Policy ≠ contextual priority |
| Proof of breach | Hypothesis until validated |

## SentriScope usage

Attack path intelligence (`KID-AGR-0001`) and risk intelligence workflows provide decision-support inputs within tenant investigation and prioritization contexts.

## Related terms

- [Attack Path](./ATTACK_PATH.md) — `KID-GLS-0011`
- [Risk Intelligence](./RISK_INTELLIGENCE.md) — `KID-GLS-0018`

## Related knowledge

- [Attack Paths as Decision Support](../knowledge/ATTACK_PATHS_AS_DECISION_SUPPORT.md) — `KID-CON-0049`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial glossary authority (SER-004) |
