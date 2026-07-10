---
title: "Threat Intelligence vs Detection"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0051
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0050
    - KID-GLS-0008
  related_to:
    - KID-CON-0017
    - KID-CON-0054
  authority_reference:
    - KID-TIN-0001
navigation:
  knowledge_series: SER-005
  pillar_page: PIL-THREAT-INTEL
  learning_path: LP-005
  difficulty: introductory
  audience: [analyst]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0050
  recommended_next:
    - KID-CON-0052
website_slug: threat-intelligence-vs-detection
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Detection produces internal signals about events; threat intelligence provides external context about threats—complementary, not interchangeable."
knowledge_tags: [threat-intelligence, detection, education]
---

# Threat Intelligence vs Detection

## What practitioners need to know

Practitioners ask: *If we have TI, do we still need detection?* *Is an IoC hit the same as an EDR alert?*

**Detection** observes **your environment**. **Threat intelligence** describes **external threat activity**. Both inform decisions; neither replaces the other.

## Comparison

| Dimension | Detection | Threat intelligence |
|-----------|-----------|---------------------|
| **Source** | Internal telemetry | External research, feeds, sharing |
| **Question** | What happened here? | What are adversaries doing? |
| **Output** | Alerts, findings, events | Context, indicators, assessments |
| **Proof** | May support evidence | Does not prove local compromise |
| **Typical use** | Triage, investigation | Prioritization, hunt hypotheses |

See [From Alerts to Evidence](./FROM_ALERTS_TO_EVIDENCE.md) (`KID-CON-0017`) for alert discipline.

## When each matters

- **Detection-led**: confirmed malicious activity, live response  
- **Intelligence-led**: proactive prioritization, campaign awareness, patch urgency when exploitation is widespread  

Best programs **link** both: intelligence elevates which detections and findings deserve depth first.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| TI platform as SIEM replacement | Detection gaps |
| Ignoring TI on critical detections | Missed campaign context |
| IoC blocklist without tuning | False positives and blind spots |
| Detection without TI context | Flat prioritization |

## Practical implications

1. **Use TI to rank detection backlog**, not to replace sensors.  
2. **Investigate IoC matches** with evidence workflow (`KID-CON-0019`).  
3. **Do not close** on feed match alone (`KID-FAQ-0030`).  

## Limitations

Detection coverage gaps mean intelligence cannot compensate for missing visibility. Intelligence gaps mean detection may lack campaign context.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0027 | [Does threat intelligence replace detection?](../faq/FAQ_DOES_TI_REPLACE_DETECTION.md) |
| KID-GLS-0025 | [Threat Indicator](../glossary/THREAT_INDICATOR.md) |

## Authority references

- `KID-TIN-0001` — threat intelligence capability context

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-005 article |
