---
title: "Operational Intelligence and Investigations"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0065
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0019
    - KID-CON-0060
  related_to:
    - KID-CON-0056
    - KID-CON-0048
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-006
  pillar_page: PIL-OP-INTEL
  learning_path: LP-006
  difficulty: intermediate
  audience: [analyst]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0019
    - KID-CON-0064
  recommended_next:
    - KID-CON-0066
website_slug: operational-intelligence-and-investigations
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Operational intelligence helps investigators choose depth and sequence—ranking which inquiries deserve effort based on internal state, not replacing hypothesis validation."
knowledge_tags: [operational-intelligence, investigation, education]
---

# Operational Intelligence and Investigations

## What practitioners need to know

Investigations consume scarce analyst time. **Operational intelligence** helps choose **which investigations deserve depth now**—based on internal state, overlap, and operational impact.

OI **prioritizes investigation effort**; it does not replace [investigation discipline](./INVESTIGATION_LIFECYCLE.md) (`KID-CON-0019`).

## Integration points

| Investigation phase | OI contribution |
|--------------------|-----------------|
| **Intake** | Rank new cases against operational context |
| **Triage** | Surface related open items and asset tier |
| **Scoping** | Highlight coverage gaps affecting confidence |
| **Depth decision** | Escalate when OI + TI align |
| **Handoff** | Carry rank rationale forward |

Pair with [Threat Intelligence in Investigation](./THREAT_INTELLIGENCE_IN_INVESTIGATION.md) (`KID-CON-0056`) when external context applies.

## OI vs evidence

| OI says | Investigator must |
|---------|-------------------|
| High operational priority | Still validate with evidence |
| Related queue cluster | Confirm linkage in data |
| Control gap on asset | Verify current state |

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Close because rank dropped | Premature disposition |
| Ignore OI on complex cases | Under-scoped investigations |
| OI rank as investigation conclusion | Audit failure |

## Practical implications

Record **OI rank at investigation open** and **at disposition**—shows whether context changed outcomes.

## Limitations

Complex investigations may exceed what queue rank captures; senior judgment still applies.

## Authority references

- `KID-INV-0001` — investigation capability

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-006 article |
