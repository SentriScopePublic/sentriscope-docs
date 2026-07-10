---
title: "Threat Intelligence as Decision Support"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0058
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0050
    - KID-CON-0055
    - KID-GLS-0023
  synthesizes:
    - KID-CON-0050
    - KID-CON-0051
    - KID-CON-0052
    - KID-CON-0053
    - KID-CON-0054
    - KID-CON-0055
    - KID-CON-0056
    - KID-CON-0057
  related_to:
    - KID-GLS-0024
  authority_reference:
    - KID-TIN-0001
navigation:
  knowledge_series: SER-005
  pillar_page: PIL-THREAT-INTEL
  learning_path: LP-005
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 10
  required_reading:
    - KID-CON-0055
  recommended_next:
    - KID-CON-0060
website_slug: threat-intelligence-as-decision-support
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Synthesis: organizations transform threat intelligence into actionable security decisions by contextualizing external knowledge—not by consuming feeds or replacing evidence and risk analysis."
knowledge_tags: [threat-intelligence, decision-support, education]
---

# Threat Intelligence as Decision Support

## What practitioners need to know

This article closes SER-005 with the **core thesis**: organizations transform threat intelligence into **actionable security decisions**—not into feed subscriptions or dashboard volume.

## The decision-support model

```text
Internal evidence + Risk context + External TI context
                        ↓
              Prioritized, explainable action
```

| Principle | Meaning |
|-----------|---------|
| **TI provides external context** | Campaigns, TTPs, exploitation status |
| **TI is not detection** | Complement sensors (`KID-CON-0051`) |
| **TI is not proof of breach** | Investigate and validate |
| **TI does not replace risk analysis** | Enriches rank (`KID-CON-0031`) |
| **TI requires confidence and relevance** | `KID-GLS-0024`, `KID-CON-0053` |
| **TI has limits** | `KID-CON-0057` |

Term: [Decision Support](../glossary/DECISION_SUPPORT.md) (`KID-GLS-0023`).

## Curriculum position

| Volume / Series | Contribution |
|-----------------|--------------|
| VOL-001 SER-001–004 | Evidence, investigation, risk, structure |
| **VOL-002 SER-005** | **External knowledge → decisions** |
| VOL-002 SER-006 | Internal knowledge → decisions (next) |
| VOL-002 SER-007 | Integrated intelligence (synthesis) |

## Operating checklist

Before acting on intelligence:

1. ☐ Is relevance to our estate established?  
2. ☐ Is confidence acceptable and documented?  
3. ☐ Does risk analysis agree or conflict—documented?  
4. ☐ Is investigation evidence required first?  
5. ☐ Is residual risk stated after action?  

## Practical implications

- **Embed** TI in triage, patch, and hunt runbooks.  
- **Train** with misconceptions article (`KID-CON-0054`) first.  
- **Prepare** for SER-006 operational intelligence as the internal counterpart.  

## Limitations

Decision support quality depends on source curation, mapping, and analyst skill—technology alone does not operationalize intelligence.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-GLS-0005 | [Threat Intelligence](../glossary/THREAT_INTELLIGENCE.md) |
| KID-CON-0054 | [Common Misconceptions About Threat Intelligence](./COMMON_MISCONCEPTIONS_ABOUT_THREAT_INTELLIGENCE.md) |

## Authority references

- `KID-TIN-0001` — [Threat Intelligence](../intelligence/THREAT_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-005 synthesis article |
