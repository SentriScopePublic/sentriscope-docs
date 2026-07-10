---
title: "Understanding Security Identities"
version: "1.0"
status: draft
classification: PUBLIC
tlp: TLP:CLEAR
disclosure_level: D0
knowledge_id: KID-CON-0090
knowledge_domain: education
knowledge_object: education
documentation_maturity: D1
knowledge_lifecycle: validated
knowledge_relationships:
  depends_on:
    - KID-GLS-0010
    - KID-CON-0089
    - KID-CON-0077
  explains:
    - KID-GLS-0010
  related_to:
    - KID-CON-0091
    - KID-GLS-0009
    - KID-CON-0040
  authority_reference:
    - KID-ARC-0001
navigation:
  knowledge_series: SER-009
  editorial_season: SEA-007
  pillar_page: PIL-IDENTITY
  learning_path: LP-009
  difficulty: introductory
  audience: [analyst, soc_manager]
  estimated_time_minutes: 9
  required_reading:
    - KID-GLS-0010
    - KID-CON-0089
    - KID-CON-0077
  recommended_next:
    - KID-CON-0091
website_slug: understanding-security-identities
last_updated: 2026-07-03
next_review: 2027-01-03
llm_summary: "A security identity is the actor every authentication event, access decision, investigation pivot, and attack-path step can attach to—not a directory row alone, but the anchor that explains who or what could cause harm."
knowledge_tags: [identity, education, decision-support, security-entities]
---

# Understanding Security Identities

## What practitioners need to know

Practitioners ask: *What is a security identity?* *Is it the same as an Active Directory account?*

Volume 3 continues with a different question: **Why are identities central to modern security?**

A **security identity** is a **user or service account** that can **authenticate**, **authorize**, **access**, or **act on** resources—human users, service principals, API keys tied to actors, and similar entities. Every login, privilege use, lateral movement step, and data access event ultimately points at an identity or the gap where an actor should be known.

Term authority: [Identity](../glossary/IDENTITY.md) (`KID-GLS-0010`).

This series teaches **security semantics**—how analysts reason about identities when prioritizing, investigating, and scoping blast radius. It is not IAM product administration or identity governance policy.

## Why every security decision touches an identity

| Decision type | Identity connection |
|---------------|---------------------|
| **Prioritization** | Which actor's activity or credential exposure deserves attention first? |
| **Investigation** | Who authenticated, from where, with what privilege? |
| **Containment** | Which accounts must be disabled, rotated, or session-revoked? |
| **Attack path analysis** | Which credential or role enables the next hop? |
| **Communication** | Was this a human user, shared account, or service principal? |

Without a clear identity anchor, teams debate alert severity while missing **who could act** and **what they could reach**.

## Identity as pivot, not peripheral metadata

Modern compromise rarely stops at a single host. Adversaries **live off credentials**—stolen passwords, session tokens, service accounts, and over-privileged roles. Identities are the **pivot** that connects:

```text
Initial access → credential abuse → lateral movement → data impact
         ↑              ↑                  ↑
    identity         identity           identity
```

[Security assets](./UNDERSTANDING_SECURITY_ASSETS.md) (`KID-CON-0080`) describe **what** can be harmed. Identities describe **who or what can cause harm**—and often determine which assets matter most in a given incident.

## Connection to Volumes 1–2 and SER-008

```text
Volume 1:  Evidence and findings need actor linkage
Volume 2:  Intelligence enriches who adversaries target and how they operate
SER-008:   Assets anchor what is at risk
SER-009:   Identities anchor who can reach it
```

[Security intelligence](./SECURITY_INTELLIGENCE_AS_DECISION_SUPPORT.md) (`KID-CON-0077`) adds context about campaigns and TTPs—but triage still asks: **which identities in our environment match that behavior?** [Security assets as decision support](./SECURITY_ASSETS_AS_DECISION_SUPPORT.md) (`KID-CON-0089`) established that entities carry explainable context; identities are the next entity in that chain.

## What security identities are

| A security identity is | A security identity is not |
|------------------------|----------------------------|
| A decision anchor for access and abuse | A completeness metric for directory sync |
| A pivot in investigations and paths | A username string in isolation |
| Enriched by privilege and lifecycle context | A static HR record |
| Linked to assets, apps, and sessions | An IAM ticket queue alone |
| Explicit when unknown or shared | Assumed because something logged a name |

## Common mistakes

| Mistake | Consequence |
|---------|-------------|
| Equating directory account count with identity maturity | False confidence in scope |
| Treating identities as IAM hygiene | Wrong investigation and containment lens |
| Ignoring service accounts in alert workflows | Missed lateral movement pivots |
| Assuming one source names the actor correctly | Split-brain attribution |
| Deferring identity linkage to closure | Shallow triage and incomplete revocation |

## Practical implications

1. **Ask which identity** before accepting a priority rank on authentication or access alerts.  
2. **Normalize actors** across IdP, directory, cloud IAM, and application logs (`KID-ARC-0001`).  
3. **Flag unknown, shared, or ambiguous identities** as decision uncertainty—not silent defaults.  
4. **Continue to** [Identity vs Account](./IDENTITY_VS_ACCOUNT.md) (`KID-CON-0091`) for the security concept vs directory record distinction.

## Limitations

Identity understanding is only as good as entity resolution, log coverage, and lifecycle freshness. Incomplete linkage produces incomplete decisions—with explicit gaps preferred over assumed completeness.

## Related knowledge

| KID | Resource |
|-----|----------|
| KID-GLS-0010 | [Identity](../glossary/IDENTITY.md) |
| KID-CON-0089 | [Security Assets as Decision Support](./SECURITY_ASSETS_AS_DECISION_SUPPORT.md) |
| KID-CON-0077 | [Security Intelligence as Decision Support](./SECURITY_INTELLIGENCE_AS_DECISION_SUPPORT.md) |
| KID-GLS-0009 | [Asset](../glossary/ASSET.md) |
| KID-CON-0040 | [Understanding Attack Paths](./UNDERSTANDING_ATTACK_PATHS.md) |

## Authority references

- `KID-ARC-0001` — [Canonical Data Model](../architecture/CANONICAL_DATA_MODEL.md)

## Why this matters for security decisions

Every prioritization, investigation scope, and containment plan eventually asks who could authenticate, escalate, or persist. When analysts treat identities as directory rows instead of decision anchors, severity scores float free of blast radius and access reach. Grounding work in security identities—known, contextualized, or explicitly unknown—turns abstract alerts into defensible choices about session revocation, credential rotation, and path scope.

## Revision History

| Version | Date | Summary |
|---------|------|---------|
| 1.0 | 2026-07-03 | Initial SER-009 article |
