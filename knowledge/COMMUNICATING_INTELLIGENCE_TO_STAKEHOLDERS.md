---
title: "Communicating Intelligence to Stakeholders"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0075
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0033
    - KID-CON-0070
    - KID-GLS-0024
  related_to:
    - KID-CON-0073
    - KID-CON-0076
  authority_reference:
    - KID-GLS-0028
navigation:
  knowledge_series: SER-007
  pillar_page: PIL-SECURITY-INTEL
  learning_path: LP-007
  difficulty: intermediate
  audience: [analyst, soc_manager, executive]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0070
  recommended_next:
    - KID-CON-0076
website_slug: communicating-intelligence-to-stakeholders
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Stakeholder communication translates integrated intelligence into decisions, confidence levels, and residual risk—not raw feeds, IoC lists, or technical jargon."
knowledge_tags: [security-intelligence, communication, education]
---

# Communicating Intelligence to Stakeholders

## What practitioners need to know

Stakeholders—executives, risk owners, legal, communications—need **decisions and rationale**, not intelligence volume. Effective communication translates integrated TI and OI into **business language** with explicit confidence and residual risk.

Extend [Risk Communication](./RISK_COMMUNICATION.md) (`KID-CON-0033`) to intelligence-specific narratives.

## Audience-appropriate framing

| Audience | Lead with | Avoid |
|----------|-----------|-------|
| **Executive** | Decision required, business impact, timeline | IoC dumps, ATT&CK technique IDs |
| **Risk owner** | Residual risk, compensating controls | Unqualified "critical threat" |
| **Legal / compliance** | Evidence status, regulatory exposure | Speculative attribution |
| **Technical peers** | Integration rationale, conflicts resolved | Duplicate TI/OI briefings |
| **Communications** | Confirmed facts only | Preliminary intel leaks |

## Communication structure

```text
1. Decision or recommendation (one sentence)
2. Why now (integrated TI + OI summary)
3. Confidence level (KID-GLS-0024)
4. Evidence status (confirmed / investigating / assumed)
5. Residual risk if no action
6. Next update cadence
```

## Confidence and uncertainty

[Intelligence confidence](../glossary/INTELLIGENCE_CONFIDENCE.md) (`KID-GLS-0024`) must appear in stakeholder briefings:

| Confidence | Communication pattern |
|------------|----------------------|
| **High** | "We have validated …" |
| **Moderate** | "Intelligence indicates … we are confirming …" |
| **Low** | "Early reporting suggests … treat as hypothesis" |
| **Conflict** | "TI and internal state disagree—we are investigating …" |

Hiding uncertainty destroys trust faster than delayed escalation.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Forwarding vendor TI verbatim | Irrelevant panic |
| Separate TI and OI briefings | Contradictory narratives |
| Intelligence without evidence status | Overreaction or dismissal |
| Jargon without translation | Decision paralysis |
| No residual risk statement | Implied false safety |

## Practical implications

1. **Use a standard briefing template** with the six-part structure above.  
2. **Pre-brief risk owners** when integrated rank changes tier.  
3. **Document what intelligence was **not** acted on** and why.  

## Limitations

Communication skill does not substitute for integration quality—contradictory intelligence surfaces eventually regardless of presentation polish.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0039 | [How communicate intelligence to executives?](../faq/FAQ_HOW_COMMUNICATE_INTELLIGENCE_TO_EXECUTIVES.md) |
| KID-FAQ-0019 | [How analysts explain risk](../faq/FAQ_HOW_ANALYSTS_EXPLAIN_RISK.md) |
| KID-CON-0032 | [Risk Acceptance](./RISK_ACCEPTANCE.md) |

## Authority references

- `KID-GLS-0028` — [Security Intelligence](../glossary/SECURITY_INTELLIGENCE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-007 article |
