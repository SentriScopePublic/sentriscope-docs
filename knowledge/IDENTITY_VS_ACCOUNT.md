---
title: "Identity vs Account"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0091
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0090
    - KID-GLS-0010
  related_to:
    - KID-CON-0092
    - KID-CON-0080
    - KID-ARC-0001
  authority_reference:
    - KID-ARC-0001
navigation:
  knowledge_series: SER-009
  editorial_season: SEA-007
  pillar_page: PIL-IDENTITY
  learning_path: LP-009
  difficulty: introductory
  audience: [analyst, soc_manager]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0090
    - KID-GLS-0010
  recommended_next:
    - KID-CON-0092
website_slug: identity-vs-account
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A security identity is the analyst's decision object for who can act; an account record is the operational artifact in a directory or cloud IAM—related but not interchangeable."
knowledge_tags: [identity, account, education, security-entities]
---

# Identity vs Account

## What practitioners need to know

Practitioners ask: *Isn't identity just the account in AD?* *Why do we need two concepts?*

Analysts need **identity** as a **security concept**—the actor findings attach to, whose privilege and reach change decisions. Directories and cloud IAM store **account records**—rows with attributes, group memberships, and lifecycle states. The distinction prevents inventory thinking from replacing investigation scope.

Foundation: [Understanding Security Identities](./UNDERSTANDING_SECURITY_IDENTITIES.md) (`KID-CON-0090`). Term: [Identity](../glossary/IDENTITY.md) (`KID-GLS-0010`).

## Comparison

| Dimension | Security identity (decision lens) | Account record (operational artifact) |
|-----------|-----------------------------------|---------------------------------------|
| **Purpose** | Explain who or what could act | Store credentials and attributes in a source |
| **Meaning** | Comes from privilege, access, and context | Comes from fields and group memberships |
| **Completeness** | May span multiple records across systems | Often treated as authoritative in one system |
| **Analyst use** | Pivot investigations, scope blast radius | Input for enrichment—not the definition of scope |
| **Unknown state** | Explicit uncertainty in decisions | Often missing row or stale object |
| **Shared actors** | One logical actor, many records possible | Multiple rows without linkage |

Same pattern as [Understanding Security Assets](./UNDERSTANDING_SECURITY_ASSETS.md) (`KID-CON-0080`): the **entity for decisions** is not the same as the **record in a source system**.

## One identity, many account records

| Scenario | Identity view | Account record view |
|----------|---------------|---------------------|
| User with on-prem AD and cloud SSO | One person acting across environments | Two objects that may not auto-link |
| Service principal in Azure and AWS | One workload identity with multi-cloud reach | Separate IAM entries per cloud |
| Break-glass admin shared by team | High-risk shared actor | Single enabled account |
| Former employee with lingering app account | One human identity with orphaned access | Disabled in HR system, active in SaaS |

Analysts **normalize** records into a security identity—or document that normalization failed. Closing an investigation on "account disabled in AD" while a cloud shadow account remains active is a **record-complete, identity-incomplete** failure.

## Account record thinking vs identity thinking

| Account record lens | Identity lens |
|---------------------|---------------|
| Ticket: sync directory | Question: who can still authenticate? |
| Count of stale accounts | Scope: which actors reach crown jewels? |
| Group membership as static truth | Role and privilege as decision context |
| One system = one answer | Cross-source actor resolution required |

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Equating IAM hygiene metrics with security outcomes | False maturity signals |
| Investigating only the account named in one log | Missed linked principals |
| Treating disabled directory account as full containment | Active sessions or cloud identities remain |
| Ignoring non-human identities | Service account abuse undetected |
| Assuming samAccountName equals actor everywhere | Wrong attribution across federated systems |

## Practical implications

1. **Resolve actors** across IdP, directory, cloud IAM, and application logs before scoping containment.  
2. **Document** when records cannot be linked to a single identity.  
3. **Ask what the identity can reach**, not only whether the account row looks clean.  
4. **Continue to** [Identity Context](./IDENTITY_CONTEXT.md) (`KID-CON-0092`) for privilege, role, access, and lifecycle dimensions.

## Limitations

Account records are necessary inputs but rarely sufficient. Federation, shadow IT, API keys, and local application accounts produce gaps that analysts must state explicitly rather than infer from directory completeness.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0090 | [Understanding Security Identities](./UNDERSTANDING_SECURITY_IDENTITIES.md) |
| KID-GLS-0010 | [Identity](../glossary/IDENTITY.md) |
| KID-CON-0080 | [Understanding Security Assets](./UNDERSTANDING_SECURITY_ASSETS.md) |
| KID-GLS-0003 | [Security Context](../glossary/SECURITY_CONTEXT.md) |

## Authority references

- `KID-ARC-0001` — [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md)

## Why this matters for security decisions

Containment, escalation, and audit narratives depend on **who could act**, not which directory row was updated. Teams that stop at account records risk leaving active sessions, federated identities, and service principals in play while reporting IAM tasks complete. Identity thinking keeps decisions aligned with actual reach and blast radius.

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-009 article |
