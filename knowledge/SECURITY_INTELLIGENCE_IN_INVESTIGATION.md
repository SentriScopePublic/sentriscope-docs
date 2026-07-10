---
title: "Security Intelligence in Investigation"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0074
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0019
    - KID-CON-0071
    - KID-CON-0056
    - KID-CON-0065
  related_to:
    - KID-CON-0048
    - KID-GLS-0018
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-007
  pillar_page: PIL-SECURITY-INTEL
  learning_path: LP-007
  difficulty: intermediate
  audience: [analyst]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0019
    - KID-CON-0071
  recommended_next:
    - KID-CON-0075
website_slug: security-intelligence-in-investigation
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "In investigation, integrated security intelligence scopes hypotheses by combining external TTP context with internal operational state—evidence still leads conclusions."
knowledge_tags: [security-intelligence, investigation, education]
---

# Security Intelligence in Investigation

## What practitioners need to know

Investigations benefit when **external threat context** and **internal operational state** inform scope together—not when analysts toggle between separate tools mid-investigation.

Combine [Threat Intelligence in Investigation](./THREAT_INTELLIGENCE_IN_INVESTIGATION.md) (`KID-CON-0056`) and [Operational Intelligence and Investigations](./OPERATIONAL_INTELLIGENCE_AND_INVESTIGATIONS.md) (`KID-CON-0065`) under the [Investigation Lifecycle](./INVESTIGATION_LIFECYCLE.md) (`KID-CON-0019`).

## Investigation integration points

| Phase | TI contribution | OI contribution | Integrated outcome |
|-------|-----------------|-----------------|-------------------|
| **Triage** | Campaign context | Asset criticality, recent changes | Scoped urgency |
| **Hypothesis** | Expected TTPs | Related identities, peer alerts | Testable statements |
| **Scoping** | Actor infrastructure patterns | Blast radius, attack paths | Hunt targets |
| **Collection** | Technique-specific hunts | Normalized signal correlation | Efficient evidence gathering |
| **Disposition** | Retire external assumptions | Update operational rank | Closed with documented intel use |

## Intelligence vs evidence discipline

| Intelligence suggests | Investigator must |
|-----------------------|-------------------|
| Technique in active campaign | Find supporting telemetry |
| High-risk asset involvement | Validate connections |
| Related operational signals | Correlate with timeline |
| External IoC match | Rule out false positive |

**Never close** on integrated intelligence alone—[evidence validation](./EVIDENCE_VALIDATION.md) (`KID-CON-0029`) remains the bar.

## Attack path and investigation link

[Attack Paths in Investigation](./ATTACK_PATHS_IN_INVESTIGATION.md) (`KID-CON-0048`) provides structural context; security intelligence adds **why this path matters now** (campaign + internal state).

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| TI scope without OI asset check | Hunting wrong estate |
| OI cluster without TI technique context | Missed TTP patterns |
| Intelligence recorded as conclusion | Overconfident closure |
| Separate intel notes from investigation record | Handoff gaps |

## Practical implications

1. **Attach integrated intel summary** to investigation at open.  
2. **Mark validated vs unvalidated** intelligence assumptions as evidence accrues.  
3. **Feed disproven assumptions** back to TI curation and OI tuning.  

## Limitations

Integrated investigation support accelerates **where to look** and **what to expect**—forensic and behavioral evidence determine **what happened**.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-INV-0001 | [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md) |
| KID-CON-0020 | [Investigation Hypothesis](./INVESTIGATION_HYPOTHESIS.md) |
| KID-FAQ-0030 | [Does TI prove an attack?](../faq/FAQ_DOES_TI_PROVE_ATTACK.md) |

## Authority references

- `KID-INV-0001` — [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-007 article |
