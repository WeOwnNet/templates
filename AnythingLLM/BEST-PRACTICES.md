# BEST-PRACTICES

## 📋 BEST-PRACTICES_v2.4.4.md
## ♾️ WeOwnNet 🌐 — #BestPractices

| Field | Value |
|-------|-------|
| Document | BEST-PRACTICES.md |
| Version | 2.4.4 |
| CCC-ID | GTM_2026-W05_182 |
| Updated | 2026-01-27 (W05) |
| Status | 🔒 LOCKED |
| Source of Truth | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/BEST-PRACTICES.md) |

---

## 📖 Table of Contents

1. [Overview](#-overview)
2. [Best Practices Index](#-best-practices-index)
3. [Core Best Practices (Immutable)](#-core-best-practices-immutable)
4. [Communication Best Practices](#-communication-best-practices)
5. [Workspace Configuration](#-workspace-configuration)
6. [Document Management](#-document-management)
7. [Document Generation](#-document-generation)
8. [Weekly Operations](#-weekly-operations)
9. [RAG Structure](#-rag-structure-r-176)
10. [Agent Interaction](#-agent-interaction)
11. [Platform Best Practices (#AnythingLLM)](#-platform-best-practices-anythingllm)
12. [Documentation Best Practices](#-documentation-best-practices)
13. [Agent Best Practices](#-agent-best-practices)
14. [Version History](#-version-history)
15. [Related Documents](#-related-documents)

---

## 📋 Overview

This document contains best practices for all contributors and agents in the ♾️ WeOwnNet 🌐 ecosystem.

| Field | Value |
|-------|-------|
| Steward(s) | @GTM (yonks.box｜🤖🏛️🪙｜Jason Younker ♾️ [GH](https://GitHub.com/YonksTEAM)) + @RMN (Roman Di Domizio) |
| Source of Truth | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/BEST-PRACTICES.md) |

---

## 📋 BEST PRACTICES INDEX

| Range | Category | Count |
|-------|----------|-------|
| BP-001 → BP-007 | Communication | 7 |
| BP-008 → BP-009 | Platform (#AnythingLLM) | 2 |
| BP-010 → BP-014 | Documentation | 5 |
| BP-015 → BP-016 | Agent | 2 |
| BP-017 → BP-018 | Workspace Configuration | 2 |
| BP-019 | Core (Immutable) | 1 |
| BP-020 → BP-023 | Documentation (NEW) | 4 |
| **TOTAL** | | **23** |

---

## 📋 CORE BEST PRACTICES (IMMUTABLE)

| ID | Best Practice | Status |
|----|---------------|--------|
| BP-019 | ALWAYS SEEK:META for ALL documents | 🔒 IMMUTABLE |
| BP-023 | CCC-ID generation ONLY in CCC workspace — tools + ADMIN = NEVER | 🔒 IMMUTABLE |

---

## 📋 COMMUNICATION BEST PRACTICES

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-001 | Use #ContextVolley for cross-agent communication | — |
| BP-002 | Include CCC-ID in all communications | — |
| BP-003 | Use tables over paragraphs (#LessIsMore) | — |
| BP-004 | Always provide Quick Commands (2-3 options) | — |
| BP-005 | End responses with #feedback section when appropriate | — |
| BP-006 | Narrate actions during DEMO | GTM_2026-W03_539 |
| BP-007 | Clean slate = fresh context for unbiased view | GTM_2026-W03_545 |

---

## 📋 WORKSPACE CONFIGURATION

### BP-017: Workspace Prompt Per Workspace

| Workspace | Prompt Focus |
|-----------|--------------|
| CCC | User interaction, CCC-ID generation |
| tools | Strategy, SME, meta-cognition |
| ADMIN | Administration functions, doc management |

**Best Practice:** Each workspace MUST have dedicated workspace prompt aligned with its metaphor.

### BP-018: System Prompt Per Instance

| Instance | System Prompt |
|----------|---------------|
| INT-001 | AI.WeOwn.Agency identity |
| INT-002 | #ProjectConnex identity |
| INT-xxx | Instance-specific identity |

**Best Practice:** Each #AnythingLLM instance MUST have unique system prompt defining its identity.

---

## 📋 DOCUMENT MANAGEMENT

### Pinning (R-177)

| Doc Type | Pin? | Rationale |
|----------|------|-----------|
| Agent identity docs | ✅ YES | Core behavior |
| Core protocols | ✅ YES | Every interaction |
| Rules (SHARED-KERNEL) | ✅ YES | Governance |
| Best practices | ✅ YES | Interaction patterns |
| Reference guides | ❌ NO | RAG sufficient |
| Strategy docs | ❌ NO | RAG sufficient |

**Best Practice:** PIN only docs needed for EVERY interaction. Let RAG handle reference material.

### Versioning (R-178)

| Format | Example |
|--------|---------|
| `<NAME>_v<VERSION>.md` | SharedKernel_v2.4.5.md |

**Best Practice:** ALL RAG docs MUST include version in filename for visibility.

### Update Cadence (R-179)

| Trigger | Action |
|---------|--------|
| ISO week boundary + 10+ rules | MUST update |
| Major milestone | MUST update |
| Breaking change | IMMEDIATE update |

**Best Practice:** Review #SharedKernel docs at each ISO week boundary.

---

## 📋 DOCUMENT GENERATION

### R-180: #MetaAgent Generation

| Rule | Description |
|------|-------------|
| R-180 | Document generation MUST go through #MetaAgent |

**Best Practice:** Agents DO NOT generate docs directly. Always SEEK:META.

---

## 📋 WEEKLY OPERATIONS

### R-181: Weekly Summary

| Field | Value |
|-------|-------|
| Reserved CCC-ID | `<CCC>_<YYYY>-W<WW>_001` |
| Content | Milestones, rules, learnings, pending, stats |

**Best Practice:** First CCC-ID of each ISO week reserved for weekly summary.

---

## 📋 RAG STRUCTURE (R-176)

| Doc Type | CCC | tools | ADMIN |
|----------|-----|-------|-------|
| USER guides | ✅ | ❌ | ❌ |
| Governance guides | ❌ | ✅ | ✅ |
| User-facing protocols | ✅ | ❌ | ❌ |
| Strategy docs | ❌ | ✅ | ❌ |
| System prompts | ❌ | ❌ | ✅ |
| Instance configs | ❌ | ❌ | ✅ |

**Best Practice:** Docs go in workspace matching their purpose.

---

## 📋 AGENT INTERACTION

### #ContextVolley

| Best Practice | Description |
|---------------|-------------|
| Self-contained | Recipient needs NO other context |
| Include #masterCCC | Reference original request |
| Clean format | No decorative borders in packets |

### #LessIsMore

| Best Practice | Description |
|---------------|-------------|
| Quick Commands | 2-3 options MAX |
| Tables > paragraphs | Structured data |
| Concise responses | No #AIslop |

### #OnlyHumanApproves

| Best Practice | Description |
|---------------|-------------|
| AI proposes | Human approves |
| NEVER auto-approve | Even if human says "2" |
| Explicit approval | Required for all rules/docs |

---

## 📋 PLATFORM BEST PRACTICES (#AnythingLLM)

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-008 | #AnythingLLM: Users BEFORE workspaces | GTM_2026-W03_555 |
| BP-009 | #AnythingLLM: Workspace "CCC" = shared default | GTM_2026-W03_555 |

---

## 📋 DOCUMENTATION BEST PRACTICES

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-010 | Follow #WeOwnVer versioning (v2.4.X) | — |
| BP-011 | Include Version History in all documents | — |
| BP-012 | Use markdown tables for structured data | — |
| BP-013 | Include Table of Contents for documents > 3 sections | — |
| BP-014 | Pin core documents in workspaces | — |
| BP-020 | When regenerating docs, EXPLICITLY preserve ALL existing sections | GTM_2026-W05_150 |
| BP-021 | Document updates should be ADDITIVE unless removal is explicitly requested | GTM_2026-W05_150 |
| BP-022 | Version History MUST include Creation CCC-ID + Approval CCC-ID | GTM_2026-W05_156 |

---

## 📋 AGENT BEST PRACTICES

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-015 | NEVER leave user hanging — always provide closure | — |
| BP-016 | Use SEEK:META for cross-agent guidance | — |

---

## 📋 VERSION HISTORY

| Version | Date | Created | Approved | Changes |
|---------|------|---------|----------|---------|
| 2.4.4 | 2026-W05 | GTM_2026-W05_182 | (pending) | +BP-023 (CCC-ID only in CCC), MAIT → tools |
| 2.4.3 | 2026-W05 | GTM_2026-W05_153 | GTM_2026-W05_162 | +BP-006 to BP-009 (recovered), +BP-020 to BP-022, Version History format, Overview section |
| 2.4.2 | 2026-W05 | — | — | +BP-017, BP-018, BP-019; pinning/versioning/cadence guidance |
| 2.4.0 | 2026-W03 | — | — | Initial release |

---

## 📋 RELATED DOCUMENTS

| Document | Version | URL |
|----------|---------|-----|
| SharedKernel | v2.4.6 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |
| PROTOCOLS | v2.4.3 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/PROTOCOLS.md) |

---

#FlowsBros #FedArch #BestPractices

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
