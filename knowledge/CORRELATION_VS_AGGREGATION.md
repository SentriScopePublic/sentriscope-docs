---
title: "Correlation vs Aggregation"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0122
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-CON-0120
    - KID-CON-0121
    - KID-GLS-0013
  related_to:
    - KID-CON-0004
    - KID-CON-0016
    - KID-GLS-0012
  authority_reference:
    - KID-GLS-0013
navigation:
  knowledge_series: SER-012
  editorial_season: SEA-010
  pillar_page: PIL-CORRELATION
  learning_path: LP-012
  difficulty: intermediate
  audience: [analyst, soc_manager]
  estimated_time_minutes: 8
  required_reading:
    - KID-CON-0121
  recommended_next:
    - KID-CON-0123
website_slug: correlation-vs-aggregation
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Aggregation counts or groups observations; correlation links them into stories that change decisions—conflating the two produces dashboards that look complete but support poor judgment."
knowledge_tags: [correlation, aggregation, education, decision-support]
---

# Correlation vs Aggregation

## What practitioners need to know

Practitioners ask: *Our SIEM already correlates—why do analysts still miss the story?* *Isn't grouping alerts the same thing?*

**Aggregation** combines observations by rule—time window, severity sum, host count, deduplication key. **Correlation** links observations because they **inform the same security understanding**—often across entity types and sources.

Conflating the two produces dashboards that **look unified** but support **fragment-based decisions**. This article teaches the distinction as decision support—not SIEM rule syntax or query language.

Foundation: [Understanding Correlation](./UNDERSTANDING_CORRELATION.md) (`KID-CON-0120`), [Why Correlation Matters for Decisions](./WHY_CORRELATION_MATTERS_FOR_DECISIONS.md) (`KID-CON-0121`).

## Side-by-side comparison

| Dimension | Aggregation | Correlation |
|-----------|-------------|-------------|
| **Primary question** | How many? How often? | Do these belong to the same story? |
| **Output** | Count, group, rollup | Linked understanding for action |
| **Entity awareness** | Optional; often flat | Requires shared entity semantics |
| **Decision impact** | May reduce noise only | May change rank, scope, narrative |
| **Typical failure** | False completeness | Missed linkage when entities differ |
| **Analyst role** | Review summary | Validate story and rationale |

## Examples that look similar but decide differently

| Scenario | Aggregation view | Correlation view |
|----------|------------------|------------------|
| 50 failed logins + 1 privilege change | "51 auth events on host" | Identity path to sensitive asset—escalate |
| Same CVE on 200 hosts | "200 critical findings" | Three choke-point hosts on customer path—prioritize those |
| Threat feed + internal scan | "Intel match count: 12" | Campaign touches reachable exposure on payment tier |
| EDR + vulnerability + identity alerts | Single "incident" ticket by time | Shared root: misconfigured service account |

Aggregation **summarizes**. Correlation **reframes the decision**.

## Why tools confuse the terms

Vendors label time-based grouping, rule chaining, and deduplication as "correlation." Those features reduce analyst load—valuable—but do not automatically produce **entity-aware stories** that change judgment.

[Why Security Tools Generate Too Many Findings](./WHY_SECURITY_TOOLS_GENERATE_TOO_MANY_FINDINGS.md) (`KID-CON-0004`) explains volume pressure. Aggregation addresses **volume**; correlation addresses **meaning under volume**.

## When aggregation is enough

| Situation | Aggregation sufficient? |
|-----------|-------------------------|
| Capacity planning (events per second) | Yes |
| Deduplication of identical alerts | Yes |
| Executive trend reporting (month-over-month counts) | Often yes |
| Prioritization among entity-linked findings | No—need correlation |
| Investigation scope across sources | No—need correlation |
| Exposure reduction order with path context | No—need correlation |

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Renaming alert groups "correlated incidents" | False confidence in story completeness |
| Ranking by aggregated severity sum | Wrong host wins |
| Skipping entity linkage because events grouped | Miss cross-domain stories |
| Measuring maturity by deduplication rate | Optimize noise, not decisions |

## Practical implications

1. **Label outputs honestly**—aggregation vs correlated story—in runbooks and dashboards.  
2. **Ask whether linkage changes action** before calling something correlated.  
3. **Continue to** [Canonical Understanding](./CANONICAL_UNDERSTANDING.md) (`KID-CON-0123`) for how shared entity semantics enable true correlation.

## Current limitations

Many platforms blend aggregation and correlation features under one label. Teams must apply the **decision test** from `KID-CON-0121` regardless of product terminology. Entity normalization gaps limit correlation even when aggregation works well.

## Canonical references

| KID | Resource |
|-----|----------|
| KID-GLS-0013 | [Correlation](../glossary/CORRELATION.md) — term authority |
| KID-GLS-0012 | [Canonical Data](../glossary/CANONICAL_DATA.md) — entity foundation for linkage |

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-CON-0120 | [Understanding Correlation](./UNDERSTANDING_CORRELATION.md) |
| KID-CON-0121 | [Why Correlation Matters for Decisions](./WHY_CORRELATION_MATTERS_FOR_DECISIONS.md) |
| KID-CON-0016 | [Evidence Correlation in Practice](./EVIDENCE_CORRELATION_IN_PRACTICE.md) |
| KID-CON-0004 | [Why Security Tools Generate Too Many Findings](./WHY_SECURITY_TOOLS_GENERATE_TOO_MANY_FINDINGS.md) |
| KID-CON-0123 | [Canonical Understanding](./CANONICAL_UNDERSTANDING.md) |

## Why this matters for security decisions

Teams that treat aggregation as correlation **optimize dashboards while degrading judgment**—high-severity fragments still win, choke points stay buried, and executives receive counts instead of stories. Naming the distinction restores accountability: summaries manage volume; correlated understanding drives defensible action.

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-012 article |
