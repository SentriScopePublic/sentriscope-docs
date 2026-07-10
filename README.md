# SentriScope

**Cyber Risk Intelligence Platform**

SentriScope helps security teams turn fragmented telemetry into **canonical understanding**, **explainable risk prioritization**, and **analyst-led investigation** — with multi-tenant governance and auditability.

**Website:** [https://sentriscope.com.br](https://sentriscope.com.br)

This repository is the public documentation set for SentriScope: product orientation, architecture concepts, security posture (public-safe), and cybersecurity knowledge articles.

---

## What is SentriScope?

SentriScope is a **Cyber Risk Intelligence Platform**. It is designed for security operations, vulnerability management, threat intelligence, and risk teams that need consolidated, tenant-governed visibility — not another disconnected tool console.

At a high level, SentriScope:

- **Ingests** security data through governed connectors (scanners, endpoint, identity, CMDB/ITSM, threat intelligence, and related sources)
- **Normalizes** that data into shared canonical entities (assets, identities, exposures, controls, incidents, threat intelligence, and more)
- **Prioritizes** risk with **deterministic, explainable** scoring (AI assistance is not in the critical scoring path)
- **Correlates** context for investigation — including threat intelligence enrichment and attack-path support
- **Supports** evidence-first investigation workflows where **human validation** remains required

SentriScope is **analyst-assisted**, not autonomous.

---

## Objective

The objective of SentriScope is to improve **security decision quality** under real operational constraints:

1. Reduce noise from multi-tool findings by normalizing evidence into one tenant-scoped model  
2. Make prioritization **traceable and explainable**, not opaque  
3. Give analysts investigation workflows grounded in **evidence and provenance**  
4. Preserve **enterprise controls** — multi-tenant isolation, RBAC, and tamper-evident audit logging  

In short: help teams decide **what matters**, **why**, and **what to do next** — with accountability.

---

## What SentriScope proposes

SentriScope proposes a layered operating model for cyber risk intelligence:

| Layer | Intent |
|-------|--------|
| Governed ingestion | Bring external security sources in with operational control and credential hygiene |
| Canonical normalization | Work across tools using shared entity concepts, not vendor-specific silos |
| Intelligence correlation | Enrich and relate findings with threat and operational context |
| Investigation workspace | Support analyst-led analysis, including attack-path oriented workflows |
| Decision & governance | Deterministic prioritization, explainability, overrides, and audit |

It is **not** positioned as a SIEM replacement, a SOAR replacement, an autonomous SOC, or a standalone vulnerability scanner. See [What SentriScope is not](platform/WHAT_SENTRISCOPE_IS_NOT.md).

---

## Benefits

| Benefit | Why it matters |
|---------|----------------|
| **Unified understanding** | Analysts work from canonical entities instead of reconciling raw tool exports by hand |
| **Explainable prioritization** | Risk decisions can be inspected; scoring is deterministic and separate from assistive AI |
| **Investigation support** | Evidence-oriented workflows and attack-path analysis support human conclusions |
| **Connector-driven coverage** | Expand visibility by integrating existing security investments rather than rip-and-replace |
| **Enterprise tenancy & audit** | Tenant isolation and security-relevant audit logging support governed multi-team use |
| **Honest product boundaries** | Public docs state limitations clearly — including what SentriScope does **not** replace |

---

## Start here

| Document | Description |
|----------|-------------|
| [What is SentriScope?](platform/WHAT_IS_SENTRISCOPE.md) | Product definition, capabilities, and limitations |
| [What SentriScope is not](platform/WHAT_SENTRISCOPE_IS_NOT.md) | Explicit boundaries (SIEM, SOAR, autonomous SOC, and more) |
| [Platform overview](platform/PLATFORM_OVERVIEW.md) | Conceptual layers of the platform |
| [Product maturity](platform/PRODUCT_MATURITY.md) | Honest maturity labels for capabilities |
| [Documentation index](INDEX.md) | Catalog of public articles |

Browse by topic: [platform](platform/), [architecture](architecture/), [security](security/), [knowledge](knowledge/), [intelligence](intelligence/), [investigations](investigations/), [AI](ai/), [FAQ](faq/), [glossary](glossary/).

---

## About this repository

- **Audience:** security practitioners, evaluators, partners, and anyone seeking public SentriScope documentation  
- **Content:** sanitized, evidence-based public documentation (PUBLIC · TLP:CLEAR)  
- **Not included:** application source code, internal engineering specifications, or confidential deployment detail  

SentriScope is **not open source**. This repository documents the product and related cybersecurity knowledge; it does not distribute the platform codebase.

## License

Documentation in this repository is available under [CC BY 4.0](LICENSE). SentriScope product software, trademarks, and private materials are not licensed under CC BY 4.0.
