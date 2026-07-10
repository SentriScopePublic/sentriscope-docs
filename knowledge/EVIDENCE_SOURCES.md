---
title: "Evidence Sources"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0028
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
    - KID-INT-0001
  related_to:
    - KID-CON-0011
    - KID-CON-0016
  authority_reference:
    - KID-INT-0001
    - KID-ARC-0001
navigation:
  knowledge_series: SER-001
  editorial_season: SEA-001
  pillar_page: PIL-EVIDENCE
  learning_path: LP-001
  search_intent_ids: [SI-001]
  difficulty: introductory
  audience: [analyst, engineer]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0010
  recommended_next:
    - KID-CON-0011
    - KID-CON-0016
website_slug: evidence-sources
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "Evidence sources are the systems and feeds that produce security observations—each with distinct credibility, coverage, and provenance characteristics that affect investigation quality."
knowledge_tags: [evidence, sources, education]
---

# Evidence Sources

## What practitioners need to know

Evidence originates from **sources**—EDR, SIEM, vulnerability scanners, identity providers, threat feeds, CMDB, cloud APIs, and manual analyst input.

Understanding source characteristics prevents **category errors** (treating inventory as live telemetry).

## Source categories

| Category | Examples | Typical strengths | Typical weaknesses |
|----------|----------|-------------------|-------------------|
| **Endpoint telemetry** | EDR, AV | High-fidelity local events | Coverage gaps |
| **Network telemetry** | Firewall, NDR | Lateral movement visibility | Encryption blind spots |
| **Identity** | IdP, AD logs | Authentication truth | Incomplete app coverage |
| **Vulnerability** | Scanners | Exposure snapshots | Point-in-time; auth limits |
| **Threat intelligence** | Feeds, ISACs | External context | Confidence varies |
| **Inventory** | CMDB, cloud tags | Business context | Drift, staleness |
| **Application** | App logs, WAF | Transaction detail | Fragmentation |

## Source credibility weighting

Not all sources are authoritative for all claims:

- CMDB for **ownership** — not for **live compromise state**  
- Scanner for **exposure** — not for **active exploitation** without corroboration  
- TI feed for **campaign context** — not for **local presence** without local evidence  

Governed connector concepts appear in `KID-INT-0001`—not redefined here.

## Industry context

Tool sprawl increased sources faster than **integration discipline**. Teams correlate across twelve systems without documenting which is authoritative for which claim type.

Canonical modeling (`KID-ARC-0001`) helps normalize entities across sources—prerequisite for reliable correlation.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Single-source investigations | Blind spots |
| Ignoring source coverage maps | False negative confidence |
| Undocumented manual sources | Broken provenance |
| Treating export snapshots as live | Stale decisions |

## Practical implications

1. **Maintain a source catalog** — coverage, owner, latency, retention.  
2. **Tag evidence with source type** at collection.  
3. **Define authoritative source per claim type** in playbooks.  
4. **Review integration health** as evidence quality prerequisite.  

## Limitations

More sources increase noise without correlation discipline. Source inventory is organizational metadata—not a substitute for validation.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-INT-0001 | [Supported Data Sources](../integrations/SUPPORTED_DATA_SOURCES.md) |
| KID-CON-0011 | [Evidence Provenance](./EVIDENCE_PROVENANCE.md) |
| KID-GLS-0012 | [Canonical Data](../glossary/CANONICAL_DATA.md) |

## Authority references

- `KID-INT-0001` — connector and data source reference
- `KID-ARC-0001` — canonical entity model

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial SER-001 article |
