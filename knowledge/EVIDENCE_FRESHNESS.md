---
title: "Evidence Freshness"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0012
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0001
    - KID-CON-0010
    - KID-CON-0011
  related_to:
    - KID-CON-0015
    - KID-CON-0013
  authority_reference:
    - KID-OIN-0001
navigation:
  knowledge_series: SER-001
  editorial_season: SEA-001
  pillar_page: PIL-EVIDENCE
  learning_path: LP-001
  search_intent_ids: [SI-004]
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 7
  required_reading:
    - KID-CON-0010
  recommended_next:
    - KID-CON-0013
    - KID-CON-0015
website_slug: evidence-freshness
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "Evidence freshness measures whether security information is current enough for the decision at hand—staleness is contextual, not merely age in days."
knowledge_tags: [evidence, freshness, education]
---

# Evidence Freshness

## What practitioners need to know

Practitioners ask: *How old is too old?* *Can I use yesterday's scan during an active incident?*

**Evidence freshness** is whether information reflects the state of the environment **at the time relevant to the decision**. Freshness is **contextual**—a one-year-old architecture diagram may suffice for classification; a one-hour-old EDR status may be stale during live containment.

## Freshness by evidence type

| Evidence type | Freshness sensitivity | Typical staleness risk |
|---------------|----------------------|------------------------|
| Live telemetry / EDR status | High | Minutes to hours |
| Vulnerability scan | Medium–high | Days (patch cycles) |
| CMDB asset record | Medium | Weeks (drift) |
| Threat intel IOC | Variable | Hours to days (campaign-dependent) |
| Policy / control documentation | Low | Months (unless change window) |

## Industry context

Exposure management and vulnerability programs often publish "days since last scan" metrics—useful but incomplete. Freshness must align with **decision type**: prioritizing quarterly remediation differs from stopping lateral movement during an incident.

Operational intelligence practices weight recency when ranking attention—but recency alone is not prioritization. See `KID-OIN-0001`.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Using stale CMDB during incident | Wrong asset owner, wrong isolation target |
| Treating all evidence as equally time-sensitive | Over-collection or under-reaction |
| Ignoring clock skew and timezone errors | False sequencing |
| Confusing "last seen" with "still true" | Ghost assets, false clearance |

## Practical implications

1. **State the decision time horizon** — incident vs strategic planning.  
2. **Record observation time and ingestion time** separately when they differ.  
3. **Re-validate critical evidence** before irreversible actions.  
4. **Document freshness assumptions** in investigation notes.  

See [Evidence Lifecycle](./EVIDENCE_LIFECYCLE.md) (`KID-CON-0015`) and [FAQ: Does evidence expire?](../faq/FAQ_DOES_EVIDENCE_EXPIRE.md) (`KID-FAQ-0006`).

## Limitations

Fresh evidence can still be wrong (sensor misconfiguration, incomplete coverage). Stale evidence can still be directionally useful with explicit caveats. Freshness is one dimension of [Evidence Quality Framework](./EVIDENCE_QUALITY_FRAMEWORK.md) (`KID-CON-0014`).

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0002 | [What Makes Security Evidence Trustworthy](./WHAT_MAKES_SECURITY_EVIDENCE_TRUSTWORTHY.md) |
| KID-CON-0011 | [Evidence Provenance](./EVIDENCE_PROVENANCE.md) |
| KID-FAQ-0006 | [Does evidence expire?](../faq/FAQ_DOES_EVIDENCE_EXPIRE.md) |

## Authority references

- `KID-OIN-0001` — operational prioritization and attention context

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-02 | Initial SER-001 article |
