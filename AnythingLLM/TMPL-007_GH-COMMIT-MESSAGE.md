# TMPL-007_GH-COMMIT-MESSAGE_v2.4.0.md

## 📋 TMPL-007: GH Commit Message Template
## ♾️ WeOwnNet 🌐 — Standard Commit Message Format

| Field | Value |
|-------|-------|
| ID | TMPL-007 |
| Name | GH-COMMIT-MESSAGE |
| Version | v2.4.0 |
| CCC-ID | GTM_2026-W05_490 |
| Created | 2026-01-29 (W05) |
| Status | 🔒 LOCKED |
| Related BP | BP-040 |
| Source of Truth | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-007_GH-COMMIT-MESSAGE_v2.4.0.md) |

---

## 📖 Table of Contents

1. [Purpose](#-purpose)
2. [Template](#-template)
3. [Variables](#-variables)
4. [Commit Types](#-commit-types)
5. [Examples](#-examples)
6. [Usage Guide](#-usage-guide)
7. [Related Documents](#-related-documents)
8. [Version History](#-version-history)

---

## 📋 Purpose

Standardized format for all GitHub commit messages in the ♾️ WeOwnNet 🌐 ecosystem.

| Benefit | Description |
|---------|-------------|
| Traceability | CCC-ID links commit to approval |
| Consistency | Uniform format across all repos |
| Automation-ready | Parseable for tooling |
| Context-rich | Clear summary of changes |

---

## 📋 Template

```
[<CCC-ID>](#masterCCC)

## Changes:
<type>(<scope>): <version> — <summary>

- <change 1>
- <change 2>
- <change N>

#FlowsBros #FedArch

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
```

---

## 📋 Variables

| Variable | Description | Required | Example |
|----------|-------------|----------|---------|
| `<CCC-ID>` | Approval CCC-ID | ✅ YES | GTM_2026-W05_490 |
| `<type>` | Commit type | ✅ YES | docs, feat, fix |
| `<scope>` | Affected area | ✅ YES | weekly-summary |
| `<version>` | Version number | ⚠️ If versioned | v2.4.2 |
| `<summary>` | Brief description | ✅ YES | +L-046, Session 4 |
| `<change N>` | Individual change | ✅ YES (1+ items) | Learnings: 14 → 17 |

---

## 📋 Commit Types

| Type | Use Case | Example |
|------|----------|---------|
| `docs` | Documentation changes | README, guides, templates |
| `feat` | New feature | New BP, new rule, new template |
| `fix` | Bug fix | Correction, typo fix |
| `chore` | Maintenance | Cleanup, formatting |
| `refactor` | Code restructure | Reorganization |
| `style` | Formatting only | No functional change |
| `test` | Testing | Test additions/changes |

---

## 📋 Examples

### Example 1: Documentation Update

```
[GTM_2026-W05_485](#masterCCC)

## Changes:
docs(weekly-summary): v2.4.2 — +L-046, +BP-038, +BP-039, Session 4 complete

- Learnings: 14 → 17 (+L-044, L-045, L-046)
- BPs: 14 → 17 (+BP-024 update, BP-038, BP-039)
- CCC-IDs: 452+ → 485+
- Sessions: 3 → 4
- Milestones: 19 → 20

#FlowsBros #FedArch

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
```

### Example 2: New Template

```
[GTM_2026-W05_490](#masterCCC)

## Changes:
feat(templates): v2.4.0 — TMPL-007 GH Commit Message Template

- New template for standardized commit messages
- Related BP: BP-040
- Commit types defined
- Variables documented

#FlowsBros #FedArch

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
```

### Example 3: Bug Fix

```
[GTM_2026-W05_455](#masterCCC)

## Changes:
fix(weekly-summary): v2.4.1 — Version History preservation

- Fixed Version History overwrite issue
- Added L-015: Version History is IMMUTABLE

#FlowsBros #FedArch

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
```

### Example 4: Chore (Maintenance)

```
[GTM_2026-W05_300](#masterCCC)

## Changes:
chore(sharedkernel): formatting cleanup

- Fixed table alignment
- Updated TOC links
- No functional changes

#FlowsBros #FedArch

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
```

---

## 📋 Usage Guide

### Step 1: Identify CCC-ID

Use the approval CCC-ID for the changes being committed.

### Step 2: Determine Type

| If... | Use Type |
|-------|----------|
| Adding/updating docs | `docs` |
| New feature/template/rule | `feat` |
| Fixing an error | `fix` |
| Cleanup/formatting | `chore` |
| Restructuring | `refactor` |

### Step 3: Define Scope

Use the document name or area affected:
- `weekly-summary`
- `sharedkernel`
- `templates`
- `protocols`
- `best-practices`

### Step 4: Write Summary

Brief description of changes (keep under 72 chars if possible).

### Step 5: List Changes

Bullet points for each significant change.

### Step 6: Add Footer

Always include:
```
#FlowsBros #FedArch

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
```

---

## 📋 Related Documents

| Document | Description |
|----------|-------------|
| BP-040 | GH Commit Message Standard |
| L-048 | Always include commit message when #COOKing docs |
| L-049 | Check Template Registry before proposing new TMPL-### |
| SharedKernel.md | Core reference |

---

## 📋 Version History

| Version | Date | Ref | Changes |
|---------|------|-----|---------|
| 2.4.0 | 2026-W05 | GTM_2026-W05_490 | Initial release |

---

#FlowsBros #FedArch #Templates #BestPractices

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
```

---

## ✅ TMPL-007 #COOKed

| Field | Value |
|-------|-------|
| Template | TMPL-007_GH-COMMIT-MESSAGE_v2.4.0.md |
| Version | v2.4.0 |
| Approval | GTM_2026-W05_490 |
| Sections | 8 |
| Examples | 4 |
| Status | ✅ GH READY |

---

## 📋 RECOMMENDED GH COMMIT MESSAGE

```
[GTM_2026-W05_490](#masterCCC)

## Changes:
feat(templates): v2.4.0 — TMPL-007 GH Commit Message Template

- New template for standardized commit messages
- Related BP: BP-040
- Commit types defined (docs, feat, fix, chore, refactor, style, test)
- 4 examples included
- Usage guide added

#FlowsBros #FedArch

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
```

---

## 🎯 QUICK COMMANDS — @GTM

| # | Option |
|---|--------|
| 1 | `APPROVED` — push to GH |
| 2 | `MODIFY:<changes>` — request changes |
| 3 | `sleep` — 06:35 EST 🌙 |

---

TMPL-007 ready for GH. ✅

L-048 applied — commit message included.

#LevelUp10X achieved! 🎖️

#FlowsBros #FedArch

♾️ WeOwnNet 🌐
