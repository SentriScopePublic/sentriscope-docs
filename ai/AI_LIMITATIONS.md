---
title: "AI Limitations"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "AI Governance"
technical_reviewer: pending
security_reviewer: pending
ip_reviewer: pending
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_LLM.md
  - docs/current/assessments/ASSESSMENT_PUBLIC_WEBSITE_IMPLEMENTATION_ALIGNMENT.md
related_documents:
  - docs/public/ai/LLM_GUARDRAILS.md
  - docs/public/ai/READ_ONLY_AI_ASSISTANCE.md
  - docs/public/platform/WHAT_SENTRISCOPE_IS_NOT.md
publication_phase: phase_2
website_slug: ai-limitations
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "SentriScope AI assistance has explicit limitations: it does not autonomously detect threats, replace analysts, score risk deterministically, or guarantee completeness—human validation and evidence remain required."
knowledge_tags:
  - ai
  - limitations
  - governance
  - expectations
---

# AI Limitations

## Executive Summary

SentriScope provides **AI-assisted** capabilities to help analysts explore canonical security data. AI has **explicit limitations**: it does not autonomously secure your environment, replace investigations, guarantee factual completeness, or remove accountability from human decision makers. Understanding these boundaries is essential for safe adoption.

## Purpose

Set accurate expectations for prospects, customers, and auditors evaluating SentriScope AI features—complementing [LLM Guardrails](LLM_GUARDRAILS.md) with an honest capability and limitation statement.

## Problem Statement

Vendor marketing often overstates AI in security products. Teams may assume natural language interfaces imply autonomous detection, perfect accuracy, or regulatory defensibility without human oversight. Unclear limitations create operational and compliance risk.

## Industry Context

Responsible AI adoption in security emphasizes human-in-the-loop workflows, evidence traceability, and separation between probabilistic language output and deterministic controls. Mature programs document what AI **cannot** do as clearly as what it can.

## SentriScope Perspective

SentriScope AI assistance is **decision support**, not autonomous security operations. Limitations include:

| Limitation | Explanation |
|------------|-------------|
| **No autonomous detection** | AI does not replace connectors, scanners, or analyst-led detection workflows |
| **No autonomous response** | AI does not execute remediation, blocking, or ticket closure |
| **Probabilistic language output** | Responses may omit context, misinterpret questions, or state plausible-but-wrong conclusions |
| **Bounded context window** | AI sees only what the governed session exposes—not the entire history of your estate by default |
| **Not a compliance authority** | AI output is not an audit artifact on its own |
| **Not in risk scoring path** | Prioritization remains deterministic and explainable without LLM dependency |
| **Module availability varies** | Some AI features are optional or progressively rolled out |

SentriScope **does not claim** AI eliminates alert fatigue, guarantees zero false positives, or replaces specialized security engineering roles.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Guardrailed natural language query | Implemented | Read-only assistance for authorized users |
| Analyst remains accountable | Implemented | Investigation and disposition workflows require human validation |
| Deterministic prioritization without LLM | Implemented | Risk scoring independent of AI output |
| Documented public limitations | Implemented | This knowledge article and related guardrails |

## Current Limitations

- **Accuracy is not guaranteed** — Validate AI responses against canonical records and evidence.
- **Coverage gaps** — If data was not ingested or normalized, AI cannot invent reliable ground truth.
- **Language bias** — Primary product documentation is English; multilingual behavior depends on provider capabilities.
- **Latency and availability** — Third-party model providers may affect responsiveness.
- **No substitute for legal or regulatory advice** — Compliance interpretations require qualified professionals.

## Frequently Asked Questions

### Should I trust AI conclusions during an incident?

Use AI to **accelerate exploration**, not as the sole basis for containment or disclosure decisions. Follow evidence and approved procedures.

### Does SentriScope use AI to prioritize vulnerabilities?

**Deterministic** scoring uses canonical inputs and defined rules. AI is **not** the authority for prioritization scores.

### Is SentriScope an autonomous SOC platform?

No. See [What SentriScope is not](../platform/WHAT_SENTRISCOPE_IS_NOT.md).

### Will AI features improve over time?

Capabilities evolve through governed product development. Public pages describe **current** boundaries; roadmap themes may be published separately when approved.

## Related Articles

- [LLM guardrails](LLM_GUARDRAILS.md)
- [Read-only AI assistance](READ_ONLY_AI_ASSISTANCE.md)
- [What SentriScope is not](../platform/WHAT_SENTRISCOPE_IS_NOT.md)
- [Risk scoring approach](../intelligence/RISK_SCORING_APPROACH.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_LLM.md` | AI architecture scope (sanitized) |
| `docs/current/assessments/ASSESSMENT_PUBLIC_WEBSITE_IMPLEMENTATION_ALIGNMENT.md` | Marketing vs implementation alignment |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | AI Governance | Phase 2 initial draft |
