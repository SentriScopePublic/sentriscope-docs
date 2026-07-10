---
title: "Attack Paths in Investigation"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0048
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0020
    - KID-CON-0040
    - KID-GLS-0002
  related_to:
    - KID-CON-0043
    - KID-CON-0047
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-004
  pillar_page: PIL-ATTACK-PATH
  learning_path: LP-004
  difficulty: intermediate
  audience: [analyst]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0020
    - KID-CON-0040
  recommended_next:
    - KID-CON-0049
website_slug: attack-paths-in-investigation
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "During investigation, attack paths help scope lateral movement hypotheses and validate reachability—they support hypotheses, not conclusions, until evidence confirms."
knowledge_tags: [attack-path, investigation, education]
---

# Attack Paths in Investigation

## What practitioners need to know

Investigations ask: *Where could the adversary go next?* Attack paths provide **structural hypotheses** for scope—not verdicts.

Practitioners ask: *When in the investigation lifecycle should I use paths?*

## Investigation integration points

| Phase | Path role |
|-------|-----------|
| **Triage** | Quick reachability check from alert asset |
| **Scoping** | Candidate lateral routes to validate |
| **Hypothesis** | Ranked paths as testable statements |
| **Evidence collection** | Targeted log/source pulls per hop |
| **Disposition** | Confirm or break assumed edges |
| **Handoff** | Document validated vs assumed hops |

Build on [Investigation Lifecycle](./INVESTIGATION_LIFECYCLE.md) (`KID-CON-0019`) and [Investigation Hypothesis](./INVESTIGATION_HYPOTHESIS.md) (`KID-CON-0020`).

## Path vs evidence discipline

| Path says | Investigator must |
|-----------|---------------------|
| Identity hop possible | Verify session / auth logs |
| Network edge exists | Confirm live connectivity |
| Vuln on node | Validate exploit attempt or presence |
| Terminal asset reachable | Check data access evidence |

**Never close investigation** on path alone.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Path as proof of lateral movement | False positive closure |
| Ignoring paths during scope creep | Missed assets |
| Full graph walk under time pressure | Analysis paralysis |
| No hop-level confidence notes | Weak handoff |

## Practical implications

1. **Attach top 3 path hypotheses** to investigation record.  
2. **Mark validated hops** as evidence accrues.  
3. **Escalate** when active signals align with high-rank path.  
4. **Update graph feedback** when investigation disproves edges.  

## Limitations

Paths accelerate **where to look**—not **what happened**. Behavioral and forensic evidence still lead conclusions.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-INV-0001 | [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md) |
| KID-CON-0023 | [Investigation Decisions](./INVESTIGATION_DECISIONS.md) |

## Authority references

- `KID-INV-0001` — investigation capability

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-004 article |
