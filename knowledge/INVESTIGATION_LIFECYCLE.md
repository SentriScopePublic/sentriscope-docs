---
title: "Investigation Lifecycle"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0019
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0002
    - KID-CON-0001
    - KID-CON-0005
    - KID-CON-0010
  related_to:
    - KID-CON-0020
    - KID-CON-0026
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-002
  editorial_season: SEA-001
  pillar_page: PIL-INVESTIGATION
  learning_path: LP-002
  search_intent_ids: [SI-006]
  difficulty: introductory
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0001
    - KID-CON-0005
  recommended_next:
    - KID-CON-0020
    - KID-CON-0021
website_slug: investigation-lifecycle
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "The investigation lifecycle moves from trigger through scoping, hypothesis, evidence collection, analysis, decision, documentation, and closure—with explicit gates for validation and handoff."
knowledge_tags: [investigation, lifecycle, education]
---

# Investigation Lifecycle

## What practitioners need to know

Practitioners ask: *What are the steps of a security investigation?* *Where do most investigations fail?*

The **investigation lifecycle** is a repeatable sequence from trigger to closure. It connects [evidence-based practice](./EVIDENCE_BASED_INVESTIGATION.md) (`KID-CON-0001`) to operational outcomes—not a rigid waterfall, but a **discipline** teams can audit.

Term authority: [Investigation](../glossary/INVESTIGATION.md) (`KID-GLS-0002`).

## Lifecycle phases

| Phase | Purpose | Common failure |
|-------|---------|----------------|
| **1. Trigger** | Signal or question initiates work | Wrong scope from start |
| **2. Scope** | Define boundaries (time, assets, users) | Scope creep or too narrow |
| **3. Hypothesis** | State what you are testing | Implicit assumptions |
| **4. Evidence collection** | Gather with provenance | Alert closure without proof |
| **5. Analysis** | Weigh supporting/contradictory evidence | Confirmation bias |
| **6. Decision** | Conclude or escalate with confidence | Severity-driven action |
| **7. Documentation** | Preserve reasoning for handoff/audit | Tribal knowledge only |
| **8. Closure** | Disposition with outcome recorded | Ticket closed, question open |

Phases **iterate**—new evidence may reopen hypothesis or scope.

## Industry context

NIST and SANS frameworks describe incident phases; investigation lifecycle emphasizes **analytical** work that may run parallel to IR. Mature SOCs embed lifecycle checkpoints in tooling—not only in runbooks.

Concept map (planned): MAP-003 Investigation lifecycle.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Skipping hypothesis | Unfocused collection |
| No scope document | Endless investigation |
| Closure without documentation | Repeat incidents |
| Single-pass analysis | Missed contradictory evidence |

## Practical implications

1. **Define phase exit criteria** — e.g., analysis complete when confidence tier met or escalation triggered.  
2. **Allow reopen** — closure is not necessarily final.  
3. **Align with evidence lifecycle** (`KID-CON-0015`) for collection and validation.  
4. **Separate IR phases** when active containment dominates (`KID-CON-0005`).  

## Limitations

Lifecycle rigor should match stakes—a suspicious login may use a lightweight path; active breach uses full phases. Over-process slows response; under-process loses defensibility.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0020 | [Investigation Hypothesis](./INVESTIGATION_HYPOTHESIS.md) |
| KID-CON-0026 | [Investigation Documentation](./INVESTIGATION_DOCUMENTATION.md) |
| KID-FAQ-0011 | [What is the investigation lifecycle?](../faq/FAQ_WHAT_IS_INVESTIGATION_LIFECYCLE.md) |

## Authority references

- `KID-INV-0001` — [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md)

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-002 article |
