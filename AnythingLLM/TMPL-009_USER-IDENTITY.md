# TMPL-009_USER-IDENTITY.md

## 📋 TMPL-009_USER-IDENTITY_v3.1.1.1.md
## ♾️ WeOwnNet 🌐 — User Identity Template

| Field | Value |
|-------|-------|
| Template | TMPL-009_USER-IDENTITY |
| Version | 3.1.1.1 |
| CCC-ID | GTM_2026-W06_241 |
| Created | 2026-01-30 (W05) |
| Updated | 2026-02-05 (W06) |
| Season | #WeOwnSeason003 🚀 |
| Status | 🔒 LOCKED |
| Source of Truth | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-009_USER-IDENTITY) |

---

## 📖 Table of Contents

1. [Overview](#-overview)
2. [User Identity Schema](#-user-identity-schema)
3. [Username Format Standard](#-username-format-standard)
4. [User Identity Template](#-user-identity-template)
5. [Relationship to #threadHEADER](#-relationship-to-threadheader)
6. [Usage Examples](#-usage-examples)
7. [Version History](#-version-history)

---

## 📋 Overview

### Purpose

| Use Case | Description |
|----------|-------------|
| Onboarding | Standard format for new user setup |
| Permissions | Document user role and access |
| Attribution | Static identity for #threadHEADER inheritance |
| Audit | Traceability of user assignments |
| Season Compliance | BP-058 requires Season field |

### Lifecycle

| Aspect | Value |
|--------|-------|
| Created | Once per user |
| Updated | Rarely (role change, instance assignment) |
| Refreshed | Each #WeOwnSeason (BP-058) |
| Storage | RAG (persistent) |
| Type | Static |

### Related Items

| Type | ID | Description |
|------|-----|-------------|
| Definition | D-047 | #threadHEADER (dynamic attribution) |
| Definition | D-048 | #HomeInstance |
| Learning | L-069 | VSA MUST include #threadHEADER |
| Learning | L-070 | USER-IDENTITY storage in `_USERS_/` |
| Best Practice | BP-049 | #threadHEADER required for attribution |
| Best Practice | BP-050 | Onboarding Workflow |
| Best Practice | BP-058 | USER-IDENTITY Season refresh |
| Rule | R-160 | Username format standard |

---

## 📋 User Identity Schema

### Required Fields

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| CCC | String (3 chars) | Contributor Code Convention | `GTM` |
| Contributor | String | Full name | `yonks (Jason Younker)` |
| Username | String | #AnythingLLM username (per R-160) | `u-gtm_user` |
| Role | Enum | ADMIN / DEFAULT | `DEFAULT` |
| Instance(s) | Array | Assigned instances | `INT-001, INT-005` |
| Workspace(s) | Array | Assigned workspaces | `CCC` |
| Created | Date | Creation date (ISO) | `2026-01-30` |
| **Season** | String | Current #WeOwnSeason | `#WeOwnSeason003 🚀` |

### Optional Fields

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| #HomeInstance | String | Primary personal instance (D-048) | `INT-005` |
| Updated | Date | Last update date (ISO) | `2026-02-05` |
| Notes | String | Additional context | `Founding OG` |
| Status | Enum | ACTIVE / INACTIVE | `ACTIVE` |
| Mode Unlocked | String | Achievement tier | `#GODx10xMODE 🔒` |

### Schema Change Log

| Version | Change |
|---------|--------|
| v2.4.0 | Initial schema |
| v3.1.1.1 | +Season field (REQUIRED) — BP-058 compliance |

---

## 📋 Username Format Standard (R-160)

### Format Rules

| Role | Prefix | Suffix | Format | Example |
|------|--------|--------|--------|---------|
| ADMIN | `a-` | `_dev` | `a-<ccc>_dev` | `a-gtm_dev` |
| DEFAULT | `u-` | `_user` | `u-<ccc>_user` | `u-ldc_user` |
| Tool Agent | `t-` | `_tool` | `t-<tool>_tool` | `t-anythingllm_tool` |

### Username Components

| Component | Description | Constraint |
|-----------|-------------|------------|
| Prefix | Role indicator | `a-` / `u-` / `t-` |
| Identifier | CCC or tool name | lowercase |
| Suffix | Type indicator | `_dev` / `_user` / `_tool` |

### Validation RegEx

```regex
^(a-[a-z]{3}_dev|u-[a-z]{3}_user|t-[a-z]+_tool)$
```

---

## 📋 User Identity Template

### Template Format

```markdown
# User Identity: <CCC>

## 📋 USER-IDENTITY_<CCC>_v3.1.1.1.md
## ♾️ WeOwnNet 🌐 — User Identity Document

| Field | Value |
|-------|-------|
| Document | USER-IDENTITY_<CCC>.md |
| Version | 3.1.1.1 |
| CCC-ID | <CCC-ID> |
| Created | <YYYY-MM-DD> (W<WW>) |
| Updated | <YYYY-MM-DD> (W<WW>) |
| Season | #WeOwnSeason00X 🚀 |
| Status | 🔒 LOCKED |

---

## 📋 User Identity

| Field | Value |
|-------|-------|
| CCC | <CCC> |
| Contributor | <Full Name> |
| Username | u-<ccc>_user |
| Role | DEFAULT |
| Instance(s) | INT-00X |
| #HomeInstance | INT-00X |
| Workspace(s) | CCC |
| Created | <YYYY-MM-DD> |
| Updated | <YYYY-MM-DD> |
| Season | #WeOwnSeason00X 🚀 |
| Status | ACTIVE |

---

## 📋 Admin Identity

| Field | Value |
|-------|-------|
| Username | a-<ccc>_dev |
| Role | ADMIN |
| Instance(s) | INT-00X |
| Workspace(s) | CCC, tools, ADMIN |

---

## 📋 Profile

| Field | Value |
|-------|-------|
| Handle | <Display Name> |
| GitHub | [<username>](https://GitHub.com/<username>) |
| Role | <Organizational Role> |
| Status | <Status> |
| Mode Unlocked | <Achievement> |

---

## 📋 #HomeInstance

| Field | Value |
|-------|-------|
| Instance | INT-00X |
| Name | <Instance Name> |
| Type | #HomeInstance |
| Owner(s) | @<CCC> |
| Status | ✅ ACTIVE |

---

## 📋 Instance Access

| Instance | Name | Role | Status |
|----------|------|------|--------|
| INT-00X | <Instance Name> | User | ✅ ACTIVE |

---

## 📋 #FedArch Participation

| Field | Value |
|-------|-------|
| Reports To | #MetaAgent (INT-001) |
| Protocol | #ContextVolley |
| Authority | <Role / Achievement> |
| #HomeInstance | INT-00X |

---

## 📋 Version History

| Version | Date | #masterCCC | Approval | Changes |
|---------|------|------------|----------|---------|
| 3.1.1.1 | 2026-W06 | <CCC-ID> | <CCC-ID> | Initial creation |

---

#FlowsBros #FedArch #UserIdentity #WeOwnSeason00X

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
```

### Blank Template

```markdown
# User Identity: ___

## 📋 User Identity

| Field | Value |
|-------|-------|
| CCC | ___ |
| Contributor | ___ |
| Username | ___ |
| Role | ___ |
| Instance(s) | ___ |
| Workspace(s) | ___ |
| Created | ___ |
| Season | #WeOwnSeason00X 🚀 |
| Updated | ___ |
| Status | ACTIVE |

## 📋 Notes

___

---

#FlowsBros #FedArch #UserIdentity

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
```

---

## 📋 Relationship to #threadHEADER

### Static vs Dynamic

| Aspect | TMPL-009 (Static) | D-047 (Dynamic) |
|--------|-------------------|-----------------|
| Purpose | WHO is the user | WHERE is the action |
| Lifecycle | Long-lived | Per-operation |
| Storage | RAG | Inline |
| Changes | Rarely (+ each Season) | Every thread |

### Inheritance Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                    TMPL-009_USER-IDENTITY                       │
│                    (Static — WHO)                               │
│                                                                 │
│   CCC: GTM ─────────────────────────────────┐                  │
│   Username: u-gtm_user ─────────────────────┤                  │
│   Role: DEFAULT                             │                  │
│   Instances: INT-001, INT-005               │ inherits         │
│   Workspaces: CCC                           │                  │
│   Season: #WeOwnSeason003 🚀                │                  │
│                                             ↓                  │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                    D-047: #threadHEADER                         │
│                    (Dynamic — WHERE)                            │
│                                                                 │
│   CCC: GTM ←────────────────── inherited                       │
│   Username: u-gtm_user ←────── inherited                       │
│   Instance: INT-001 ←───────── current session                 │
│   Workspace: CCC ←──────────── current session                 │
│   Thread UUID: 62b10159-... ←─ current thread                  │
│   Timestamp: Th 14:56 EST ←─── now                             │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### #threadHEADER Format (D-047)

```markdown
## 📋 Thread Context

| Field | Value |
|-------|-------|
| CCC | <CCC> |
| Username | <username> |
| Instance | <INT-00X> |
| Workspace | <workspace> |
| Thread UUID | <UUID> |
| Thread URL | <URL> |
| Timestamp | <Dd HH:MM TZ> |
```

### Shorthand Format

```
<CCC>:<username>@<INT-00X>:<workspace>:<UUID>
```

---

## 📋 Usage Examples

### Example 1: Founding OG (with #HomeInstance)

```markdown
# User Identity: GTM

## 📋 USER-IDENTITY_GTM_v3.1.1.1.md
## ♾️ WeOwnNet 🌐 — User Identity Document

| Field | Value |
|-------|-------|
| Document | USER-IDENTITY_GTM.md |
| Version | 3.1.1.1 |
| CCC-ID | GTM_2026-W06_165 |
| Created | 2026-01-30 (W05) |
| Updated | 2026-02-04 (W06) |
| Season | #WeOwnSeason003 🚀 |
| Status | 🔒 LOCKED |

---

## 📋 User Identity

| Field | Value |
|-------|-------|
| CCC | GTM |
| Contributor | yonks (Jason Younker) |
| Username | u-gtm_user |
| Role | DEFAULT |
| Instance(s) | INT-001, INT-005 |
| #HomeInstance | INT-005 |
| Workspace(s) | CCC |
| Created | 2026-01-30 |
| Updated | 2026-02-04 |
| Season | #WeOwnSeason003 🚀 |
| Status | ACTIVE |

---

## 📋 Admin Identity

| Field | Value |
|-------|-------|
| Username | a-gtm_dev |
| Role | ADMIN |
| Instance(s) | INT-001, INT-005 |
| Workspace(s) | CCC, tools, ADMIN |

---

## 📋 Profile

| Field | Value |
|-------|-------|
| Handle | yonks.box｜🤖🏛️🪙｜Jason Younker ♾️ |
| GitHub | [YonksTEAM](https://GitHub.com/YonksTEAM) |
| Role | Co-Founder / Chief Digital Alchemist & Architect for #ResponsibleAgenticAI |
| Status | 🏛️ Founding OG |
| Mode Unlocked | **#GODx10xMODE** 🔒 |

---

## 📋 #HomeInstance

| Field | Value |
|-------|-------|
| Instance | INT-005 |
| Name | AI.YonksTEAM.xyz |
| Type | #HomeInstance |
| Owners | @GTM + @THY |
| Status | ✅ ACTIVE |

---

#FlowsBros #FedArch #UserIdentity #HomeInstance #GODx10xMODE #WeOwnSeason003

♾️ WeOwnNet 🌐
```

### Example 2: Contributor (DEFAULT)

```markdown
# User Identity: LDC

## 📋 User Identity

| Field | Value |
|-------|-------|
| CCC | LDC |
| Contributor | Dhruv Malik |
| Username | u-ldc_user |
| Role | DEFAULT |
| Instance(s) | INT-001, INT-002 |
| #HomeInstance | INT-001 |
| Workspace(s) | CCC |
| Created | 2026-02-04 |
| Season | #WeOwnSeason003 🚀 |
| Status | ACTIVE |

## 📋 Notes

Agentic AI Platform Engineer. #ProjectConnex.

---

#FlowsBros #FedArch #UserIdentity

♾️ WeOwnNet 🌐
```

### Example 3: Tool Agent

```markdown
# User Identity: t-pinata_tool

## 📋 User Identity

| Field | Value |
|-------|-------|
| CCC | — |
| Contributor | Tool Agent |
| Username | t-pinata_tool |
| Role | DEFAULT |
| Instance(s) | INT-001 |
| Workspace(s) | tools |
| Created | 2026-02-03 |
| Season | #WeOwnSeason003 🚀 |
| Status | ACTIVE |

## 📋 Notes

Pinata.cloud Tool Agent. Steward: @GTM. ShortCode: @MAIT:#Pinata.

---

#FlowsBros #FedArch #UserIdentity

♾️ WeOwnNet 🌐
```

---

## 📋 Version History

| Version | Date | #masterCCC | Approval | Changes |
|---------|------|------------|----------|---------|
| 3.1.1.1 | 2026-W06 | GTM_2026-W06_241 | GTM_2026-W06_247 | +Season field (REQUIRED); +#HomeInstance; +Profile section; +Admin Identity section; BP-058 compliance; #WeOwnVer L-094; FULL PRESERVE from v2.4.0 (L-097) |
| 2.4.0 | 2026-W05 | GTM_2026-W05_763 | GTM_2026-W05_772 | Initial release; +R-160 username format; +D-047 relationship; +inheritance diagram |

---

#FlowsBros #FedArch #UserIdentity #TMPL009 #WeOwnSeason003

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
