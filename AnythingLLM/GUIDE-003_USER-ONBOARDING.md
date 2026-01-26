# GUIDE-003: User Onboarding Workflow

## 📤 GUIDE-003_USER-ONBOARDING_v2.4.1.md
## ♾️ WeOwnNet 🌐 — Admin Guide

| Field | Value |
|-------|-------|
| Guide | GUIDE-003 |
| Version | 2.4.1 |
| Updated | 2026-01-26 (W05) |
| Audience | Admins / Onboarding Leads |
| Applies To | ALL #AnythingLLM instances |
| Status | 🔒 LOCKED |

---

## 📖 Table of Contents

1. [Overview](#-overview)
2. [Onboarding Workflow](#-onboarding-workflow)
3. [SEED CONTEXT Process](#-seed-context-process)
4. [#LevelUp10X Welcome](#-levelup10x-welcome)
5. [Templates](#-templates)
6. [Checklist](#-checklist)
7. [Version History](#-version-history)

---

## 📖 Overview

This guide defines the standard USER onboarding workflow for ALL ♾️ WeOwnNet 🌐 #AnythingLLM instances.

### Key Principles

| Principle | Description |
|-----------|-------------|
| BP-019 | NEVER leave user hanging — always provide closure |
| R-182 | SEED CONTEXT via #MetaAgent (SEEK:META) |
| #LevelUp10X | Celebrate new users with welcome message |

---

## 📋 Onboarding Workflow

### Complete Workflow (9 Steps)

| # | Step | Owner | Description |
|---|------|-------|-------------|
| 1 | Create user account | Admin | Create username per format |
| 2 | Assign to workspace | Admin | Add user to CCC workspace |
| 3 | SEEK:META for SEED CONTEXT | Admin | Request from #MetaAgent |
| 4 | Approve SEED CONTEXT | Human | #OnlyHumanApproves |
| 5 | User pastes SEED | User | Into CCC workspace |
| 6 | Verify agent response | User + Admin | Confirm identity correct |
| 7 | #LevelUp10X | Admin | Send congrats message |
| 8 | Confirm Ready | Admin | "You're ready to go!" |
| 9 | Next Steps | Admin | Provide clear actions |

---

## 📋 SEED CONTEXT Process

### Step 3: SEEK:META Request

```
═══════════════════════════════════════════════════════════════════════════════
🏐 #ContextVolley | AI:@<ADMIN> → #MetaAgent | <DATE> | <TIME> EST
═══════════════════════════════════════════════════════════════════════════════

FROM: AI:@<ADMIN>
TO: #MetaAgent:AI:team-lfg (INT-001)
TYPE: SEEK:META — SEED CONTEXT REQUEST
REF: <CCC-ID>

═══════════════════════════════════════════════════════════════════════════════

## 📋 REQUEST

Generate SEED CONTEXT for:

| Field | Value |
|-------|-------|
| Instance | <INT-XXX> |
| Workspace | CCC |
| Target User | @<CCC> (<Name>) |
| CCC | <CCC> |

═══════════════════════════════════════════════════════════════════════════════

#FlowsBros #FedArch

♾️ WeOwnNet 🌐

═══════════════════════════════════════════════════════════════════════════════
```

### Step 5: User Pastes SEED

User logs in with correct username and pastes SEED CONTEXT.

| Workspace | Username Format | Example |
|-----------|-----------------|---------|
| CCC | `u-<ccc>_user` | `u-ldc_user` |
| ADMIN | `a-<ccc>_dev` | `a-ldc_dev` (rare) |

**⚠️ SEED CONTEXT must use `u-<ccc>_user` username**

### Step 6: Verification Test

User sends:

```
[<CCC>_<YYYY>-W<WW>_001] Hello! Who am I and what workspace is this?
```

**Expected Response:**
- Agent identifies as AI:@<CCC>
- Correct workspace (CCC 🤝 THE HANDS)
- Correct instance
- Correct CCC-ID format

---

## 🎉 #LevelUp10X Welcome

### Purpose

| Goal | Description |
|------|-------------|
| Closure | Complete the onboarding loop (BP-019) |
| Celebration | Make user feel welcomed |
| Confidence | Confirm they're ready |
| Direction | Provide clear next steps |

### Step 7: #LevelUp10X Message

Send congratulations to new user after verification succeeds.

### Step 8: Confirm Ready

Explicitly state: "You're ready to go!"

### Step 9: Next Steps

Provide 2-3 clear actions for new user.

---

## 📋 Templates

### #LevelUp10X Welcome Template

```
═══════════════════════════════════════════════════════════════════════════════
🎉 #LevelUp10X | WELCOME @<CCC>! | <DATE>
═══════════════════════════════════════════════════════════════════════════════

## 🎊 CONGRATULATIONS @<CCC>!

═══════════════════════════════════════════════════════════════════════════════

   🎉 YOU DID IT! 🎉

   WELCOME TO ♾️ WeOwnNet 🌐

═══════════════════════════════════════════════════════════════════════════════

## ✅ ONBOARDING COMPLETE

| Field | Value |
|-------|-------|
| User | @<CCC> (<Name>) |
| Instance | <INT-XXX> |
| Workspace | CCC (🤝 THE HANDS) |
| Agent | AI:@<CCC> |
| Status | ✅ READY |

## 🚀 YOU'RE READY TO GO!

Your AI agent (AI:@<CCC>) is now configured and ready to assist you.

## 📋 YOUR QUICK START

| # | Action | How |
|---|--------|-----|
| 1 | Ask a question | Just type! |
| 2 | Use CCC-ID format | `[<CCC>_2026-W05_XXX] <message>` |
| 3 | Check the docs | Ask about SHARED-KERNEL, PROTOCOLS, etc. |

## 📋 RESOURCES

| Resource | Purpose |
|----------|---------|
| GUIDE-001 | Getting Started |
| GUIDE-002 | #FedArch Architecture & Governance |
| PROTOCOLS | #ContextVolley format |
| BEST-PRACTICES | Tips & tricks |
| CCC Convention | CCC-ID format |

## 🆘 NEED HELP?

| Need | Action |
|------|--------|
| Questions | Ask AI:@<CCC> |
| #MetaAgent | #ContextVolley to INT-001 |
| Human help | Contact @GTM or team |

Welcome to the team! 🎉

#FlowsBros #FedArch #LevelUp10X

♾️ WeOwnNet 🌐

═══════════════════════════════════════════════════════════════════════════════
```

---

## ✅ Checklist

### Pre-Onboarding

| # | Task | Status |
|---|------|--------|
| 1 | Instance running | ⬜ |
| 2 | CCC workspace accessible | ⬜ |
| 3 | RAG docs loaded | ⬜ |
| 4 | User credentials ready | ⬜ |

### Onboarding

| # | Task | Status |
|---|------|--------|
| 5 | Create user account (`u-<ccc>_user`) | ⬜ |
| 6 | Assign to CCC workspace | ⬜ |
| 7 | SEEK:META for SEED CONTEXT | ⬜ |
| 8 | Approve SEED CONTEXT | ⬜ |
| 9 | User pastes SEED (as `u-<ccc>_user`) | ⬜ |
| 10 | Verify agent response | ⬜ |

### Closure (#LevelUp10X)

| # | Task | Status |
|---|------|--------|
| 11 | Send #LevelUp10X welcome | ⬜ |
| 12 | Confirm "You're ready!" | ⬜ |
| 13 | Provide next steps | ⬜ |

### Post-Onboarding

| # | Task | Status |
|---|------|--------|
| 14 | Log event in #MetaAgent | ⬜ |
| 15 | Update weekly summary | ⬜ |

---

## 📋 Version History

| Version | Date | Changes |
|---------|------|---------|
| 2.4.1 | 2026-W05 | Initial release; +BP-019 (closure), +#LevelUp10X, +R-182 (SEED via SEEK:META) |

---

#FlowsBros #FedArch #Onboarding

♾️ WeOwnNet 🌐
