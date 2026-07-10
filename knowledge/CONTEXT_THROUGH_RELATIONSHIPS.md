---
title: "Context Through Relationships"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0124
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0123
    - KID-GLS-0039
    - KID-CON-0114
  related_to:
    - KID-CON-0083
    - KID-CON-0094
    - KID-CON-0104
    - KID-CON-0040
  authority_reference:
    - KID-ARC-0001
navigation:
  knowledge_series: SER-012
  editorial_season: SEA-010
  pillar_page: PIL-CORRELATION
  learning_path: LP-012
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-CON-0123
    - KID-GLS-0039
  recommended_next:
    - KID-CON-0125
website_slug: context-through-relationships
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Security relationships supply decision context—reachability, privilege, dependency, and path structure—so correlated observations change rank and scope based on how entities connect, not in isolation."
knowledge_tags: [correlation, relationships, education, decision-support]
---

# Context Through Relationships

## What practitioners need to know

Practitioners ask: *Why does a medium finding on a jump host outrank a critical CVE elsewhere?* *How do relationships change what correlation means?*

Observations gain significance through **how entities connect**. A **relationship** in security decision support is a link—asset-to-asset, identity-to-asset, application-to-service, exposure-to-path—that changes interpretation, prioritization, or investigation scope.

Term authority: [Relationship](../glossary/RELATIONSHIP.md) (`KID-GLS-0039`).

Foundation: [Canonical Understanding](./CANONICAL_UNDERSTANDING.md) (`KID-CON-0123`), [Exposure Relationships](./EXPOSURE_RELATIONSHIPS.md) (`KID-CON-0114`). Entity primers: [Asset Relationships](./ASSET_RELATIONSHIPS.md) (`KID-CON-0083`), [Identity Relationships](./IDENTITY_RELATIONSHIPS.md) (`KID-CON-0094`), [Application Relationships](./APPLICATION_RELATIONSHIPS.md) (`KID-CON-0104`), [Understanding Attack Paths](./UNDERSTANDING_ATTACK_PATHS.md) (`KID-CON-0040`).

This article teaches **relationship-aware correlation**—not graph database administration, network topology products, or discovery tooling tutorials.

## Why relationships change correlated stories

| Isolated correlation | Relationship-aware correlation |
|----------------------|------------------------------|
| Same CVE on two hosts | CVE on **path node** vs leaf node |
| Login alert + asset alert | **Identity bridge** to privileged scope |
| Three low findings | **Shared dependency**—one root cause |
| Intel match + scan finding | Match on **reachable** exposure only |
| Time-grouped "incident" | **Structural choke point** breaking many paths |

Relationships explain **rank inversions** without abandoning severity or intelligence inputs.

## Relationship types for correlation

| Relationship | Correlation question | Decision impact |
|--------------|---------------------|-----------------|
| **Asset-to-asset** | What else is reachable if this is affected? | Lateral scope |
| **Identity-to-asset** | Who can exploit or is affected? | Privilege-weighted urgency |
| **Application-to-service** | What business capability depends on this? | Stakeholder scope |
| **Exposure-to-path** | Which paths include this weakness? | Structural prioritization |
| **Entity-to-intelligence** | Does campaign knowledge apply here now? | Timely elevation or deprioritization |
| **Observation-to-observation** | Do signals share a root cause? | Consolidated remediation |

## Correlation patterns enabled by relationships

| Pattern | Relationship dependency |
|---------|-------------------------|
| **Structural** | Path membership, dependency chains |
| **Actor-resource** | Identity access to asset or application |
| **Compound exposure** | Linked weaknesses amplifying reachability |
| **Cross-source** | Same canonical entity across tools |
| **Temporal + structural** | Events on connected entities in sequence |

Temporal grouping alone is aggregation. **Structural linkage** produces correlation that changes decisions.

## Connection to blast radius

[Blast Radius](../glossary/BLAST_RADIUS.md) (`KID-GLS-0022`) describes potential impact spread. Relationships are the **edges** analysts traverse when estimating blast radius during correlation—choke points, identity bridges, and dependency chains elevate correlated stories disproportionately.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Correlating by IP or hostname string only | Misses identity and application context |
| Drawing network maps but not using them in triage | Visualization without decision impact |
| Treating relationships as static | Stale path after environment change |
| Assuming discovery tools supply decision-ready relationships | Incomplete or unvalidated linkage |

## Practical implications

1. **Ask structural questions** when correlating: path node? identity bridge? dependency root?  
2. **Cross-reference** Volume 3 entity relationship articles for domain-specific patterns.  
3. **Flag relationship confidence** when inferred—not only observation confidence.  
4. **Continue to** [Correlation During Investigation](./CORRELATION_DURING_INVESTIGATION.md) (`KID-CON-0125`).

## Current limitations

Relationship accuracy varies by source maturity, cloud abstraction, and identity hygiene. Incomplete relationship graphs produce incomplete correlated stories—with explicit gaps preferred over assumed connectivity. This article establishes correlation semantics; investigation and risk applications follow in later SER-012 articles.

## Canonical references

| KID | Resource |
|-----|----------|
| KID-GLS-0039 | [Relationship](../glossary/RELATIONSHIP.md) — term authority |
| KID-GLS-0038 | [Canonical Understanding](../glossary/CANONICAL_UNDERSTANDING.md) |
| KID-GLS-0022 | [Blast Radius](../glossary/BLAST_RADIUS.md) |
| KID-ARC-0001 | [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md) |

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0123 | [Canonical Understanding](./CANONICAL_UNDERSTANDING.md) |
| KID-CON-0114 | [Exposure Relationships](./EXPOSURE_RELATIONSHIPS.md) |
| KID-CON-0083 | [Asset Relationships](./ASSET_RELATIONSHIPS.md) |
| KID-CON-0040 | [Understanding Attack Paths](./UNDERSTANDING_ATTACK_PATHS.md) |
| KID-CON-0125 | [Correlation During Investigation](./CORRELATION_DURING_INVESTIGATION.md) |

## Why this matters for security decisions

Correlation without relationships produces **flat stories**—same severity wins, choke points stay hidden, and investigations stay narrow. Relationship-aware correlation elevates structural significance, consolidates root causes, and scopes action proportionally to how harm could spread through the environment.

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-012 article |
