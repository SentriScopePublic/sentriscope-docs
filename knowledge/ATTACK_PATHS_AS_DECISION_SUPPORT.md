---
title: "Attack Paths as Decision Support"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0049
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0040
    - KID-CON-0045
    - KID-CON-0031
  synthesizes:
    - KID-CON-0040
    - KID-CON-0041
    - KID-CON-0042
    - KID-CON-0043
    - KID-CON-0044
    - KID-CON-0045
    - KID-CON-0046
    - KID-CON-0047
    - KID-CON-0048
  related_to:
    - KID-GLS-0023
  authority_reference:
    - KID-AGR-0001
navigation:
  knowledge_series: SER-004
  pillar_page: PIL-ATTACK-PATH
  learning_path: LP-004
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 10
  required_reading:
    - KID-CON-0045
  recommended_next:
    - KID-CON-0030
website_slug: attack-paths-as-decision-support
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Synthesis: attack paths are decision-support tools providing structural context for prioritization, investigation scope, and stakeholder communication—not standalone findings or risk replacements."
knowledge_tags: [attack-path, decision-support, education]
---

# Attack Paths as Decision Support

## What practitioners need to know

This article closes SER-004 with the **core thesis**: organizations use attack paths to make **better security decisions**—not to collect prettier graphs.

## The decision-support model

```text
Findings + Context + Risk judgment
              ↓
      Attack path context
              ↓
   Prioritized, explainable action
```

| Principle | Meaning |
|-----------|---------|
| **Paths provide context** | Reachability, chains, choke points |
| **Paths are not findings** | Do not ticket the graph |
| **Paths are not vulnerabilities** | Complement CVE work (`KID-CON-0041`) |
| **Paths do not replace risk analysis** | Inform rank; human judgment remains |
| **Paths help prioritize action** | Sequence fixes and investigations |
| **Paths require validation** | Context + evidence (`KID-CON-0043`, `KID-CON-0048`) |
| **Paths have limits** | Know when to supplement (`KID-CON-0047`) |

Term: [Decision Support](../glossary/DECISION_SUPPORT.md) (`KID-GLS-0023`).

## Curriculum position

| Series | Contribution |
|--------|--------------|
| SER-001 Evidence | Trustworthy inputs to graph |
| SER-002 Investigation | Hypothesis validation discipline |
| SER-003 Risk Intelligence | Prioritization framework paths feed |
| **SER-004 Attack Paths** | **Structural context for decisions** |
| SER-005+ | Threat and operational layers build next |

## Operating checklist

Before acting on a path:

1. ☐ Is rank justified with context?  
2. ☐ Does risk analysis agree or conflict—documented?  
3. ☐ Is business impact articulated?  
4. ☐ Is investigation evidence required first?  
5. ☐ Is graph confidence acceptable?  
6. ☐ Is residual risk stated after action?  

## Common mistakes

Treating SER-004 as **graph theory training** misses the point. Success is measured in **better decisions**, not graph completeness.

## Practical implications

- **Embed** path review in triage, patch, and investigation runbooks.  
- **Train** stakeholders with misconceptions article (`KID-CON-0044`) first.  
- **Pause after SER-004** for architecture review: do SER-001–004 read as one coherent analytical workflow?  

## Limitations

Decision support quality depends on data, model, and analyst skill—technology alone does not mature prioritization.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-GLS-0011 | [Attack Path](../glossary/ATTACK_PATH.md) |
| KID-GLS-0023 | [Decision Support](../glossary/DECISION_SUPPORT.md) |
| KID-CON-0044 | [Common Misconceptions About Attack Paths](./COMMON_MISCONCEPTIONS_ABOUT_ATTACK_PATHS.md) |

## Authority references

- `KID-AGR-0001` — [Attack Graph Overview](../capabilities/ATTACK_GRAPH_OVERVIEW.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-004 synthesis article |
