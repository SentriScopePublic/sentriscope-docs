---
title: "How do I prioritize vulnerabilities?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0017
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0031
  - KID-CON-0030
  - KID-CON-0003
knowledge_relationships:
  depends_on:
    - KID-CON-0031
  explains:
    - KID-CON-0031
  authority_reference:
    - KID-OIN-0001
website_slug: faq-how-to-prioritize-vulnerabilities
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Prioritize vulnerabilities by enriching findings with risk context, validating evidence, combining threat signals, and documenting explainable rank rationale—not CVSS sort alone."
---

# How do I prioritize vulnerabilities?

## Short answer

Normalize findings to **assets**, enrich with **context** (exposure, tier, identity, threat), **validate** critical assumptions, rank with **explainable rationale**, and **re-rank** when context changes.

## Explanation

Step-by-step: [Risk Prioritization in Practice](../knowledge/RISK_PRIORITIZATION_IN_PRACTICE.md) (`KID-CON-0031`).

Evidence role: [How Evidence Influences Risk Prioritization](../knowledge/HOW_EVIDENCE_INFLUENCES_RISK_PRIORITIZATION.md) (`KID-CON-0038`).

## Related

- [Why Severity Alone Is Insufficient](../knowledge/WHY_SEVERITY_ALONE_IS_INSUFFICIENT.md) — `KID-CON-0034`

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ — SER-003 |
