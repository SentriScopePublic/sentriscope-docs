---
title: "Understanding Threat Intelligence"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0050
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0005
    - KID-CON-0030
    - KID-CON-0049
  explains:
    - KID-GLS-0005
  related_to:
    - KID-CON-0051
    - KID-CON-0054
  authority_reference:
    - KID-TIN-0001
navigation:
  knowledge_series: SER-005
  editorial_season: SEA-003
  pillar_page: PIL-THREAT-INTEL
  learning_path: LP-005
  difficulty: introductory
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0030
    - KID-GLS-0005
  recommended_next:
    - KID-CON-0051
    - KID-CON-0054
website_slug: understanding-threat-intelligence
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Threat intelligence is validated external knowledge about threats used to enrich prioritization and investigation when correlated with internal context—not feed volume or automatic verdicts."
knowledge_tags: [threat-intelligence, education, decision-support]
---

# Understanding Threat Intelligence

## What practitioners need to know

Practitioners ask: *What is threat intelligence?* *Is it the same as IoC feeds?*

**Threat intelligence** is **validated external knowledge** about threats—actors, campaigns, techniques, and exploitation context. Its value appears when intelligence **changes a decision** in your environment, not when it fills a dashboard.

Term authority: [Threat Intelligence](../glossary/THREAT_INTELLIGENCE.md) (`KID-GLS-0005`).

## What threat intelligence is

| Threat intelligence is | Threat intelligence is not |
|------------------------|----------------------------|
| Decision-support context | Proof of compromise in your estate |
| Correlated external knowledge | Raw feed volume |
| Input to risk and investigation | Replacement for evidence |
| Confidence-scored assessments | Unverified social media rumors |
| Actionable when contextualized | Automatic ticket generation |

## Connection to Volume 1

| Prior series | Role |
|--------------|------|
| SER-001 Evidence | TI does not replace validated internal evidence |
| SER-002 Investigation | TI scopes hypotheses; investigation validates |
| SER-003 Risk Intelligence | TI enriches risk context layers |
| SER-004 Attack Paths | TI may elevate path relevance when exploitation is active |

## Industry context

Mature programs consume intelligence through **workflows**—prioritization, hunt hypotheses, investigation scope—not through inbox volume. Frameworks such as MITRE ATT&CK help **describe** techniques; they do not replace environment-specific judgment.

Educational focus: **interpretation and decisions**—not feed ingestion mechanics or vendor platform tours.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| TI without asset mapping | Irrelevant alerts |
| Treating IoC match as incident | False escalation |
| Ignoring intelligence confidence | Over-reaction to stale data |
| TI instead of patching known exposure | Theater over substance |

## Practical implications

1. **Ask what decision TI changes** before acting.  
2. **Map intelligence to your assets and paths** (`KID-CON-0043`).  
3. **Record confidence** when escalating (`KID-GLS-0024`).  
4. **Validate with evidence** before closure (`KID-CON-0029`).  

## Limitations

Threat intelligence reflects external visibility at a point in time. Absence of intelligence does not prove safety; presence does not prove breach.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0026 | [What is threat intelligence?](../faq/FAQ_WHAT_IS_THREAT_INTELLIGENCE.md) |
| KID-CON-0058 | [Threat Intelligence as Decision Support](./THREAT_INTELLIGENCE_AS_DECISION_SUPPORT.md) |

## Authority references

- `KID-TIN-0001` — [Threat Intelligence](../intelligence/THREAT_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-005 article |
