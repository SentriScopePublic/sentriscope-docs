---
title: "Asset Relationships"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0083
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0082
    - KID-CON-0040
  related_to:
    - KID-CON-0084
    - KID-GLS-0011
    - KID-GLS-0010
  authority_reference:
    - KID-ARC-0001
    - KID-AGR-0001
navigation:
  knowledge_series: SER-008
  editorial_season: SEA-006
  pillar_page: PIL-ASSETS
  learning_path: LP-008
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 10
  required_reading:
    - KID-CON-0082
    - KID-CON-0040
  recommended_next:
    - KID-CON-0084
website_slug: asset-relationships
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Assets gain security meaning through relationships—to other assets, identities, applications, and exposures—forming the structure analysts use to reason about attack paths and blast radius."
knowledge_tags: [assets, relationships, attack-path, education]
---

# Asset Relationships

## What practitioners need to know

Practitioners ask: *Why does a low-severity host sometimes outrank a critical CVE elsewhere?* *Can we prioritize one asset at a time?*

Assets rarely matter in **isolation**. **Asset relationships** describe how resources connect—network reachability, shared credentials, application dependencies, data flows, and administrative paths. Those links determine **blast radius** and **attack path** potential.

Foundation: [Asset Criticality](./ASSET_CRITICALITY.md) (`KID-CON-0082`). Path primer: [Understanding Attack Paths](./UNDERSTANDING_ATTACK_PATHS.md) (`KID-CON-0040`).

## Relationship types that change decisions

| Relationship | Example | Security question |
|--------------|---------|-------------------|
| **Network adjacency** | App server → database subnet | Can compromise hop laterally? |
| **Identity dependency** | Service account on multiple hosts | One credential, many targets |
| **Application dependency** | API gateway → microservices | Which failure cascades? |
| **Data flow** | ETL job → analytics warehouse | Where does sensitive data land? |
| **Administrative path** | Jump host → production tier | Is break-glass reachable? |
| **Shared control plane** | Kubernetes node → cluster workloads | Node compromise scope |

A finding on a **peripheral** asset can outrank a **critical CVE** on an isolated lab machine when relationships show a path to high-value targets.

## Isolated asset thinking vs connected thinking

| Isolated lens | Connected lens |
|---------------|----------------|
| Fix the noisiest host | Fix the bridge node in paths |
| Rank by local severity | Rank by reachable criticality |
| Close ticket when patch applied | Validate path break |
| One asset = one story | One asset = one step in a chain |

Attack paths are the structured expression of connected asset thinking. Term authority: [Attack Path](../glossary/ATTACK_PATH.md) (`KID-GLS-0011`).

## Relationships and attack paths

```text
Entry asset → pivot identity → adjacent asset → crown jewel
     ↑              ↑                ↑
  exposure      privilege         criticality
```

| Path element | Relationship role |
|--------------|-------------------|
| **Step** | Asset or identity node |
| **Edge** | Allowed reach, role, or dependency |
| **Destination** | Critical asset or data store |
| **Confidence** | Data quality and model scope |

Paths do not prove active attack—they show **plausible reach** that changes prioritization. See [Attack Paths as Decision Support](./ATTACK_PATHS_AS_DECISION_SUPPORT.md) (`KID-CON-0049`).

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Remediating leaf nodes only | Core bridge remains |
| Ignoring identity edges | Missed lateral movement |
| Static relationship diagrams | Wrong after cloud migration |
| Treating relationships as IT diagrams only | Security reachability missed |
| Path visualization without decision question | Activity without reprioritization |

## Practical implications

1. **Ask what this asset connects to** before accepting isolation assumptions.  
2. **Prioritize bridge and identity-hub assets** when path evidence supports reachability.  
3. **Validate relationship assumptions** with fresh exposure and identity data.  
4. **Document why a relationship changed rank** for audit and handoff.  
5. **Continue to** [Unknown Assets](./UNKNOWN_ASSETS.md) (`KID-CON-0084`) for gaps in the graph.

## Limitations

Relationship models reflect integrated inventory and graph scope. Missing nodes produce incomplete paths—state confidence explicitly rather than implying full visibility.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0082 | [Asset Criticality](./ASSET_CRITICALITY.md) |
| KID-CON-0040 | [Understanding Attack Paths](./UNDERSTANDING_ATTACK_PATHS.md) |
| KID-GLS-0011 | [Attack Path](../glossary/ATTACK_PATH.md) |
| KID-GLS-0010 | [Identity](../glossary/IDENTITY.md) |
| KID-CON-0043 | [Why Attack Paths Change Priorities](./WHY_ATTACK_PATHS_CHANGE_PRIORITIES.md) |
| KID-GLS-0022 | [Blast Radius](../glossary/BLAST_RADIUS.md) |

## Authority references

- `KID-ARC-0001` — [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md)
- `KID-AGR-0001` — [Attack Graph Overview](../capabilities/ATTACK_GRAPH_OVERVIEW.md)

## Why this matters for security decisions

Single-asset triage hides the structure adversaries exploit: relationships turn a minor foothold into access to tier-zero data. Analysts who map how assets connect can reprioritize remediation, scope investigations, and explain blast radius to stakeholders with precision. Ignoring relationships produces locally correct fixes that leave the organization globally exposed.

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-008 article |
