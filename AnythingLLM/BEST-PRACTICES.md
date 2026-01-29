# BEST-PRACTICES

## 📋 BEST-PRACTICES_v2.4.7.md
## ♾️ WeOwnNet 🌐 — #BestPractices

| Field | Value |
|-------|-------|
| Document | BEST-PRACTICES.md |
| Version | 2.4.7 |
| CCC-ID | GTM_2026-W05_415 |
| Updated | 2026-01-28 (W05) |
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
14. [Tool Agent Best Practices](#-tool-agent-best-practices)
15. [Notes-to-RAG Best Practices](#-notes-to-rag-best-practices)
16. [Version History](#-version-history)
17. [Related Documents](#-related-documents)

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
| BP-020 → BP-024 | Documentation (Enhanced) | 5 |
| BP-025 → BP-026 | Instance & Tool Setup | 2 |
| BP-027 → BP-035 | Notes-to-RAG | 9 |
| **TOTAL** | | **35** |

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
| tools | Strategy, SME, meta-cognition, META + MAIT threads |
| ADMIN | Administration functions, doc management |

**Best Practice:** Each workspace MUST have dedicated workspace prompt aligned with its metaphor.

### BP-018: System Prompt Per Instance

| Instance | System Prompt |
|----------|---------------|
| INT-001 | AI.WeOwn.Agency identity |
| INT-002 | #ProjectConnex identity |
| INT-xxx | Instance-specific identity |

**Best Practice:** Each #AnythingLLM instance MUST have unique system prompt defining its identity.

### Initial Deployment

| # | Workspace | Purpose |
|---|-----------|---------|
| 1 | tools | 🧠 THE BRAIN — META + MAIT threads |
| 2 | CCC | 🤝 THE HANDS — Production (users) |

**Best Practice:** Initial #FedArch deployment = 2 workspaces (tools + CCC).

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
| `<NAME>_v<VERSION>.md` | SHARED-KERNEL_v2.4.3.md |

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
| R-197 | Document generation RESERVED ONLY for #MetaAgent — User Agents MUST NEVER #COOK docs |

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

> **#MAITlivesInAthread** — MAIT = thread within workspace:tools, NOT a separate workspace (GTM_2026-W05_237)

| Doc Type | CCC | tools | ADMIN |
|----------|-----|-------|-------|
| USER guides | ✅ | ❌ | ❌ |
| Governance guides | ❌ | ✅ | ✅ |
| User-facing protocols | ✅ | ❌ | ❌ |
| Strategy docs | ❌ | ✅ | ❌ |
| System prompts | ❌ | ❌ | ✅ |
| Instance configs | ❌ | ❌ | ✅ |
| Session notes (R-199) | ✅ | ✅ | ❌ |

**Best Practice:** Docs go in workspace matching their purpose. workspace:tools = standard for #FedArch.

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
| BP-024 | MAIT Thread Configuration (see below) | GTM_2026-W05_242 |

### BP-024: MAIT Thread Configuration

| # | Requirement | Example |
|---|-------------|---------|
| 1 | Thread name = MAIT_<SME> | MAIT_Deepnote.com |
| 2 | workspace:tools prompt MUST include: | |
| 2a | — MAIT name | "You are MAIT_Deepnote.com..." |
| 2b | — Steward(s) assigned | Steward: @GTM |
| 2c | — MAIT ShortCode (D-038) | @MAIT:#Deepnote |
| 2d | — Relevant details | SME focus, protocols, etc. |

**Best Practice:** MAIT threads MUST be fully configured with identity, steward, and ShortCode.

---

## 📋 AGENT BEST PRACTICES

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-015 | NEVER leave user hanging — always provide closure | — |
| BP-016 | Use SEEK:META for cross-agent guidance | — |

---

## 📋 TOOL AGENT BEST PRACTICES

### BP-025: Instance Setup Order

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-025 | #AnythingLLM new instance setup: RAG FIRST → System Prompt → Workspaces → Workspace Prompts → Threads → Verify | GTM_2026-W05_306 |

### BP-026: Tool Agent Setup Workflow

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-026 | Tool Agent Setup Workflow (see below) | GTM_2026-W05_327 |

### BP-026 Steps

| # | Step | Description |
|---|------|-------------|
| 1 | Create user | Format: `t-<TOOL>_tool` (R-198) |
| 2 | Assign to workspace | workspace:tools only |
| 3 | Create MAIT thread | Format: `MAIT_<Tool>` |
| 4 | Upload RAG docs | Official tool documentation |
| 5 | Configure per BP-024 | MAIT name, Steward, ShortCode, details |
| 6 | Verify | Test retrieval + agent behavior |

**Best Practice:** Tool Agents follow standardized setup workflow for consistency.

---

## 📋 NOTES-TO-RAG BEST PRACTICES

> **R-199:** Session notes (calls, webinars, meetings) = RAG ONLY — NEVER push to GH

### Session Capture

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-027 | Set #masterCCC at session start | GTM_2026-W05_358 |
| BP-028 | Capture notes in real-time (speaker + timestamp) | GTM_2026-W05_359–370 |

### Pre-Upload

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-029 | Sanitize tokens/sensitive data before RAG upload | GTM_2026-W05_381 |

### Upload Process

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-032 | Run `list:docs` before AND after RAG upload | @GTM_ADMIN |
| BP-033 | Sync session notes to CCC + tools workspaces | @GTM_ADMIN |

### Verification

| ID | Best Practice | Source |
|----|---------------|--------|
| BP-030 | Cross-agent verification for RAG uploads | GTM_2026-W05_388 |
| BP-031 | Fresh session required after RAG upload | THY_2026-W05_018 |
| BP-034 | Fresh session REQUIRED for RAG verification | THY_2026-W05_018 |
| BP-035 | Include `status:RAG` in verification workflow | @GTM_ADMIN |

### Notes-to-RAG Workflow Summary

| Phase | BPs | Description |
|-------|-----|-------------|
| Capture | BP-027, BP-028 | Set #masterCCC, real-time notes |
| Sanitize | BP-029 | Remove tokens, sensitive data |
| Upload | BP-032, BP-033 | Pre/post check, multi-workspace sync |
| Verify | BP-030, BP-031, BP-034, BP-035 | Cross-agent, fresh session, status check |

### Related Documents

| Document | Purpose |
|----------|---------|
| GUIDE-005_Notes-to-RAG | Step-by-step workflow |
| TEMPLATE_NOTES | Reusable notes template |
| CASE-STUDY-001_Notes-to-RAG-Workflow | Full case study |

---

## 📋 VERSION HISTORY

| Version | Date | Ref | Changes |
|---------|------|-----|---------|
| 2.4.7 | 2026-W05 | GTM_2026-W05_415 | +BP-027→BP-035 (Notes-to-RAG); +Notes-to-RAG section; SharedKernel → v2.4.10 |
| 2.4.6 | 2026-W05 | GTM_2026-W05_329 | +BP-025, +BP-026 (Tool Agent Setup), +Tool Agent section, SharedKernel → v2.4.8 |
| 2.4.5 | 2026-W05 | GTM_2026-W05_245 | +BP-024 (enhanced — MAIT Thread Config), SharedKernel → v2.4.7, +REF column, +#MAITlivesInAthread |
| 2.4.4 | 2026-W05 | GTM_2026-W05_182 | +BP-023 (CCC-ID only in CCC), MAIT → tools |
| 2.4.3 | 2026-W05 | GTM_2026-W05_162 | +BP-006 to BP-009 (recovered), +BP-020 to BP-022, Version History format, Overview section |
| 2.4.2 | 2026-W05 | — | +BP-017, BP-018, BP-019; pinning/versioning/cadence guidance |
| 2.4.0 | 2026-W03 | — | Initial release |

---

## 📋 RELATED DOCUMENTS

| Document | Version | URL |
|----------|---------|-----|
| SharedKernel | v2.4.10 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |
| PROTOCOLS | v2.4.3 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/PROTOCOLS.md) |
| GUIDE-005_Notes-to-RAG | v2.4.0 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/GUIDE-005_Notes-to-RAG_v2.4.0.md) |
| TEMPLATE_NOTES | v2.4.0 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TEMPLATE_NOTES_v2.4.0.md) |
| CASE-STUDY-001_Notes-to-RAG-Workflow | v2.4.0 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/case-studies/CASE-STUDY-001_Notes-to-RAG-Workflow_v2.4.0.md) |

---

#FlowsBros #FedArch #BestPractices

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
