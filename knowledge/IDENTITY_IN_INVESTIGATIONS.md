---
title: "Identity in Investigations"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0097
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0096
    - KID-CON-0019
    - KID-CON-0087
  related_to:
    - KID-CON-0020
    - KID-CON-0048
    - KID-CON-0094
  authority_reference:
    - KID-INV-0001
navigation:
  knowledge_series: SER-009
  editorial_season: SEA-007
  pillar_page: PIL-IDENTITY
  learning_path: LP-009
  difficulty: intermediate
  audience: [analyst]
  estimated_time_minutes: 10
  required_reading:
    - KID-CON-0096
    - KID-CON-0019
    - KID-CON-0087
  recommended_next:
    - KID-CON-0098
website_slug: identity-in-investigations
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "During investigation, identities anchor scope, hypothesis, and containment—using context, access paths, relationships, and privilege to understand incidents without treating directory records as proof."
knowledge_tags: [identity, investigation, incident, education, security-entities]
---

# Identity in Investigations

## What practitioners need to know

Investigations ask: *Who acted, with what reach, and what could happen next?* **Identities** are primary anchors for those questions—not because directories are complete, but because compromise and persistence flow through **actors**.

This article shows how identity understanding helps analysts **scope**, **hypothesize**, and **contain** during incidents. It builds on [Investigation Lifecycle](./INVESTIGATION_LIFECYCLE.md) (`KID-CON-0019`), [Assets in Investigations](./ASSETS_IN_INVESTIGATIONS.md) (`KID-CON-0087`), and [Identity Exposure and Access](./IDENTITY_EXPOSURE_AND_ACCESS.md) (`KID-CON-0096`).

Not incident response runbooks or IAM provisioning procedures—**decision support** for analysts reasoning about actors under uncertainty.

## Identities across the investigation lifecycle

| Phase | Identity role |
|-------|---------------|
| **Triage** | Identify primary and adjacent actors from alert context |
| **Scoping** | Expand or constrain identity set using relationships (`KID-CON-0094`) |
| **Hypothesis** | State testable claims about authentication, privilege, and session use (`KID-CON-0020`) |
| **Evidence collection** | Target sources per actor; note provenance and gaps |
| **Containment** | Revoke sessions, rotate credentials, disable paths **per identity** |
| **Handoff** | Document validated actors, unknowns, and residual access |

## What identity context changes during investigation

| Context element | Investigation use |
|-----------------|-------------------|
| **Privilege** (`KID-CON-0093`) | Escalation threshold and executive notification |
| **Access paths** (`KID-CON-0096`) | Which assets and apps require immediate validation |
| **Relationships** (`KID-CON-0094`) | Lateral scope and attack path hypotheses |
| **Lifecycle state** (`KID-CON-0092`) | Dormant, orphaned, or departing actors raise suspicion |
| **Unknown identity** (`KID-CON-0095`) | Widen scope; avoid premature closure |
| **Asset scope** (`KID-CON-0087`) | Pair actor pivot with resource impact |

## Identity and asset discipline together

Incidents touch **who** and **where**. Analysts need both lenses:

```text
Identity pivot ──access──► Asset scope ──relationship──► Expanded asset set
       │                           │
       └── session / credential ───┘
```

| Combined view | Investigator must |
|---------------|-------------------|
| Privileged identity + crown-jewel asset | Prioritize evidence; notify early |
| Suspicious login + unknown reach | Map access paths before closing |
| Compromised host + unclear actor | Resolve identity before declaring containment |
| Service account + multi-workload access | Scope all dependent automation |
| Asset-only investigation record | Add identity map before handoff |

**Never close** an investigation on directory metadata alone. Context **directs** attention; evidence **proves** outcomes.

## Identity discipline: context vs proof

| Identity context says | Investigator must |
|-----------------------|-------------------|
| Domain admin service account | Treat any anomaly as high urgency |
| Access to regulated data store | Validate data access in logs—not assume exfiltration |
| Path to production control plane | Hunt for movement evidence (`KID-CON-0048`) |
| Unknown owner or orphan account | Document uncertainty; choose proportional containment |
| Missing from central IAM | Treat as unknown identity; do not ignore signals |

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Single alert actor = full scope | Missed federated or service principals |
| Ignoring identity relationships | Incomplete blast radius |
| Directory gap = "not our problem" | Shadow accounts mishandled |
| Privilege context without evidence | Panic escalation or false calm |
| Containment in one system only | Active sessions elsewhere |
| No identity list in handoff | Continuity breaks next shift |

## Practical implications

1. **Maintain a living identity scope list** with confidence notes (confirmed / assumed / unknown).  
2. **Attach top relationships and access paths** to the investigation record early.  
3. **Pair asset scope** (`KID-CON-0087`) with actor scope before escalation.  
4. **Revoke across all reachable paths**, not only the system that generated the alert.  
5. **Update identity feedback** when investigation disproves assumed context.  

## Limitations

Identity context accelerates **who to investigate** and **how urgently**—not **what happened**. Behavioral, forensic, and asset evidence still lead conclusions. Incomplete identity knowledge requires explicit uncertainty in decisions.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0019 | [Investigation Lifecycle](./INVESTIGATION_LIFECYCLE.md) |
| KID-CON-0087 | [Assets in Investigations](./ASSETS_IN_INVESTIGATIONS.md) |
| KID-CON-0096 | [Identity Exposure and Access](./IDENTITY_EXPOSURE_AND_ACCESS.md) |
| KID-CON-0020 | [Investigation Hypothesis](./INVESTIGATION_HYPOTHESIS.md) |
| KID-CON-0048 | [Attack Paths in Investigation](./ATTACK_PATHS_IN_INVESTIGATION.md) |
| KID-INV-0001 | [Investigation Workspace](../investigations/INVESTIGATION_WORKSPACE.md) |

## Authority references

- `KID-INV-0001` — investigation capability

## Why this matters for security decisions

Incidents are understood through **who could act** and **what they could reach**. Analysts who use identities as investigative anchors—with context, access paths, and relationships—make faster scoping choices, clearer containment, and auditable handoffs instead of treating every authentication alert as an isolated event disconnected from blast radius.

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-009 article |
