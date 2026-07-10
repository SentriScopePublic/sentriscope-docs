---
title: "Attack Paths and Business Impact"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0046
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0045
    - KID-CON-0032
  related_to:
    - KID-GLS-0022
  authority_reference:
    - KID-ARC-0001
navigation:
  knowledge_series: SER-004
  pillar_page: PIL-ATTACK-PATH
  learning_path: LP-004
  difficulty: intermediate
  audience: [analyst, soc_manager, executive]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0045
  recommended_next:
    - KID-CON-0047
website_slug: attack-paths-and-business-impact
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Connect attack paths to business impact by anchoring path endpoints to asset criticality, blast radius, and service dependencies—not technical hop counts alone."
knowledge_tags: [attack-path, business-impact, education]
---

# Attack Paths and Business Impact

## What practitioners need to know

Executives do not fund **hop counts**—they fund **impact reduction**.

Practitioners ask: *How do I explain why this path matters to the business?*

Anchor paths to **what could be lost or disrupted** if the sequence succeeds.

## Linking paths to impact

| Path element | Business question |
|--------------|-------------------|
| **Terminal node** | What service or data lives here? |
| **Blast radius** | How many users or systems downstream? |
| **Identity hop** | What administrative or financial access? |
| **Recovery time** | How long if this path succeeds? |
| **Regulatory exposure** | PII, PHI, PCI on path? |

See [Blast Radius](../glossary/BLAST_RADIUS.md) (`KID-GLS-0022`) and [Risk Communication](./RISK_COMMUNICATION.md) (`KID-CON-0033`).

## Communication pattern

1. **One sentence**: path from X to **business asset Y**.  
2. **Impact**: revenue, customer, legal, or safety consequence.  
3. **Proposed action**: fix or control with expected path reduction.  
4. **Residual**: what remains after fix.  

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Technical path dump to executives | Disengagement |
| Missing asset tier on terminal node | Wrong narrative |
| Impact without remediation ask | No decision |
| Overstating certainty | Credibility loss |

## Practical implications

Use path analysis to **translate** technical reachability into the same language as risk communication—not a separate executive story.

## Limitations

Business impact models may lag technical graphs. Reconcile with asset owners when tiers disagree.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-GLS-0022 | [Blast Radius](../glossary/BLAST_RADIUS.md) |
| KID-CON-0035 | [Business Context in Risk Decisions](./BUSINESS_CONTEXT_IN_RISK_DECISIONS.md) |

## Authority references

- `KID-ARC-0001` — asset and entity model

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-004 article |
