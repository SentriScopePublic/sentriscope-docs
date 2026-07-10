---
title: "LLM Guardrails"
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
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
related_documents:
  - docs/public/ai/AI_LIMITATIONS.md
  - docs/public/ai/READ_ONLY_AI_ASSISTANCE.md
  - docs/public/security/PLATFORM_SECURITY_BOUNDARIES.md
  - docs/public/platform/WHAT_IS_SENTRISCOPE.md
publication_phase: phase_2
website_slug: llm-guardrails
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "SentriScope applies guardrails to LLM-assisted features: tenant-scoped context, schema-grounded responses, read-only assistance, and separation from deterministic risk scoring—so AI supports analysts without autonomous security actions."
knowledge_tags:
  - ai
  - llm
  - guardrails
  - governance
---

# LLM Guardrails

## Executive Summary

SentriScope uses large language models (LLMs) as **assistance** for authorized tenant users—not as autonomous security operators. **Guardrails** constrain how AI features access context, respond to queries, and interact with security data. AI is **read-only** with respect to mutating canonical records, **not** in the deterministic risk-scoring path, and subject to tenant configuration. Guardrails are **implemented**; exact provider and model choices may vary by deployment.

## Purpose

Explain how SentriScope limits AI-assisted features so security teams can evaluate trust boundaries, compliance fit, and analyst workflow impact—without exposing prompts, pipelines, or model internals.

## Problem Statement

Ungoverned AI in security tools can hallucinate findings, leak context across scopes, bypass approval workflows, or create false confidence in prioritization. Teams need transparent guardrails that align AI behavior with evidence-first investigation culture.

## Industry Context

Regulated enterprises increasingly require AI systems to be explainable, scoped, auditable, and subordinate to human decision authority. Security buyers distinguish between **decision support** and **autonomous action**.

## SentriScope Perspective

SentriScope guardrails follow these principles (implemented unless noted):

| Guardrail | Intent |
|-----------|--------|
| **Tenant scope** | AI context is limited to the active tenant session |
| **Schema grounding** | Responses are oriented around canonical security concepts, not arbitrary free-form database access |
| **Read-only assistance** | AI does not autonomously create, update, or delete security records |
| **Separation from risk scoring** | Deterministic prioritization does not depend on LLM output |
| **Human validation** | Investigations and governance decisions require analyst judgment |
| **Configurable enablement** | Tenants may enable or constrain AI features per policy (partial—depends on edition and flags) |
| **No public prompt disclosure** | Operational prompts and tuning are internal |

AI may help analysts **explore**, **summarize**, and **query** within guardrails—it does **not** replace connectors, scanners, or approval workflows.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Read-only natural language query over canonical data | Implemented | Analyst-facing assistance within tenant scope |
| LLM outside critical risk-scoring path | Implemented | Prioritization remains deterministic |
| Tenant-scoped AI sessions | Implemented | No cross-tenant AI context |
| Platform reliability monitoring for LLM features | Partial | Operator-facing reliability capabilities exist; customer-visible depth varies |
| Public documentation quality gates for AI content | Implemented | Published knowledge blocks unsafe internal references |

## Current Limitations

- This document does **not** describe model names, prompt templates, token limits, or provider SLAs.
- **AI output may be incorrect**; analysts must validate conclusions against evidence.
- Not every module exposes AI assistance; availability may be **feature-flagged** per tenant.
- SentriScope does **not** claim AI replaces tier-1 SOC judgment or regulatory accountability.
- **Autonomous remediation** or unsupervised blocking based on LLM output is **not** offered.

## Frequently Asked Questions

### Can the AI change vulnerability status or close incidents?

No. AI assistance is **read-only** with respect to mutating canonical security records.

### Is AI used to calculate risk scores?

**No.** Risk scoring is **deterministic**. See [Risk scoring approach](../intelligence/RISK_SCORING_APPROACH.md).

### Does AI training use my tenant data for global model training?

Public documentation describes **tenant-scoped operational use**. Contractual data processing terms govern provider behavior; this page does not replace your agreement.

### What happens if the LLM provider is unavailable?

AI-assisted features may degrade or become unavailable depending on configuration. Core ingestion, correlation, and investigation workflows do not require LLM availability.

## Related Articles

- [AI limitations](AI_LIMITATIONS.md)
- [Read-only AI assistance](READ_ONLY_AI_ASSISTANCE.md)
- [Platform security boundaries](../security/PLATFORM_SECURITY_BOUNDARIES.md)
- [What is SentriScope?](../platform/WHAT_IS_SENTRISCOPE.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_LLM.md` | LLM architecture boundaries (sanitized) |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Public AI messaging constraints |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | AI Governance | Phase 2 initial draft |
