---
title: "When Attack Paths Are Not Enough"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0047
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0043
    - KID-CON-0038
  related_to:
    - KID-CON-0044
navigation:
  knowledge_series: SER-004
  pillar_page: PIL-ATTACK-PATH
  learning_path: LP-004
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0043
  recommended_next:
    - KID-CON-0048
website_slug: when-attack-paths-are-not-enough
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Attack paths do not replace threat intelligence, behavioral detection, policy compliance, or incomplete-inventory remediation—know when to supplement or override path guidance."
knowledge_tags: [attack-path, limitations, education]
---

# When Attack Paths Are Not Enough

## What practitioners need to know

Attack paths are powerful **context**—not a complete security program.

Practitioners ask: *When should I ignore or override path guidance?*

## Gaps paths do not cover

| Gap | What to use instead |
|-----|---------------------|
| **Active intrusion without graph signal** | Investigation + detection (`SER-002`) |
| **Zero-day with no mapped edge** | Threat intel + compensating controls |
| **Policy / compliance mandate** | GRC requirements (parallel track)  |
| **Data quality too poor** | Inventory remediation first |
| **Non-structural abuse** | Fraud, insider misuse, app logic |
| **Supply chain / third party** | Vendor risk outside graph scope |
| **Human / process failure** | Training, procedure—not path fix |

Parallel limits article: [When Attack Paths Are Not Enough](./WHEN_ATTACK_PATHS_ARE_NOT_ENOUGH.md) (`KID-CON-0047`). Risk series covers complementary prioritization limits in [Risk Prioritization in Practice](./RISK_PRIORITIZATION_IN_PRACTICE.md) (`KID-CON-0031`).

## Override signals

- Confirmed active compromise on non-path vector  
- Regulatory deadline unrelated to structure  
- Business-critical change window  
- Path confidence below team threshold  

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Path-only program | Blind spots |
| Ignoring paths entirely | Structural debt |
| Waiting for perfect graph | Paralysis |
| No escalation path for gaps | Analyst confusion |

## Practical implications

Define **explicit supplement triggers** in runbooks: when path output is insufficient, which parallel capability owns the decision.

## Limitations

This article sets boundaries for SER-004. SER-005 Threat Intelligence and SER-006 Operational Intelligence extend the stack.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0024 | [When should I ignore attack paths?](../faq/FAQ_WHEN_IGNORE_ATTACK_PATHS.md) |
| KID-CON-0048 | [Attack Paths in Investigation](./ATTACK_PATHS_IN_INVESTIGATION.md) |

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-004 article |
