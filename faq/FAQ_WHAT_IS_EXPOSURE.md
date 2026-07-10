---
title: "What is exposure?"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-FAQ-0056
knowledge_domain: faq
knowledge_object: faq
documentation_maturity: D1
attached_to:
  - KID-CON-0110
knowledge_relationships:
  depends_on:
    - KID-CON-0110
  explains:
    - KID-CON-0110
    - KID-GLS-0007
website_slug: faq-what-is-exposure
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "Exposure is a security finding that links a weakness to a specific asset or environment—not a CVE catalog entry or scanner count alone."
---

# What is exposure?

## Short answer

**Exposure** is a security finding that links a **weakness** to a **specific asset or environment**—answering *this resource, here, under these conditions*—not a CVE catalog entry or vulnerability count by itself.

## Explanation

Practitioners often conflate exposure with vulnerability backlogs. Exposure is **decision-oriented**: it ties a flaw or misconfiguration to where it exists and why that placement matters. The same CVE can produce many exposures across assets; remediation and priority depend on **which exposures exist where**, enriched by context from assets, applications, and intelligence.

Term authority: [Exposure](../glossary/EXPOSURE.md) (`KID-GLS-0007`).

Guide: [Understanding Security Exposure](../knowledge/UNDERSTANDING_SECURITY_EXPOSURE.md) (`KID-CON-0110`).

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial FAQ (SER-011) |
