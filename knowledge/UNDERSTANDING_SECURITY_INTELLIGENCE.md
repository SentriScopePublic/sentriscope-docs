---
title: "Understanding Security Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0070
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0028
    - KID-CON-0058
    - KID-CON-0068
    - KID-CON-0030
  explains:
    - KID-GLS-0028
  related_to:
    - KID-CON-0071
    - KID-CON-0072
  authority_reference:
    - KID-TIN-0001
    - KID-OIN-0001
navigation:
  knowledge_series: SER-007
  editorial_season: SEA-005
  pillar_page: PIL-SECURITY-INTEL
  learning_path: LP-007
  difficulty: introductory
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0058
    - KID-CON-0068
    - KID-GLS-0028
  recommended_next:
    - KID-CON-0071
website_slug: understanding-security-intelligence
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Security intelligence integrates external threat knowledge and internal operational knowledge with evidence and risk context to support explainable security decisions—not a third feed or autonomous SOC."
knowledge_tags: [security-intelligence, decision-support, education]
---

# Understanding Security Intelligence

## What practitioners need to know

Practitioners ask: *We have threat feeds and internal dashboards—what is security intelligence?* *Is it just TI plus OI?*

**Security intelligence** is how organizations **integrate** external threat knowledge and internal operational knowledge into a **unified decision process**—with evidence and risk context as non-negotiable anchors.

Term authority: [Security Intelligence](../glossary/SECURITY_INTELLIGENCE.md) (`KID-GLS-0028`).

## Volume 2 capstone position

```text
SER-005 Threat Intelligence      → external knowledge → decisions
SER-006 Operational Intelligence → internal knowledge → decisions
SER-007 Security Intelligence    → integrated knowledge → decisions
```

Volume 1 supplies the analytical foundation: evidence, investigation, risk, and attack paths. Volume 2 teaches how intelligence **feeds** those disciplines—not replaces them.

## What security intelligence is

| Security intelligence is | Security intelligence is not |
|--------------------------|------------------------------|
| Integrated decision support | A merged intelligence platform SKU |
| Explainable recommendations with reasons | Black-box priority scores |
| TI + OI + evidence + risk in one process | Feed volume or dashboard count |
| Practitioner judgment with context | Autonomous SOC |
| Auditable rationale for stakeholders | Marketing "AI security brain" |

## The integration model

```text
Threat intelligence (external)  ──┐
Operational intelligence (internal) ├──→ Security intelligence → Decision
Evidence + Risk context (Volume 1) ─┘
```

Each input **constrains** the others:

- TI without internal mapping → irrelevant urgency  
- OI without external context → missed campaign relevance  
- Intelligence without evidence → premature action  
- Intelligence without risk context → wrong business trade-offs  

## Connection to decision support

[Decision support](../glossary/DECISION_SUPPORT.md) (`KID-GLS-0023`) means intelligence **informs** choices; humans remain accountable. Security intelligence operationalizes that principle across intelligence types.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Treating SI as a product category | Buying tools without integration process |
| Stacking TI and OI without reconciliation | Contradictory priorities |
| Skipping Volume 1 foundations | Intelligence without evidence discipline |
| Equating integration with automation | Fast wrong decisions |
| One team owns "all intelligence" | Silos persist under new label |

## Practical implications

1. **Map current TI and OI outputs** to specific decisions (triage, patch, hunt, escalate).  
2. **Document where ranks diverge** today—that is the integration starting point.  
3. **Require reason codes** that cite intelligence type and confidence.  

## Limitations

Security intelligence quality depends on source curation, inventory accuracy, analyst skill, and governance—not on renaming existing feeds "integrated intelligence."

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0036 | [What is security intelligence?](../faq/FAQ_WHAT_IS_SECURITY_INTELLIGENCE.md) |
| KID-CON-0077 | [Security Intelligence as Decision Support](./SECURITY_INTELLIGENCE_AS_DECISION_SUPPORT.md) |
| KID-CON-0058 | [Threat Intelligence as Decision Support](./THREAT_INTELLIGENCE_AS_DECISION_SUPPORT.md) |
| KID-CON-0068 | [Operational Intelligence as Decision Support](./OPERATIONAL_INTELLIGENCE_AS_DECISION_SUPPORT.md) |

## Authority references

- `KID-TIN-0001` — [Threat Intelligence](../intelligence/THREAT_INTELLIGENCE.md)
- `KID-OIN-0001` — [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-007 article |
