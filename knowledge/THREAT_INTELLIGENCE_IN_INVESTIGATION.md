---
title: "Threat Intelligence in Investigation"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0056
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0019
    - KID-CON-0050
    - KID-GLS-0002
  related_to:
    - KID-CON-0048
    - KID-CON-0053
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-005
  pillar_page: PIL-THREAT-INTEL
  learning_path: LP-005
  difficulty: intermediate
  audience: [analyst]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0019
    - KID-CON-0050
  recommended_next:
    - KID-CON-0057
website_slug: threat-intelligence-in-investigation
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "During investigation, threat intelligence helps scope hypotheses and prioritize log analysis—it supports investigation, not conclusions, until evidence confirms."
knowledge_tags: [threat-intelligence, investigation, education]
---

# Threat Intelligence in Investigation

## What practitioners need to know

Investigations ask: *What techniques should we expect?* *What else should we hunt?*

Threat intelligence provides **external hypotheses** for scope—not verdicts.

## Investigation integration points

| Phase | TI role |
|-------|---------|
| **Triage** | Campaign context for alert cluster |
| **Scoping** | TTPs suggest additional assets and identities |
| **Hypothesis** | Actor behavior models testable statements |
| **Evidence collection** | Targeted hunts for known techniques |
| **Disposition** | Confirm or retire TI-suggested scope |
| **Handoff** | Document validated vs assumed TI links |

Build on [Investigation Lifecycle](./INVESTIGATION_LIFECYCLE.md) (`KID-CON-0019`) and [Attack Paths in Investigation](./ATTACK_PATHS_IN_INVESTIGATION.md) (`KID-CON-0048`).

## TI vs evidence discipline

| TI suggests | Investigator must |
|-------------|-------------------|
| Technique in use | Find supporting telemetry |
| Actor infrastructure | Validate connections in logs |
| Sector campaign | Confirm relevance to your estate |
| IoC match | Distinguish true positive from collision |

**Never close investigation** on intelligence alone.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| TI as proof of attribution | Overconfident closure |
| Ignoring TI during scope creep | Missed related activity |
| Full ATT&CK walk under time pressure | Paralysis |

## Practical implications

1. **Attach top TI hypotheses** to investigation record.  
2. **Mark validated techniques** as evidence accrues.  
3. **Feed back** disproven intel assumptions to curation team.  

## Limitations

TI accelerates **where to look**—not **what happened**. Forensic and behavioral evidence lead conclusions.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-INV-0001 | [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md) |

## Authority references

- `KID-INV-0001` — investigation capability

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-005 article |
