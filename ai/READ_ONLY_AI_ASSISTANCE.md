---
title: "Read-Only AI Assistance"
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
  - docs/current/architecture/ARCHITECTURE_DATA.md
related_documents:
  - docs/public/ai/LLM_GUARDRAILS.md
  - docs/public/ai/AI_LIMITATIONS.md
  - docs/public/architecture/CANONICAL_DATA_MODEL.md
  - docs/public/investigations/INVESTIGATION_WORKSPACE.md
publication_phase: phase_2
website_slug: read-only-ai-assistance
last_updated: 2026-07-07
next_review: 2026-10-07
llm_summary: "SentriScope AI assistance is read-only: it helps authorized users query and interpret canonical security data without autonomously changing records, bypassing RBAC, or substituting investigation workflows."
knowledge_tags:
  - ai
  - read-only
  - analyst-assistance
  - investigation
---

# Read-Only AI Assistance

## Executive Summary

SentriScope **read-only AI assistance** helps authorized users ask questions about tenant-scoped canonical security data and receive narrative or structured guidance **without** the AI autonomously creating, updating, or deleting security records. Analysts remain responsible for investigations, dispositions, and configuration changes. This pattern is **implemented** for supported AI modules.

## Purpose

Describe how read-only AI assistance fits into analyst workflows and how it differs from autonomous agents or mutating integrations—supporting evaluation alongside [LLM Guardrails](LLM_GUARDRAILS.md).

## Problem Statement

Security analysts need faster ways to navigate large canonical datasets, but mutating AI agents introduce unacceptable risk: silent record changes, unapproved prioritization shifts, and weak auditability. Teams want **assistance** that respects existing RBAC, evidence standards, and investigation culture.

## Industry Context

"Read-only" AI in operational tools typically means query and summarization over governed APIs—not direct write access to production tables or bypass of approval workflows. This model aligns with human-in-the-loop security operations.

## SentriScope Perspective

Read-only AI assistance in SentriScope means:

- **Query and explain** — Natural language interfaces over canonical concepts such as assets, exposures, and intelligence context.
- **No autonomous writes** — AI does not persist findings, change statuses, or modify connector configuration.
- **Same authorization boundary** — Users must already have permission to access underlying modules; AI does not elevate privilege.
- **Evidence-first culture** — AI supports [investigation workflows](../investigations/INVESTIGATION_WORKSPACE.md); it does not replace them.
- **Complement to deterministic analytics** — Prioritization and correlation engines operate independently.

Read-only assistance is **not** a chatbot with unrestricted tool use across your environment.

## Current Capabilities

| Capability | State | Summary |
|------------|-------|---------|
| Natural language query assistance | Implemented | Tenant-scoped, guardrailed interfaces |
| Non-mutating responses | Implemented | AI does not apply changes to canonical records |
| Integration with canonical model | Implemented | Assistance oriented around normalized entities |
| Investigation context support | Partial | Depth varies by module; advanced scenario features may be limited |
| Audit of user-driven actions | Implemented | Human-initiated security actions remain auditable separately from AI text output |

## Current Limitations

- AI responses are **not** themselves tamper-evident audit records—capture decisions in standard workflows.
- **Export or copy** of AI text outside the platform is outside SentriScope control.
- Read-only assistance does **not** guarantee all relevant evidence appears in a single answer.
- Some tenants may have AI features **disabled** by policy.
- This document does **not** describe internal tool-calling mechanics or prompt structure.

## Frequently Asked Questions

### Can I ask the AI to mark a finding as accepted risk?

Disposition decisions are **human workflows**. AI does not autonomously apply risk acceptance or exception states.

### Does read-only mean the AI cannot suggest actions?

The AI may **suggest** analyst next steps in natural language. Suggestions are not executed automatically.

### How is this different from a SOAR playbook?

SOAR executes automated actions. SentriScope AI assistance described here does **not** replace SOAR; it supports analyst understanding within guardrails.

### Can AI access connector credentials?

No. Credential material is not exposed through AI assistance interfaces.

## Related Articles

- [LLM guardrails](LLM_GUARDRAILS.md)
- [AI limitations](AI_LIMITATIONS.md)
- [Canonical data model](../architecture/CANONICAL_DATA_MODEL.md)
- [Investigation workspace](../investigations/INVESTIGATION_WORKSPACE.md)
- [Role-based access control](../security/ROLE_BASED_ACCESS_CONTROL.md)

## Canonical References

| Source | Used for |
|--------|----------|
| `docs/current/architecture/ARCHITECTURE_LLM.md` | Read-only assistance boundaries (sanitized) |
| `docs/current/architecture/ARCHITECTURE_DATA.md` | Canonical data context for assistance |

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 2026-07-07 | AI Governance | Phase 2 initial draft |
