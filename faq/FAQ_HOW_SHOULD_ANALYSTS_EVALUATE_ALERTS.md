---
title: "How should analysts evaluate alerts?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0010
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0017
  - KID-CON-0008
  - KID-FAQ-0001
knowledge_relationships:
  depends_on:
    - KID-FAQ-0001
    - KID-CON-0017
  related_to:
    - KID-CON-0029
  authority_reference:
    - KID-INV-0001
website_slug: faq-how-should-analysts-evaluate-alerts
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "Analysts evaluate alerts by scoping context, validating signals, converting validated observations to evidence, and deciding with explicit confidence—not by severity label alone."
---

# How should analysts evaluate alerts?

## Short answer

Evaluate alerts by: (1) scoping context, (2) validating the signal, (3) converting validated observations to evidence, and (4) deciding with explicit confidence—not by closing on severity alone.

## Explanation

Recommended flow:

1. **Triage** — acknowledge; form initial hypothesis  
2. **Contextualize** — link asset, identity, business impact  
3. **Validate** — replay queries; corroborate (`KID-CON-0029`)  
4. **Record evidence** — provenance + confidence  
5. **Decide** — action matched to quality bar  

Guides: [From Alerts to Evidence](../knowledge/FROM_ALERTS_TO_EVIDENCE.md) (`KID-CON-0017`), [From Alerts to Decisions](../knowledge/FROM_ALERTS_TO_DECISIONS.md) (`KID-CON-0008`).

## Common mistake

Bulk-closing alerts to meet SLA without answering whether the underlying risk was understood.

## Related

- [Alert vs evidence](./FAQ_ALERT_VS_EVIDENCE.md) — `KID-FAQ-0001`
- [Evidence Prioritization](../knowledge/EVIDENCE_PRIORITIZATION.md) — `KID-CON-0027`

## Authority references

- `KID-INV-0001` — investigation workspace

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial FAQ — SER-001 |
