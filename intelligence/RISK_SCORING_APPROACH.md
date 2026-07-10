---
title: "Risk Scoring Approach"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Risk Intelligence PM"
technical_reviewer: pending
security_reviewer: n/a
ip_reviewer: pending
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_DATA.md
  - docs/current/assessments/ASSESSMENT_PUBLIC_WEBSITE_IMPLEMENTATION_ALIGNMENT.md
related_documents:
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
  - docs/public/intelligence/INTELLIGENCE_CORRELATION.md
  - docs/public/glossary/RISK.md
  - docs/public/ai/LLM_GUARDRAILS.md
publication_phase: phase_2
website_slug: risk-scoring-approach
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "SentriScope prioritizes security findings using deterministic, explainable risk scoring over canonical data—combining severity, exploitability, threat context, and asset context without LLM involvement in the scoring path."
knowledge_tags:
  - risk
  - prioritization
  - scoring
  - intelligence
---

# Risk Scoring Approach

## Executive Summary

SentriScope **risk scoring** prioritizes exposures and related findings using **deterministic, explainable** rules over canonical data—not opaque machine learning or LLM output. Inputs may include industry-standard severity and exploitability signals, known-exploited context, asset criticality, and threat intelligence correlation where available. Risk scoring is **implemented**; exact weighting and tenant overrides are product configuration details not disclosed in public documentation.

## Purpose

Help risk and vulnerability management teams understand how SentriScope approaches prioritization honestly—what is automated, what requires context, and what AI does **not** control.

## Problem Statement

Scanner severity alone produces unusable backlogs. Teams need prioritization that reflects **likelihood**, **impact**, and **threat relevance** in **their** environment—while remaining explainable to auditors and remediation owners.

## Industry Context

Common inputs include CVSS, EPSS, CISA Known Exploited Vulnerabilities catalogs, and structured decision frameworks such as SSVC. Mature programs combine these signals with asset criticality and exposure context rather than treating generic scores as final truth.

## SentriScope Perspective

SentriScope risk scoring principles:

| Principle | Description |
|-----------|-------------|
| **Deterministic** | Same inputs yield the same prioritized outcome within a defined ruleset |
| **Explainable** | Analysts can understand which factors influenced ordering |
| **Context-aware** | Asset, identity, and exposure linkage matter—not isolated CVE rows |
| **Threat-enriched** | Intelligence correlation may elevate relevance when validated |
| **LLM-independent** | AI assistance does not authoritatively set risk scores |
| **Analyst sovereignty** | Humans validate decisions; scoring supports—not replaces—judgment |

Scoring operates on **canonical entities** ingested through governed connectors. Stale or missing upstream data limits scoring quality—garbage in, governed but imperfect out.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Deterministic prioritization over canonical exposures | Implemented | Explainable ordering for triage workflows |
| Industry signal incorporation | Implemented | Common severity and exploitability inputs supported conceptually |
| Threat intelligence enrichment influence | Implemented | Correlated threat context may affect prioritization |
| Asset and exposure context | Implemented | Same finding may rank differently on different assets |
| Separation from LLM scoring | Implemented | AI not in critical scoring path |
| Risk decision workflows | Partial | Decision recording depth varies by module maturity |

## Current Limitations

- This document does **not** publish formulas, weights, or tenant override matrices.
- Scoring does **not** guarantee exploitability in your specific environment.
- **Custom risk frameworks** beyond supported inputs may require manual analyst judgment.
- **Organizational risk appetite** is not automatically encoded without configuration and governance.
- SentriScope does **not** claim to eliminate all false positives or reduce triage time by a fixed marketing percentage.

## Frequently Asked Questions

### Does SentriScope use AI to rank vulnerabilities?

**No.** Prioritization is **deterministic**. AI may help analysts **explore** results but does not authoritatively score them.

### Why does the same CVE rank differently on two assets?

**Context**—criticality, exposure conditions, controls, and threat relevance—changes priority. See [Glossary: Risk](../glossary/RISK.md).

### Is this the same as FAIR quantitative risk?

SentriScope provides **operational prioritization** for security teams. Full quantitative risk management programs may use additional financial models outside this document's scope.

### Can I override a score?

Human disposition and investigation workflows allow analyst judgment. Automatic score overrides without governance are **not** the default model.

## Related Articles

- [Intelligence correlation](INTELLIGENCE_CORRELATION.md)
- [Attack path analysis](ATTACK_PATH_ANALYSIS.md)
- [Canonical data model](../architecture/CANONICAL_DATA_MODEL.md)
- [LLM guardrails](../ai/LLM_GUARDRAILS.md)
- [Glossary: Risk](../glossary/RISK.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Risk and canonical data relationships (sanitized) |
| `docs/current/assessments/ASSESSMENT_PUBLIC_WEBSITE_IMPLEMENTATION_ALIGNMENT.md` | Implementation alignment for prioritization claims |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | Risk Intelligence PM | Phase 2 initial draft |
