---
title: "Why Threat Intelligence Changes Priorities"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0052
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0050
    - KID-CON-0031
  related_to:
    - KID-CON-0042
    - KID-CON-0055
  authority_reference:
    - KID-TIN-0001
navigation:
  knowledge_series: SER-005
  pillar_page: PIL-THREAT-INTEL
  learning_path: LP-005
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0051
  recommended_next:
    - KID-CON-0055
website_slug: why-threat-intelligence-changes-priorities
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Threat intelligence changes priorities by surfacing active exploitation, campaign relevance, and technique prevalence that static severity sorting cannot reflect."
knowledge_tags: [threat-intelligence, prioritization, education]
---

# Why Threat Intelligence Changes Priorities

## What practitioners need to know

Practitioners ask: *Why did this CVE jump the queue after a TI report?* *The scanner rank did not change.*

Threat intelligence **adds time-sensitive external context**—active exploitation, targeted campaigns, technique relevance—that static severity and internal snapshots miss.

## Priority shift patterns

| Pattern | Example | Priority effect |
|---------|---------|-----------------|
| **Active exploitation** | KEV / vendor advisory confirms in-the-wild use | Raise |
| **Campaign targeting your sector** | Industry ISAC alert | Raise for matching controls |
| **Technique on prioritized path** | TI links TTP to attack path hop | Raise path review |
| **Stale / retracted intel** | IoC deprecated, low confidence | Lower |
| **Generic commodity malware** | No asset overlap | Lower |

Connect to [Risk Prioritization in Practice](./RISK_PRIORITIZATION_IN_PRACTICE.md) (`KID-CON-0031`) and [Why Attack Paths Change Priorities](./WHY_ATTACK_PATHS_CHANGE_PRIORITIES.md) (`KID-CON-0042`).

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Auto-promote every TI alert | Fatigue returns |
| Ignore TI on low-severity exposed assets | Missed exploitation window |
| No documented rationale | Stakeholder distrust |
| Static rank after intel refresh | Stale queue |

## Practical implications

1. **Document why TI changed rank** in ticket narrative.  
2. **Review TI-driven changes** in weekly triage.  
3. **Combine with risk context** (`KID-CON-0030`) and paths (`KID-CON-0043`).  
4. **Decay priority** when exploitation window closes.  

## Limitations

TI-driven urgency is only as good as source quality and asset mapping. Treat large rank swings as **hypothesis triggers** for validation.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0028 | [How does TI help prioritization?](../faq/FAQ_HOW_TI_HELPS_PRIORITIZATION.md) |

## Authority references

- `KID-TIN-0001` — threat intelligence capability

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-005 article |
