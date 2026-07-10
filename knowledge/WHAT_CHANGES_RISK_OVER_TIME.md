---
title: "What Changes Risk Over Time"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0036
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0032
    - KID-CON-0012
    - KID-GLS-0021
  explains:
    - KID-GLS-0021
  related_to:
    - KID-CON-0031
    - KID-CON-0034
  authority_reference:
    - KID-OIN-0001
navigation:
  knowledge_series: SER-003
  editorial_season: SEA-005
  pillar_page: PIL-RISK
  learning_path: LP-003
  search_intent_ids: [SI-008]
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0031
    - KID-CON-0032
  recommended_next:
    - KID-CON-0033
website_slug: what-changes-risk-over-time
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Risk is not static—exposure, threat activity, asset role, control changes, and evidence freshness all require re-prioritization and review of accepted residual risk."
knowledge_tags: [risk, monitoring, education]
---

# What Changes Risk Over Time

## What practitioners need to know

Practitioners ask: *What changes risk over time?* *We ranked this last month—why is it urgent now?*

**Risk is dynamic.** A deferred issue can become critical overnight; an urgent issue can become irrelevant after a control change. Static queues create **stale risk**.

Term: [Residual Risk](../glossary/RESIDUAL_RISK.md) (`KID-GLS-0021`)—what remains after fixes and acceptances—**requires monitoring**.

## Change triggers

| Trigger | Effect on risk |
|---------|----------------|
| **New exposure** | Internal → internet-facing |
| **Threat escalation** | KEV added, active campaign |
| **Asset role change** | Lab promoted to production |
| **Control change** | WAF removed, MFA disabled |
| **Evidence refresh** | Validation disproves mitigation |
| **Acceptance expiry** | Deferred item due for review |
| **Patch deployment** | Risk reduced; re-rank siblings |

Link to [evidence freshness](./EVIDENCE_FRESHNESS.md) (`KID-CON-0012`)—stale context produces stale rank.

## Industry context

Point-in-time assessments (annual pentest, quarterly scan) snapshot risk. Continuous programs **re-rank** on triggers—preview of operational intelligence (SER-006) and threat intelligence (SER-005) as inputs.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Set-and-forget queue | Surprise incidents |
| No acceptance review dates | Permanent deferrals |
| Ignore threat feed updates | Miss exploitation wave |
| Re-rank without communication | Stakeholder confusion |

## Practical implications

1. **Define re-rank triggers** in policy.  
2. **Automate watchlists** for accepted high-residual items.  
3. **Log rank history** with reason codes.  
4. **Integrate threat and exposure change feeds** into review cadence.  

## Limitations

Continuous re-ranking can cause churn. Balance **trigger-based** review with periodic full queue hygiene.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0032 | [Risk Acceptance](./RISK_ACCEPTANCE.md) |
| KID-GLS-0021 | [Residual Risk](../glossary/RESIDUAL_RISK.md) |
| KID-CON-0034 | [Why Severity Alone Is Insufficient](./WHY_SEVERITY_ALONE_IS_INSUFFICIENT.md) |

## Authority references

- `KID-OIN-0001` — continuous operational reprioritization

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-003 article |
