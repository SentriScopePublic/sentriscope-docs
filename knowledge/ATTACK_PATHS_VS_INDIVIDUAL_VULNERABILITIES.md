---
title: "Attack Paths vs Individual Vulnerabilities"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0041
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0040
    - KID-CON-0034
    - KID-GLS-0008
  related_to:
    - KID-CON-0037
    - KID-CON-0042
  authority_reference:
    - KID-AGR-0001
navigation:
  knowledge_series: SER-004
  pillar_page: PIL-ATTACK-PATH
  learning_path: LP-004
  search_intent_ids: [SI-031]
  difficulty: introductory
  audience: [analyst]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0040
  recommended_next:
    - KID-CON-0042
website_slug: attack-paths-vs-individual-vulnerabilities
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Individual vulnerabilities describe isolated weaknesses; attack paths show how weaknesses chain together in context—both matter, but they answer different prioritization questions."
knowledge_tags: [attack-path, vulnerability, education]
---

# Attack Paths vs Individual Vulnerabilities

## What practitioners need to know

Practitioners ask: *Should I still care about CVEs if I have attack paths?* *Are paths just fancy vulnerability lists?*

**Vulnerabilities** describe **isolated weaknesses**. **Attack paths** describe **how weaknesses could chain** in your environment. Neither replaces the other.

## Comparison

| Dimension | Individual vulnerability | Attack path |
|-----------|-------------------------|-------------|
| **Unit** | CVE / misconfiguration | Multi-step sequence |
| **Question** | How severe is this flaw? | What could be reached if exploited? |
| **Context** | Often generic | Environment-specific |
| **Output** | Finding | Decision-support model |
| **Typical input** | Scanner, advisory | Graph + findings + context |

See [Why Severity Alone Is Insufficient](./WHY_SEVERITY_ALONE_IS_INSUFFICIENT.md) (`KID-CON-0034`) for score limits.

## When each matters

- **Vulnerability-centric**: patch hygiene, compliance baselines, vendor advisories  
- **Path-centric**: crown jewel reachability, lateral movement risk, choke-point remediation  

Best programs **link** both: CVE on a node within a prioritized path.

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Ignoring paths for "Critical CVE" culture | Fix leaf nodes; miss chains |
| Ignoring CVE detail on path nodes | Incomplete remediation |
| Duplicate work per CVE × path | Inefficient patching |
| Assuming path implies exploitability | False certainty |

## Practical implications

1. **Map top vulnerabilities to path nodes**.  
2. **Prioritize fixes that break multiple paths** (choke points).  
3. **Do not drop CVE tracking** when adopting path analysis.  
4. **Explain to stakeholders** using both views (`KID-CON-0046`).  

## Limitations

Paths depend on vulnerability data being linked to correct entities. Orphan CVEs without asset mapping weaken path value.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0037 | [Why Identical Findings Create Different Risk](./WHY_IDENTICAL_FINDINGS_CREATE_DIFFERENT_RISK.md) |
| KID-FAQ-0021 | [Are attack paths the same as vulnerabilities?](../faq/FAQ_ATTACK_PATHS_VS_VULNERABILITIES.md) |

## Authority references

- `KID-AGR-0001` — attack graph capability context

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-004 article |
