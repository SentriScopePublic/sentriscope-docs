---
title: "Investigation Prioritization"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0024
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0003
    - KID-CON-0027
    - KID-CON-0019
  related_to:
    - KID-CON-0023
    - KID-CON-0004
  authority_reference:
    - KID-OIN-0001
navigation:
  knowledge_series: SER-002
  editorial_season: SEA-001
  pillar_page: PIL-INVESTIGATION
  learning_path: LP-002
  search_intent_ids: [SI-008]
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0019
    - KID-GLS-0003
  recommended_next:
    - KID-CON-0023
    - KID-CON-0008
website_slug: investigation-prioritization
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Investigation prioritization ranks which inquiries deserve analyst depth next—using context, evidence quality gaps, and decision stakes—not FIFO queues or severity alone."
knowledge_tags: [investigation, prioritization, education]
---

# Investigation Prioritization

## What practitioners need to know

Not every investigation deserves equal depth at equal urgency. **Prioritization** allocates analyst attention where **context and stakes** justify it.

Practitioners ask: *Which investigation do I pick up next?* *Why are we deep-diving low-impact alerts?*

## Prioritization factors

| Factor | Question |
|--------|----------|
| **Business context** | What asset or data is at risk? (`KID-GLS-0003`) |
| **Evidence confidence gap** | High impact + low confidence → prioritize validation |
| **Active vs historical** | Live intrusion beats last month's scan finding |
| **Corroboration strength** | Multi-source signals may jump queue |
| **Regulatory / legal exposure** | Compliance-driven urgency |
| **Queue age** | SLA pressure—secondary to context |

[Evidence prioritization](./EVIDENCE_PRIORITIZATION.md) (`KID-CON-0027`) ranks **observations**; investigation prioritization ranks **inquiries**.

## Industry context

Operational intelligence (`KID-OIN-0001`) helps teams rank attention at scale. Without context, FIFO and severity-only sorts dominate—see [Why Security Tools Generate Too Many Findings](./WHY_SECURITY_TOOLS_GENERATE_TOO_MANY_FINDINGS.md) (`KID-CON-0004`).

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Severity-only queues | Context-blind deep dives |
| Never reprioritizing | Stale priorities |
| Equal depth on all alerts | Analyst burnout |
| Ignoring executive asks without evidence | Both bias and noise |

## Practical implications

1. **Tier investigations** (quick triage vs deep dive vs executive).  
2. **Re-score when new evidence arrives**.  
3. **Cap parallel deep investigations** per analyst.  
4. **Align with operational intelligence** where available.  

## Limitations

Prioritization is imperfect under uncertainty. Document **deferred** investigations with rationale and revisit triggers.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0027 | [Evidence Prioritization](./EVIDENCE_PRIORITIZATION.md) |
| KID-CON-0003 | [Context Matters More Than Severity](./CONTEXT_MATTERS_MORE_THAN_SEVERITY.md) |
| KID-GLS-0003 | [Security Context](../glossary/SECURITY_CONTEXT.md) |

## Authority references

- `KID-OIN-0001` — [Operational Intelligence](../intelligence/OPERATIONAL_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-002 article |
