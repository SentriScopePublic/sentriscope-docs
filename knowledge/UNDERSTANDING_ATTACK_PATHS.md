---
title: "Understanding Attack Paths"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0040
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0011
    - KID-CON-0030
    - KID-CON-0031
  explains:
    - KID-GLS-0011
  related_to:
    - KID-CON-0041
    - KID-FAQ-0002
  authority_reference:
    - KID-AGR-0001
    - KID-ARC-0001
navigation:
  knowledge_series: SER-004
  editorial_season: SEA-002
  pillar_page: PIL-ATTACK-PATH
  learning_path: LP-004
  search_intent_ids: [SI-030]
  difficulty: introductory
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0030
    - KID-GLS-0011
  recommended_next:
    - KID-CON-0041
    - KID-CON-0044
website_slug: understanding-attack-paths
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Attack paths are decision-support models showing plausible multi-step compromise sequences through assets and identities—they provide context for prioritization, not proof of attack or replacement for risk analysis."
knowledge_tags: [attack-path, education, decision-support]
---

# Understanding Attack Paths

## What practitioners need to know

Practitioners ask: *What is an attack path?* *Is it the same as a network diagram?*

An **attack path** is a **decision-support model**—a plausible multi-step sequence showing how compromise could propagate through **assets**, **identities**, and **exposures**. It answers: *If something fails here, what could be reached?*

Term authority: [Attack Path](../glossary/ATTACK_PATH.md) (`KID-GLS-0011`).

## What attack paths are

| Attack paths are | Attack paths are not |
|------------------|----------------------|
| Structural hypotheses | Proof of active attack |
| Context for prioritization | Standalone findings |
| Multi-step reachability models | Single CVE records |
| Inputs to risk decisions | Replacement for risk analysis |
| Snapshot-bound views | Live attack telemetry |

## Connection to prior series

| Prior series | Role |
|--------------|------|
| SER-001 Evidence | Paths require validated entity linkage |
| SER-002 Investigation | Paths inform scope hypotheses |
| SER-003 Risk Intelligence | Paths **provide context** for rank—not the rank itself |

## Industry context

Attack path analysis emerged as environments grew too complex for flat vulnerability lists. Teams needed **reachability-aware** prioritization without claiming every edge equals imminent breach.

Educational focus: **interpretation and decisions**—not graph algorithms or path calculation mechanics.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Treating path as finding | False urgency |
| Ignoring model confidence | Over-remediation |
| Path without business context | Wrong fix order |
| Confusing visualization with analysis | Pretty graphs, no action |

## Practical implications

1. **Use paths to ask better questions** before remediation.  
2. **Combine with risk context** (`KID-CON-0030`).  
3. **Validate critical assumptions** with evidence (`KID-CON-0029`).  
4. **Document why a path changed priority** (`KID-CON-0042`).  

## Limitations

Paths reflect integrated data quality and model scope. Incomplete inventory produces incomplete paths—with explicit confidence, not false certainty.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-FAQ-0002 | [What is an attack path?](../faq/FAQ_WHAT_IS_AN_ATTACK_PATH.md) |
| KID-CON-0049 | [Attack Paths as Decision Support](./ATTACK_PATHS_AS_DECISION_SUPPORT.md) |

## Authority references

- `KID-AGR-0001` — [Attack Graph Overview](../capabilities/ATTACK_GRAPH_OVERVIEW.md)
- `KID-ARC-0001` — canonical entities on paths

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-004 article |
