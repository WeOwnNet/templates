# TMPL-009_USER-IDENTITY.md

## 📋 TMPL-009_USER-IDENTITY_v2.4.0.md
## ♾️ WeOwnNet 🌐 — User Identity Template

| Field | Value |
|-------|-------|
| Template | TMPL-009_USER-IDENTITY |
| Version | 2.4.0 |
| CCC-ID | GTM_2026-W05_773 |
| Updated | 2026-01-30 (W05) |
| Status | 🔒 LOCKED |
| Source of Truth | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-009_USER-IDENTITY_v2.4.0.md) |

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

### Lifecycle

| Aspect | Value |
|--------|-------|
| Created | Once per user |
| Updated | Rarely (role change, instance assignment) |
| Storage | RAG (persistent) |
| Type | Static |

### Related Items

| Type | ID | Description |
|------|-----|-------------|
| Definition | D-047 | #threadHEADER (dynamic attribution) |
| Learning | L-069 | VSA MUST include #threadHEADER |
| Best Practice | BP-049 | #threadHEADER required for attribution |
| Rule | R-160 | Username format standard |

---

## 📋 User Identity Schema

### Required Fields

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| CCC | String (3 chars) | Contributor Code Convention | `GTM` |
| Contributor | String | Full name | `yonks` |
| Username | String | #AnythingLLM username (per R-160) | `a-gtm_dev` |
| Role | Enum | ADMIN / DEFAULT | `ADMIN` |
| Instance(s) | Array | Assigned instances | `INT-001, INT-002` |
| Workspace(s) | Array | Assigned workspaces | `CCC, tools, ADMIN` |
| Created | Date | Creation date (ISO) | `2026-01-30` |

### Optional Fields

| Field | Type | Description | Example |
|-------|------|-------------|---------|
| Updated | Date | Last update date (ISO) | `2026-01-30` |
| Notes | String | Additional context | `Founding OG` |
| Status | Enum | ACTIVE / INACTIVE | `ACTIVE` |

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

## 📋 User Identity

| Field | Value |
|-------|-------|
| CCC | <CCC> |
| Contributor | <Full Name> |
| Username | <username> |
| Role | <ADMIN / DEFAULT> |
| Instance(s) | <INT-00X, ...> |
| Workspace(s) | <workspace, ...> |
| Created | <YYYY-MM-DD> |
| Updated | <YYYY-MM-DD> |
| Status | <ACTIVE / INACTIVE> |

## 📋 Notes

<Optional notes about user>

---

#FlowsBros #FedArch #UserIdentity

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
| Changes | Rarely | Every thread |

### Inheritance Diagram

```
┌─────────────────────────────────────────────────────────────────┐
│                    TMPL-009_USER-IDENTITY                       │
│                    (Static — WHO)                               │
│                                                                 │
│   CCC: GTM ─────────────────────────────────┐                  │
│   Username: a-gtm_dev ──────────────────────┤                  │
│   Role: ADMIN                               │                  │
│   Instances: INT-001, INT-002               │ inherits         │
│   Workspaces: CCC, tools, ADMIN             │                  │
│                                             ↓                  │
└─────────────────────────────────────────────────────────────────┘
                              │
                              ↓
┌─────────────────────────────────────────────────────────────────┐
│                    D-047: #threadHEADER                         │
│                    (Dynamic — WHERE)                            │
│                                                                 │
│   CCC: GTM ←────────────────── inherited                       │
│   Username: a-gtm_dev ←─────── inherited                       │
│   Instance: INT-001 ←───────── current session                 │
│   Workspace: tools ←────────── current session                 │
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

### Example 1: Founding OG (ADMIN)

```markdown
# User Identity: GTM

## 📋 User Identity

| Field | Value |
|-------|-------|
| CCC | GTM |
| Contributor | yonks |
| Username | a-gtm_dev |
| Role | ADMIN |
| Instance(s) | INT-001, INT-002 |
| Workspace(s) | CCC, tools, ADMIN |
| Created | 2026-01-15 |
| Updated | 2026-01-30 |
| Status | ACTIVE |

## 📋 Notes

Founding OG. Co-Founder / Chief Digital Alchemist.

---

#FlowsBros #FedArch #UserIdentity

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
```

### Example 2: Contributor (DEFAULT)

```markdown
# User Identity: LDC

## 📋 User Identity

| Field | Value |
|-------|-------|
| CCC | LDC |
| Contributor | Dhruv |
| Username | u-ldc_user |
| Role | DEFAULT |
| Instance(s) | INT-002 |
| Workspace(s) | CCC, tools |
| Created | 2026-01-20 |
| Updated | — |
| Status | ACTIVE |

## 📋 Notes

Agentic AI Engineer / Project Lead. #ProjectConnex.

---

#FlowsBros #FedArch #UserIdentity

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
```

### Example 3: Tool Agent

```markdown
# User Identity: t-vsa_tool

## 📋 User Identity

| Field | Value |
|-------|-------|
| CCC | — |
| Contributor | Tool Agent |
| Username | t-vsa_tool |
| Role | DEFAULT |
| Instance(s) | INT-001 |
| Workspace(s) | tools |
| Created | 2026-01-30 |
| Updated | — |
| Status | ACTIVE |

## 📋 Notes

VSA Framework Tool Agent. Steward: @GTM.

---

#FlowsBros #FedArch #UserIdentity

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
```

---

## 📋 Version History

| Version | Date | #masterCCC | Approval | Changes |
|---------|------|------------|----------|---------|
| 2.4.0 | 2026-W05 | GTM_2026-W05_763 | GTM_2026-W05_772 | Initial release; +R-160 username format; +D-047 relationship; +inheritance diagram |

---

#FlowsBros #FedArch #UserIdentity #TMPL009

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
