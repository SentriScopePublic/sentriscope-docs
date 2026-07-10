---
title: "What SentriScope Is Not"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D1
audience: public
owner: "Product Governance"
technical_reviewer: pending
security_reviewer: pending
ip_reviewer: pending
knowledge_id: KID-PLT-0002
knowledge_domain: boundaries
knowledge_object: boundary
authority_tier: T1
is_authority: true
authority_document: KID-PLT-0002
knowledge_lifecycle: validated
document_version: "1.0"
knowledge_version: "1.0"
publication_version: "0"
documentation_maturity: D1
canonical_sources:
  - docs/current/architecture/ARCHITECTURE_LLM.md
  - docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md
  - docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md
related_documents:
  - docs/public/platform/WHAT_IS_SENTRISCOPE.md
  - docs/public/platform/PLATFORM_OVERVIEW.md
knowledge_relationships:
  depends_on:
    - KID-PLT-0001
  explains: []
  supersedes: []
  related_to:
    - KID-PLT-0003
  implements: []
  introduces: []
  deprecates: []
  expands: []
navigation:
  personas: [evaluator, investor, public]
  learning_paths: [LP-001]
  prerequisites:
    - KID-PLT-0001
  recommended_reading_order: 2
documentation_health:
  assessed: 2026-07-02
  completeness: 96
  evidence_coverage: 100
  review_completion: 0
  publication_readiness: 76
  review_score: conditional
knowledge_debt_reference: docs/public/metadata/KNOWLEDGE_DEBT_BACKLOG.md
publication_phase: phase-1
website_slug: what-sentriscope-is-not
last_updated: 2026-07-02
next_review: 2026-10-02
llm_summary: "SentriScope is not a SIEM, SOAR, or autonomous SOC replacement; not an unrestricted AI agent; not a standalone vulnerability scanner; and not a source of truth without integrated evidence and analyst validation."
knowledge_tags:
  - platform
  - boundaries
  - faq
---

# What SentriScope Is Not

## Executive Summary

SentriScope is a security intelligence platform that **complements** existing security investments. It is **not** a drop-in replacement for a SIEM, SOAR, or autonomous security operations center. It is **not** an unrestricted AI agent, a standalone vulnerability scanner, or a system that produces trustworthy conclusions without integrated evidence and **analyst validation**.

## Purpose

This document sets clear boundaries for due diligence, LLM grounding, and technical evaluation. Accurate boundaries reduce misinformation about SentriScope capabilities.

## Problem Statement

Security products are often categorized loosely—"AI-powered," "autonomous," or "SIEM replacement"—which creates incorrect expectations. Readers evaluating SentriScope need explicit statements about what the platform **does not** claim to be.

## Industry Context

Organizations typically operate a stack of specialized tools: log aggregation and detection (often associated with SIEM), orchestration and response automation (SOAR), vulnerability management, endpoint detection, identity security, and threat intelligence platforms. No single product category fully subsumes all of these functions.

## SentriScope Perspective

The following boundaries apply to SentriScope as implemented and publicly described today.

### Not a SIEM replacement

SentriScope **does not** replace a Security Information and Event Management platform. It may ingest and normalize data from security sources and support correlation and investigation, but it is **not** positioned as a full log aggregation and real-time detection engine substitute.

### Not a SOAR replacement

SentriScope **does not** replace Security Orchestration, Automation, and Response platforms. Response automation and broad playbook orchestration across an entire SOC toolchain are **outside** the core boundary of what SentriScope publicly describes as implemented.

### Not an autonomous SOC

SentriScope **does not** operate as an autonomous security operations center. **Analyst validation** is required for investigation conclusions and governed decisions. AI features are assistive and read-only with respect to critical evidence paths.

### Not an unrestricted AI agent

SentriScope **does not** provide an unrestricted AI agent that writes directly into evidence, executes arbitrary actions, or bypasses schema validation. AI assistance is **guardrailed** and **not** in the deterministic risk-scoring path (implemented).

### Not a vulnerability scanner by itself

SentriScope **does not** perform standalone network or agent-based scanning as its primary function. It **ingests** vulnerability and exposure data from governed connectors and normalizes findings for prioritization and investigation (implemented).

### Not a source of truth without integrated evidence

SentriScope **does not** assert conclusions without traceable evidence from integrated sources. Canonical entities carry provenance concepts; analyst workflows are **evidence-driven** (implemented).

### Not open source

SentriScope is **not** open source software.

## Current Capabilities

This document describes **boundaries**, not features. For what SentriScope **does** support, see [WHAT_IS_SENTRISCOPE.md](WHAT_IS_SENTRISCOPE.md).

Relevant implemented boundaries:

- Deterministic risk scoring separate from LLM assistance (implemented)
- Read-only, validated natural language query over canonical data (implemented)
- Governed connector ingestion rather than native scanning (implemented)

## Current Limitations

- Boundary statements here reflect **public documentation at v1.0**. Specific deployment configurations may enable or disable optional integrations.
- SentriScope **may** integrate with SIEM, SOAR, ITSM, or scanner ecosystems through connectors; integration depth varies by connector and tenant configuration.
- **ITSM ticket creation** capability exists but is **partially implemented** from a default-enablement perspective (may be off by default).
- Public documentation **does not** enumerate every integration scenario; refer to connector and data source pages when published.

## Frequently Asked Questions

### Can SentriScope replace our SIEM?

SentriScope is designed to complement existing tooling by normalizing and correlating security data for analyst-led workflows. Organizations should not plan a SIEM replacement strategy based on SentriScope alone.

### Does SentriScope automatically respond to incidents?

SentriScope supports investigation and decision support. Autonomous response orchestration is **not** described as a core implemented capability in public documentation.

### Is SentriScope "AI-powered detection"?

SentriScope uses AI for **assistive**, **read-only** analysis workflows over canonical data. It **does not** describe autonomous detection of all attacks.

### Is SentriScope similar to asset management or ASM-only tools?

SentriScope includes attack surface and exposure concepts within a broader canonical model. It is **not** defined solely as an attack surface management point product.

## Related Articles

- [What is SentriScope?](WHAT_IS_SENTRISCOPE.md)
- [Platform overview](PLATFORM_OVERVIEW.md)
- Planned: `faq-siem-replacement`, `faq-ai-usage`, `ai-limitations` (see [INDEX.md](../INDEX.md))

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_LLM.md` | LLM not in scoring path; read-only assistance |
| `docs/current/foundations/DESIGN_PUBLIC_SITE_CONTENT_MODEL.md` | Messaging pillars and safe boundaries |
| `docs/current/assessments/ASSESSMENT_SENTRISCOPE_PUBLIC_WEBSITE_COVERAGE.md` | Partial capabilities (SBOM UI, ITSM defaults) |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-02 | Product Governance | Initial public draft |
