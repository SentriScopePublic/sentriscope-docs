---
title: "Unknown Identities"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0095
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0094
  related_to:
    - KID-CON-0090
    - KID-CON-0029
    - KID-CON-0084
    - KID-GLS-0010
  authority_reference:
    - KID-ARC-0001
navigation:
  knowledge_series: SER-009
  editorial_season: SEA-007
  pillar_page: PIL-IDENTITY
  learning_path: LP-009
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0094
  recommended_next:
    - KID-CON-0096
website_slug: unknown-identities
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Unknown identities are decision uncertainty—not merely missing directory rows—because stale, orphaned, and unattributed service accounts weaken prioritization, investigation scope, and containment confidence."
knowledge_tags: [identity, unknown, uncertainty, education, security-entities]
---

# Unknown Identities

## What practitioners need to know

Practitioners ask: *We have authentication logs—why do we still have unknown identities?* *Isn't account cleanup someone else's problem?*

An **unknown identity** is any actor that security analysis **cannot reliably attribute or contextualize**—unmapped service principals, orphaned automation accounts, stale break-glass users, local application accounts with no owner, or log entries that lack a canonical identity link. Unknown identities create **uncertainty in decisions**, not just gaps in a directory export.

Foundation: [Identity Relationships](./IDENTITY_RELATIONSHIPS.md) (`KID-CON-0094`). Series opener: [Understanding Security Identities](./UNDERSTANDING_SECURITY_IDENTITIES.md) (`KID-CON-0090`).

## Uncertainty vs missing directory rows

| Directory gap mindset | Security uncertainty mindset |
|-----------------------|------------------------------|
| Stale account count is low | Decision confidence about **who acted** is low |
| IAM lifecycle project backlog | Active investigation and containment scope risk |
| IdP sync completeness KPI | Prioritization may target wrong actor |
| Problem for identity governance team | Problem for every analyst queue |
| Fixed when provisioned | Fixed when **attributed, contextualized, and scoped** |

A finding without a trusted identity anchor is not fully prioritized—it is **conditionally prioritized** until attribution improves.

## How unknown identities appear

| Pattern | Example | Decision impact |
|---------|---------|-----------------|
| **Unattributed log actor** | Username in app log with no IdP link | Severity without reach or privilege context |
| **Orphaned service account** | Automation account; owner departed | No one to validate expected behavior |
| **Stale privileged account** | Dormant admin reactivated without review | High blast radius with unknown intent |
| **Split identity** | Same person, conflicting records across clouds | Correlation and containment failure |
| **Local-only account** | Application DB user outside federation | Hidden path not in central IAM view |
| **Uncertain service context** | Generic `svc_*` with unknown workload | Cannot judge normal vs abusive API use |
| **Orphan in path** | Attack path step with unresolved principal | Path confidence drops |

## Unknown identities in the decision workflow

| Workflow stage | Effect of unknown identity |
|----------------|----------------------------|
| **Triage** | Rank may default to severity-only |
| **Investigation** | Scope hypothesis incomplete; actor pivot unclear |
| **Attack path analysis** | Broken or low-confidence identity edges |
| **Containment** | Revocation may miss federated or shadow accounts |
| **Risk communication** | Cannot name accountable party or business function |
| **Closure** | Residual uncertainty undocumented |

Treat unknown attribution as a **first-class decision state**—similar to unknown evidence confidence (`KID-CON-0029`) and [unknown assets](./UNKNOWN_ASSETS.md) (`KID-CON-0084`).

## Responding without pretending completeness

| Response | When to use |
|----------|-------------|
| **Explicit unknown flag** | Any rank or narrative lacking identity link |
| **Conservative scope** | Assume wider reach until privilege and relationships mapped |
| **Attribution task** | Parallel track—not after closure |
| **Confidence downgrade** | Path or correlation depends on missing actor |
| **Escalation trigger** | Unknown + privileged signal + sensitive asset access |

Do not silently assign a placeholder identity to clear a queue—that converts uncertainty into false certainty.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Default unknown actors to "standard user" | Hidden admin or service abuse |
| Closing tickets without actor resolution | Repeat blind spots |
| Counting directory sync as identity maturity | Confident wrong priorities |
| Ignoring unknown service accounts on paths | Overstated path confidence |
| Deferring all unknowns to IAM team | Analyst scope stays blind |
| Treating stale accounts as low risk by age alone | Dormant compromise missed |

## Practical implications

1. **Flag unknown identity linkage** in prioritization rationale.  
2. **Do not treat unattributed authentication events as fully contextualized risk**.  
3. **Pair high-severity unknowns** with attribution or conservative containment.  
4. **Measure decision uncertainty**, not only directory completeness percentage.  
5. **Continue the series** at `KID-CON-0096` when published.

## Limitations

Some environments will always have transient, federated, or locally scoped actors. The goal is **visible uncertainty** and **bounded decisions**—not impossible 100% identity resolution before any action.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0094 | [Identity Relationships](./IDENTITY_RELATIONSHIPS.md) |
| KID-CON-0090 | [Understanding Security Identities](./UNDERSTANDING_SECURITY_IDENTITIES.md) |
| KID-CON-0029 | [Evidence Confidence](./EVIDENCE_CONFIDENCE.md) |
| KID-CON-0084 | [Unknown Assets](./UNKNOWN_ASSETS.md) |
| KID-GLS-0010 | [Identity](../glossary/IDENTITY.md) |

## Authority references

- `KID-ARC-0001` — [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md)

## Why this matters for security decisions

Unknown identities are not a housekeeping metric—they directly weaken every judgment that depends on privilege, relationships, and blast radius. When analysts acknowledge actor uncertainty instead of masking it, stakeholders receive honest scope estimates and teams invest attribution effort where severity and access reach demand it. Pretending an identity is known when it is not is one of the fastest paths to incomplete containment and wrong priority.

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-009 article |
