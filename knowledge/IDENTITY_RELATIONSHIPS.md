---
title: "Identity Relationships"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0094
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0093
    - KID-CON-0040
    - KID-CON-0083
  related_to:
    - KID-GLS-0010
    - KID-GLS-0011
    - KID-GLS-0022
  authority_reference:
    - KID-ARC-0001
navigation:
  knowledge_series: SER-009
  editorial_season: SEA-007
  pillar_page: PIL-IDENTITY
  learning_path: LP-009
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 10
  required_reading:
    - KID-CON-0093
    - KID-CON-0040
    - KID-CON-0083
  recommended_next: []
website_slug: identity-relationships
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Identities gain security meaning through relationships—to assets, applications, sessions, and attack paths—forming the structure analysts use to scope investigations and containment."
knowledge_tags: [identity, relationships, attack-path, education, security-entities]
---

# Identity Relationships

## What practitioners need to know

Practitioners ask: *Why does a low-severity login sometimes outrank a critical malware alert?* *Can we investigate one identity without mapping what it touches?*

Identities rarely matter in **isolation**. **Identity relationships** describe how actors connect—to assets they administer, applications they authenticate to, sessions they hold, delegated roles they assume, and paths they enable. Those links determine **investigation scope**, **containment breadth**, and **blast radius**.

Foundation: [Identity Privilege and Blast Radius](./IDENTITY_PRIVILEGE_AND_BLAST_RADIUS.md) (`KID-CON-0093`). Path primer: [Understanding Attack Paths](./UNDERSTANDING_ATTACK_PATHS.md) (`KID-CON-0040`). Asset mirror: [Asset Relationships](./ASSET_RELATIONSHIPS.md) (`KID-CON-0083`).

## Relationship types that change decisions

| Relationship | Example | Security question |
|--------------|---------|-------------------|
| **Asset access** | DBA identity → production database cluster | What data could be exfiltrated or destroyed? |
| **Application binding** | SSO user → finance SaaS tenant | Which business process is at risk? |
| **Session and token** | Refresh token valid across devices | How many active sessions must be revoked? |
| **Role assumption** | Developer → temporary cloud admin role | Was elevation expected and time-bound? |
| **Service dependency** | Kubernetes service account → API secrets | Which workloads inherit compromise? |
| **Path enablement** | Jump-box operator identity → production tier | Does this actor bridge network segments? |

A suspicious event on a **peripheral** identity can outrank a **critical alert** on an isolated host when relationships show a path to high-value assets or control planes.

## Isolated identity thinking vs connected thinking

| Isolated lens | Connected lens |
|---------------|----------------|
| Reset the flagged password | Map all assets and apps the identity reaches |
| Close ticket when MFA re-enrolled | Validate no lateral use of sessions or keys |
| One identity = one system | One identity = many records across IdP, cloud, apps |
| Rank by local alert severity | Rank by reachable criticality through relationships |

Attack paths are the structured expression of connected identity and asset thinking. Term authority: [Attack Path](../glossary/ATTACK_PATH.md) (`KID-GLS-0011`).

## Identities, assets, and paths together

```text
Identity ──access──► Asset ──adjacency──► Asset
    │                      │
    └──authenticates──► Application
                │
                └──enables step in ──► Attack Path
```

| Layer | What relationships answer |
|-------|---------------------------|
| **Identity → asset** | Where can this actor act directly? |
| **Identity → application** | Which business functions are exposed? |
| **Asset ↔ asset** | Where can compromise spread after initial access? |
| **Path** | Which sequence of steps connects entry to impact? |

[Asset relationships](./ASSET_RELATIONSHIPS.md) (`KID-CON-0083`) describe resource-side links; this article completes the picture from the **actor side**. Both views are required for defensible scope.

## Relationships in investigation workflow

| Phase | Relationship use |
|-------|------------------|
| **Triage** | Does this identity touch production, admin, or regulated data? |
| **Scoping** | Which sessions, keys, and role bindings to include |
| **Containment** | Revoke access across all related assets and apps—not one system |
| **Validation** | Confirm path break: no remaining identity→asset edges |
| **Communication** | Explain impact as reachable business functions |

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Containment in one directory only | Federated and cloud access remains |
| Ignoring service account relationships | Hidden multi-host scope |
| Asset investigation without identity map | Missed credential pivot |
| Treating relationships as static | Priority inverts after role change |
| Path analysis without identity anchors | Abstract topology, no actor to revoke |

## Practical implications

1. **Build a relationship sketch** early for any privileged or suspicious identity.  
2. **Cross-reference asset-side and identity-side maps** before closing scope.  
3. **Include applications and sessions**, not only host logons.  
4. **Document relationship confidence** when inventory or IAM data is incomplete.  
5. **Use attack path framing** (`KID-CON-0040`) when relationships suggest multi-step impact.

## Limitations

Relationship graphs are snapshot-bound and source-dependent. Cloud federation, shadow SaaS, and local application accounts often appear only after investigation—state gaps explicitly.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0093 | [Identity Privilege and Blast Radius](./IDENTITY_PRIVILEGE_AND_BLAST_RADIUS.md) |
| KID-CON-0040 | [Understanding Attack Paths](./UNDERSTANDING_ATTACK_PATHS.md) |
| KID-CON-0083 | [Asset Relationships](./ASSET_RELATIONSHIPS.md) |
| KID-GLS-0010 | [Identity](../glossary/IDENTITY.md) |
| KID-GLS-0011 | [Attack Path](../glossary/ATTACK_PATH.md) |
| KID-GLS-0022 | [Blast Radius](../glossary/BLAST_RADIUS.md) |

## Authority references

- `KID-ARC-0001` — [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md)

## Why this matters for security decisions

Investigations fail when analysts treat identities as single-system usernames instead of **connected actors**. Relationship mapping turns "suspicious login" into an explainable scope narrative—which assets, applications, and path steps must be reviewed, contained, and validated. Decisions without identity relationships optimize for ticket closure while leaving reachable crown jewels and active sessions in play.

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-009 article |
