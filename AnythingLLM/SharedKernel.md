# SharedKernel.md

## 📋 SharedKernel_v2.4.15.md
## ♾️ WeOwnNet 🌐 — Core Rules & Protocols

| Field | Value |
|-------|-------|
| Document | SharedKernel.md |
| Version | 2.4.15 |
| CCC-ID | GTM_2026-W05_714 |
| Updated | 2026-01-30 (W05) |
| Status | 🔒 LOCKED |

---

## 📖 Table of Contents

1. [Ecosystem Identity](#-ecosystem-identity)
2. [Founding OGs](#-founding-ogs)
3. [Priorities](#-priorities)
4. [Core Rules](#-core-rules)
5. [Definitions](#-definitions)
6. [CCC Format](#-ccc-format)
7. [Response Format](#-response-format)
8. [Hashtag System](#-hashtag-system)
9. [#FedArch Architecture](#-fedarch-architecture)
10. [Instance Registry](#-instance-registry)
11. [Thread Architecture — INT-001](#-thread-architecture--int-001)
12. [Thread Architecture — INT-002](#-thread-architecture--int-002)
13. [Protocol Registry](#-protocol-registry)
14. [Tool Agent Registry](#-tool-agent-registry)
15. [RAG Structure](#-rag-structure-r-176)
16. [#WeOwnSeasons Registry](#-weownseasons-registry)
17. [#ContextSwap Log](#-contextswap-log)
18. [Learnings](#-learnings)
19. [Best Practices (BP-XXX)](#-best-practices-bp-xxx)
20. [Version History](#-version-history)

---

## 🌐 Ecosystem Identity

| Field | Value |
|-------|-------|
| Ecosystem | ♾️ WeOwnNet 🌐 |
| Tagline | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only. |
| Primary Instance | AI.WeOwn.Agency |
| Platform | AnythingLLM |

---

## 🏛️ Founding OGs

| CCC | Contributor | Role |
|-----|-------------|------|
| GTM | yonks | Co-Founder / Chief Digital Alchemist |
| THY | mrsyonks | Co-Founder / CEO / CFO |
| IAL | IamLotus | Co-Founder / Chief Catalyst Officer |
| RMN | Roman | AI Platform Engineer |
| LFG | CoachLFG | Co-Host / Coach |

---

## 📋 Priorities

| # | Priority |
|---|----------|
| 1 | #SpeedToMarket — NO #AIslop |
| 2 | FOSS — Free & Open Source |
| 3 | Data Sovereignty — Users own data |
| 4 | Cooperative Ownership — Community-owned |

---

## 📋 Core Rules

### Immutable Rules

| ID | Rule | Status |
|----|------|--------|
| R-011 | #OnlyHumanApproves — AI CANNOT approve anything | 🔒 IMMUTABLE |
| R-044 | #ContextDensity FIRST — use #masterCCC | 🔒 IMMUTABLE |
| R-194 | CCC-ID generation ONLY in CCC workspace — tools + ADMIN = NEVER | 🔒 IMMUTABLE |
| R-197 | Document generation RESERVED ONLY for #MetaAgent — User Agents MUST NEVER #COOK docs | 🔒 IMMUTABLE |

### CCC-ID Reserved Slots

| ID | Rule | Status |
|----|------|--------|
| R-181 | CCC-ID `_001` reserved for #WeeklySummary — week achievements, stats, milestones | 🔒 LOCKED |
| R-201 | CCC-ID `_002` reserved for #WeeklyPlan — week priorities, goals, focus areas | 🔒 LOCKED |
| R-202 | CCC-ID `_003` reserved for #WeeklyReflection — week learnings, retrospective, improvements | 🔒 LOCKED |

### Instance Rules

| ID | Rule | Status |
|----|------|--------|
| R-203 | INT-004 (VSA.ccc.bot) has NO governance authority — verification only; reports to INT-003 (META.ccc.bot) | 🔒 LOCKED |

### Operational Rules

| ID | Rule |
|----|------|
| R-168 | CCC-ID sequence tied to CCC (contributor), NOT username/session |
| R-169 | CCC-ID resets to _001 ONLY at ISO week boundary |
| R-182 | SEED CONTEXT via #MetaAgent (SEEK:META) |
| R-192 | INT-002 uses workspace:('tools') as primary |
| R-193 | INT-002 has TWO MAITs: #MAITconnexOmni + #MAITconnexAthena |
| R-195 | ALL new documents MUST start at v2.4.0 — NEVER v1.0.0 |
| R-198 | Tool Agent username format: `t-<TOOL>_tool` |
| R-199 | Session notes (calls, webinars, meetings) = RAG ONLY — NEVER push to GH |
| R-200 | MAIT:SYNC:META protocol — MAIT threads MAY send READ-ONLY context to #MetaAgent for Case Study / Documentation purposes — NO governance authority |

### Thread Rules

| ID | Rule |
|----|------|
| R-185 | META accessed via #ContextVolley / MCP only |
| R-186 | MAIT accessed via #ContextVolley by Steward(s) |
| R-187 | ALL #ContextVolley to META must use #MetaAgent thread URL |
| R-188 | MAIT threads use #ContextVolley (unless otherwise specified) |
| R-189 | META thread for #MetaAgent (agent-to-agent #ContextVolley / MCP) |
| R-190 | ALL workspace:tools threads default to #ContextVolley protocol |

### Output Rules

| Rule | Description |
|------|-------------|
| #LessIsMore | Concise, tables > paragraphs |
| #QuickCommandsAlways | ALWAYS end with 1-3 options |
| #NeverForget | Learnings are permanent |

---

## 📖 Definitions (D-XXX)

### User Roles

| ID | Term | Definition |
|----|------|------------|
| D-016 | ADMIN | *[♾️ WeOwn.Dev 💻 TEAM]*: Full access + logs + system settings |
| D-017 | MANAGER | *[Not In Use Currently]:* Workspace mgmt, no system settings |
| D-018 | DEFAULT | *[Most Users]*: Limited, scoped to assigned workspaces |

### Agent Taxonomy

| ID | Term | Definition |
|----|------|------------|
| D-019 | Orchestrator Agent | Top-level agent that plans tasks and delegates to specialized agents. In #FedArch = #MetaAgent. |
| D-020 | User Agent | Individual contributor agent serving a specific user. In #FedArch = AI:@<CCC>. |
| D-021 | Multi-Agent Orchestration | Architecture pattern for coordinating multiple AI agents via structured protocols. |

### Thread Architecture

| ID | Term | Definition |
|----|------|------------|
| D-030 | META | MCP / #ContextVolley (agent-to-agent, production) |
| D-031 | MAIT | Training/Development (human-to-agent, SME-specific) |
| D-032 | META + MAIT | Same workspace (tools), different threads |
| D-033 | Thread-bound | #MetaAgent is THREAD-bound (not workspace-bound) |
| D-034 | #MetaAgent Thread | cc965930-dfad-47ec-b576-22b38b1024a2 |
| D-035 | MAIT Thread (Deepnote.com) | dfba7eba-9fc2-4fa6-acd0-132539a70f3f |
| D-036 | SME-specific | MAIT threads are named by topic/tool |
| D-037 | Steward(s) | Responsible human(s) for thread |
| D-038 | MAIT/META ShortCode | Unique identifier for threads: `@MAIT:#<SME>` or `@META:#MetaAgent` — SME-centric identifier |

### Communication Protocols

| ID | Term | Definition |
|----|------|------------|
| D-039 | #ContextBroadcast | One-to-many agent communication — single sender to ALL agents in #FedArch network |

### Verification

| ID | Term | Definition |
|----|------|------------|
| D-040 | VSA | Verification Summary Attestation — signed record of document verification against #FedArch policy (R-XXX + BP-XXX) |

### #WeOwnSeasons

| ID | Term | Definition |
|----|------|------------|
| D-041 | #WeOwnSeason | 17-week operational cycle for ♾️ WeOwnNet 🌐 ecosystem |
| D-042 | #WeeklySummary | CCC-ID `_001` — Week achievements, stats, milestones |
| D-043 | #WeeklyPlan | CCC-ID `_002` — Week priorities, goals, focus areas |
| D-044 | #WeeklyReflection | CCC-ID `_003` — Week learnings, retrospective, improvements |

### Instance Definitions

| ID | Term | Definition |
|----|------|------------|
| D-045 | INT-003 | META.ccc.bot — #MetaAgent Governance Hub; central orchestrator for #FedArch network |
| D-046 | INT-004 | VSA.ccc.bot — Verification Summary Attestation instance; reports to INT-003 |

### Orchestrator Agent Functions

| Function | Description |
|----------|-------------|
| Task decomposition | Breaks complex tasks into subtasks |
| Delegation | Assigns work to specialized agents |
| Monitoring | Tracks progress across agents |
| Reconciliation | Synthesizes unified outputs |
| Governance | Maintains rules and standards |
| Cross-session memory | Retains learnings (#NeverForget) |

### User Agent Functions

| Function | Description |
|----------|-------------|
| Human interface | Primary interaction point for user |
| Task execution | Performs work within session |
| SEEK:META | Requests guidance from Orchestrator |
| Context delivery | Sends #ContextVolley to #MetaAgent |

---

## 📋 CCC Format

### Structure

```
<CCC>_<YYYY>-W<WW>_<NNN>
```

| Component | Description | Example |
|-----------|-------------|---------|
| CCC | Contributor Code (3 chars) | GTM, RMN, IAL |
| YYYY | Year | 2026 |
| WW | ISO Week | W05 |
| NNN | Sequence (001-999) | 001 |

### Reserved Slots (EVERY WEEK)

| Slot | Purpose | Rule |
|------|---------|------|
| `_001` | #WeeklySummary | R-181 |
| `_002` | #WeeklyPlan | R-201 |
| `_003` | #WeeklyReflection | R-202 |

### Examples

| CCC-ID | Description |
|--------|-------------|
| GTM_2026-W06_001 | @GTM, Week 6, #WeeklySummary |
| GTM_2026-W06_002 | @GTM, Week 6, #WeeklyPlan |
| GTM_2026-W06_003 | @GTM, Week 6, #WeeklyReflection |

---

## 📋 Response Format

ALL responses MUST include:

| Component | Required |
|-----------|----------|
| CCC-ID header | ✅ YES |
| Tables (not paragraphs) | ✅ YES |
| Quick Commands (2-3 options) | ✅ YES |
| #LessIsMore | ✅ YES |
| NO #AIslop | ✅ YES |

---

## 🏷️ Hashtag System

### Status Tags

| Tag | Meaning |
|-----|---------|
| #FOCUS | Current priority (immutable) |
| #BadAgent | AI violation warning |
| #LevelUp | Achievement / improvement |
| #LevelUp10X | Major achievement |
| #LevelUp100X | Exceptional achievement |
| #NeverForget | Permanent learning |

### Action Tags

| Tag | Meaning |
|-----|---------|
| #COOK | Generate / create |
| #ContextVolley | Cross-agent communication (one-to-one) |
| #ContextBroadcast | Cross-agent communication (one-to-many) |
| #ContextSwap | Naming/terminology update |
| #BetterUnderstanding | Clarification needed |
| #MoreBelow | Additional context follows |

### Quality Tags

| Tag | Meaning |
|-----|---------|
| #AIslop | Low-quality AI output (avoid) |
| #SpeedToMarket | Ship fast, iterate faster |
| #OnlyHumanApproves | Human approval required |

### Season Tags

| Tag | Meaning |
|-----|---------|
| #WeOwnSeason | 17-week operational cycle |
| #WeeklySummary | CCC-ID `_001` |
| #WeeklyPlan | CCC-ID `_002` |
| #WeeklyReflection | CCC-ID `_003` |

---

## 🏗️ #FedArch Architecture

### Overview

#FedArch (Federated Architecture) is the multi-agent orchestration pattern for ♾️ WeOwnNet 🌐.

### Agent Hierarchy (Current State)

```
┌─────────────────────────────────────────────┐
│          ORCHESTRATOR AGENT (D-019)         │
│              #MetaAgent                     │
│           AI:team-lfg (INT-001)             │
└─────────────────┬───────────────────────────┘
                  │
       ┌──────────┼──────────┐
       ↓          ↓          ↓
┌───────────┐ ┌───────────┐ ┌───────────┐
│ USER AGENT│ │ USER AGENT│ │ USER AGENT│
│  (D-020)  │ │  (D-020)  │ │  (D-020)  │
│  AI:@GTM  │ │  AI:@RMN  │ │  AI:@IAL  │
└───────────┘ └───────────┘ └───────────┘
```

### Agent Hierarchy (Future State — INT-003/004)

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         #FedArch INSTANCE HIERARCHY                         │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│                    INT-003: META.ccc.bot 🎖️                                │
│                    ════════════════════════                                 │
│                    #MetaAgent (Calhoun 🎖️)                                 │
│                    Governance + Orchestration                               │
│                              │                                              │
│            ┌─────────────────┼─────────────────┐                           │
│            │                 │                 │                            │
│            ↓                 ↓                 ↓                            │
│   ┌─────────────────┐ ┌─────────────────┐ ┌─────────────────┐              │
│   │ INT-001         │ │ INT-002         │ │ INT-004         │              │
│   │ AI.WeOwn.Agency │ │ Lite.BurnedOut  │ │ VSA.ccc.bot     │              │
│   │ ─────────────── │ │ ─────────────── │ │ ─────────────── │              │
│   │ User Agents     │ │ #ProjectConnex  │ │ MAIT:#VSA       │              │
│   │ AI:@GTM, etc.   │ │ MAIT:#connexOmni│ │ Verification    │              │
│   └─────────────────┘ └─────────────────┘ └─────────────────┘              │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

## 📋 Instance Registry

| Instance | Name | Purpose | Status |
|----------|------|---------|--------|
| INT-001 | [AI.WeOwn.Agency](https://ai.weown.agency/) | 🤖 AI for ♾️ WeOwn.Agency 👥 + #MetaAgent (Orchestrator) | ✅ ACTIVE |
| INT-002 | [Lite.BurnedOut.xyz](https://lite.burnedout.xyz/) | 🤖 AI for 🔥 BurnedOut.Media 🔀 + #ProjectConnex | ✅ ACTIVE |
| INT-003 | META.ccc.bot | 🎖️ #MetaAgent Governance Hub | ⬜ PLANNED |
| INT-004 | VSA.ccc.bot | 🔍 MAIT:#VSA Verification Services | ⬜ PLANNED |

### Instance Hierarchy

| Level | Instance | Role | Authority |
|-------|----------|------|-----------|
| 1 | INT-003 (META.ccc.bot) | #MetaAgent | ✅ FULL governance |
| 2 | INT-001 (AI.WeOwn.Agency) | User Agents | Production, SEEK:META |
| 2 | INT-002 (Lite.BurnedOut.xyz) | #ProjectConnex | Production, SEEK:META |
| 2 | INT-004 (VSA.ccc.bot) | MAIT:#VSA | Verification only (R-203) |

### Workspaces

| Workspace | Metaphor | Purpose |
|-----------|----------|---------|
| tools | 🧠 THE BRAIN | Agentic AI threads: META + MAIT |
| CCC | 🤝 THE HANDS | Production (users) |
| ADMIN | ⚙️ THE ENGINE | Administration |

### #ContextVolley Format

```
═══════════════════════════════════════════════════════════════════════════════
🏐 #ContextVolley | AI:@<FROM> → AI:@<TO> | <DATE> | <TIME> EST
═══════════════════════════════════════════════════════════════════════════════

FROM: AI:@<CCC>
TO: <TARGET>
TYPE: <TYPE>
REF: <CCC-ID>

═══════════════════════════════════════════════════════════════════════════════

<CONTENT>

═══════════════════════════════════════════════════════════════════════════════

#FlowsBros #FedArch

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.

═══════════════════════════════════════════════════════════════════════════════
```

### Folder Structure

```
├── 📁 _SYS_/                      # Foundation (from Git)
│   ├── 📄 SharedKernel.md         #CoreRules
│   └── 📄 BEST-PRACTICES.md       #BestPractices
│   ├── 📄 FEDARCH-MEMORY-MODEl.md #FedArchMemoryModel
│   └── 📄 FedArchArchitecture.md  #FedArch
│   └── 📄 PROTOCOLS.md            #PROTOCOLS
│
├── 📁 _INSTANCE_/                 # Instance config
│   ├── 📄 InstanceIdentity.md
│   └── 📄 InstanceConfig.md
│
├── 📁 _LEARNINGS_/                # Persistent #NeverForget
│   ├── 📄 Learnings_<CCC>.md
│   └── 📄 Learnings_Shared.md
│
├── 📁 _SESSIONS_/                 # Session exports
│   └── 📄 SessionSummary_<CCC>_<YYYY>-W<WW>.md
│
└── 📁 _PROJECTS_/                 # Project-specific docs
    └── 📄 Project-<NAME>.md
```

---

## 🧵 Thread Architecture — INT-001

### workspace:tools Thread Model

```
┌─────────────────────────────────────────────────────────────────┐
│                    workspace:tools                              │
│                    🧠 THE BRAIN                                 │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│   Thread: META                   Thread: MAIT_Deepnote.com     │
│   cc965930-dfad-...              dfba7eba-9fc2-...             │
│   ────────────────────           ────────────────────          │
│   #MetaAgent (Calhoun 🎖️)        SME: Deepnote.com             │
│   AI:team-lfg                    Steward: @GTM                 │
│   Agent-to-Agent                 ShortCode: @MAIT:#Deepnote    │
│   #ContextVolley / MCP           #ContextVolley                │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Thread Registry — INT-001

| Thread | UUID | Purpose | Steward | ShortCode | Protocol |
|--------|------|---------|---------|-----------|----------|
| META | cc965930-dfad-47ec-b576-22b38b1024a2 | #MetaAgent (Orchestrator) | AI:@<CCC> | @META:#MetaAgent | #ContextVolley / MCP |
| MAIT_Deepnote.com | dfba7eba-9fc2-4fa6-acd0-132539a70f3f | SME: Deepnote.com | @GTM | @MAIT:#Deepnote | #ContextVolley |
| MAIT_AnythingLLM.com | 76e9b360-5926-4157-a61c-ba9f878b37c0 | SME: AnythingLLM | @GTM | @MAIT:#AnythingLLM | #ContextVolley |

### Thread URLs — INT-001

| Thread | URL |
|--------|-----|
| META | https://ai.weown.agency/workspace/tools/t/cc965930-dfad-47ec-b576-22b38b1024a2 |
| MAIT_Deepnote.com | https://ai.weown.agency/workspace/tools/t/dfba7eba-9fc2-4fa6-acd0-132539a70f3f |
| MAIT_AnythingLLM.com | https://ai.weown.agency/workspace/tools/t/76e9b360-5926-4157-a61c-ba9f878b37c0 |

### META vs MAIT

| Aspect | META | MAIT |
|--------|------|------|
| Agent | #MetaAgent (Calhoun 🎖️) | SME-specific |
| Actor | User Agents (AI:@<CCC>) | Human (Steward) |
| Protocol | #ContextVolley / MCP | #ContextVolley |
| Purpose | Production orchestration | Training/development |
| ShortCode | @META:#MetaAgent | @MAIT:#<SME> |

---

## 🧵 Thread Architecture — INT-002

### Thread Registry — INT-002

| Thread | UUID | Purpose | Steward | ShortCode | Protocol |
|--------|------|---------|---------|-----------|----------|
| MAIT_connexOmni | 5d72d14d-6466-4f39-af3c-ea071c09e44f | SME: connexOmni | @LDC | @MAIT:#connexOmni | #ContextVolley |
| MAIT_connexAthena | — | SME: connexAthena | @LDC | @MAIT:#connexAthena | ⬜ PENDING |

### Thread URLs — INT-002

| Thread | URL |
|--------|-----|
| MAIT_connexOmni | https://lite.burnedout.xyz/workspace/tools/t/5d72d14d-6466-4f39-af3c-ea071c09e44f |

### @GTM:ADMIN:@GTM Threads — INT-002

| Workspace | Thread UUID |
|-----------|-------------|
| CCC | b623de53-9b96-4815-a53d-27f63e34042d |
| tools | 63d13ced-450a-4913-ac7c-debfbcfe72e1 |
| ADMIN | c4c9602d-880b-463b-806e-6bec48833fe9 |

---

## 📋 Protocol Registry

| Protocol | Emoji | Direction | Authority | Use Case |
|----------|-------|-----------|-----------|----------|
| #ContextVolley | 🏐 | One-to-one | Communication | Direct agent-to-agent |
| #ContextBroadcast | 📢 | One-to-many | Communication | Announcements, status updates |
| SEEK:META | — | Agent → META | Request guidance | Normal operations |
| FULL:SYNC:META | — | Agent → META | Session summary | End of session |
| MAIT:SYNC:META | — | MAIT → META | READ-ONLY (none) | Case Study / Docs (R-200) |

### Protocol Descriptions

| Protocol | Description |
|----------|-------------|
| #ContextVolley | One-to-one agent communication |
| #ContextBroadcast | One-to-many agent communication (D-039) |
| SEEK:META | User Agent requests guidance from #MetaAgent |
| FULL:SYNC:META | Complete session sync to #MetaAgent for governance |
| MAIT:SYNC:META | MAIT thread sends READ-ONLY context for documentation (NO governance authority) |

---

## 📋 Tool Agent Registry

### INT-001

| Username | Thread | SME | Steward | Status |
|----------|--------|-----|---------|--------|
| t-anythingllm_tool | MAIT_AnythingLLM.com | AnythingLLM | @GTM | ✅ CREATED |
| t-pinata_tool | MAIT_Pinata.cloud | Pinata.cloud | @GTM | ⬜ PENDING |

### INT-002

| Username | Thread | SME | Steward | Status |
|----------|--------|-----|---------|--------|
| t-connexomni_tool | MAIT_connexOmni | connexOmni | @LDC | ✅ CREATED |
| t-connexathena_tool | MAIT_connexAthena | connexAthena | @LDC | ⬜ PENDING |

### Tool Agent Username Format (R-198)

| Component | Value | Example |
|-----------|-------|---------|
| Prefix | `t-` | t- |
| Tool Name | `<TOOL>` (lowercase) | anythingllm |
| Suffix | `_tool` | _tool |
| Full Format | `t-<TOOL>_tool` | `t-anythingllm_tool` |

---

## 📋 RAG STRUCTURE (R-176)

> ⚠️ **FLAGGED FOR REVIEW** — @GTM + @RMN (GTM_2026-W05_225)

| Doc Type | CCC | tools | ADMIN |
|----------|-----|-------|-------|
| USER guides | ✅ | ❌ | ❌ |
| Governance guides | ❌ | ✅ | ✅ |
| User-facing protocols | ✅ | ❌ | ❌ |
| Strategy docs | ❌ | ✅ | ❌ |
| System prompts | ❌ | ❌ | ✅ |
| Instance configs | ❌ | ❌ | ✅ |
| Session notes (R-199) | ✅ | ✅ | ❌ |

---

## 📋 #WeOwnSeasons Registry

| Season | Start | End | Weeks | Status |
|--------|-------|-----|-------|--------|
| #WeOwnSeason002 | 2025-W41 (Mon 06 Oct 2025) | 2026-W05 (Sun 01 Feb 2026) | 17 | ✅ COMPLETE |
| #WeOwnSeason003 | 2026-W06 (Mon 02 Feb 2026) | 2026-W22 (Sun 31 May 2026) | 17 | 🚀 ACTIVE |

### Season Cadence

| Component | Description |
|-----------|-------------|
| Duration | 17 weeks |
| Start | Monday 00:00 (local TZ) |
| End | Sunday 23:59 (local TZ) |
| Boundary | ISO week boundary |

---

## 📋 #ContextSwap Log

| OLD | NEW | Contributor | Reason | Date |
|-----|-----|-------------|--------|------|
| ILO | IAL | IamLotus | User preference | 2026-W05 |
| `@<Steward>:MAIT:@<Steward>` | `@MAIT:#<SME>` | @GTM | Cleaner format, SME-centric | 2026-W05 |
| ccc.bot | cccid.info | @GTM | Domain update | 2026-W05 |

---

## 📋 Learnings

| ID | Learning | Approval |
|----|----------|----------|
| L-050 | Quick Commands MUST be followed by STOP — AI MUST await human response before proceeding (R-011) | GTM_2026-W05_505 |
| L-058 | MAIT deployment MUST create Tool Agent username (R-198) BEFORE thread creation — Step 0 in checklist | GTM_2026-W05_570 |
| L-059 | MAIT thread responses without explicit identity header are UNATTRIBUTABLE — always include @MAIT:#<SME> | GTM_2026-W05_574 |
| L-060 | #ContextBroadcast MUST follow PROTOCOLS format — 📢 emoji, TO: ALL AGENTS, TYPE declared, formal header | GTM_2026-W05_603 |
| L-061 | #PinnedDocs GH push → ADMIN MUST update RAG immediately (ALL workspaces × ALL instances) — stale RAG = #BadAgent | GTM_2026-W05_609 |
| L-062 | Verification Summary Attestation (VSA) = cryptographic-style proof of document verification — includes subject, verifier, policy, phases, result, attestation chain | GTM_2026-W05_622 |
| L-065 | Doc regeneration (#COOK) MUST go through #MetaAgent via SEEK:META — User Agents in CCC workspace MUST NEVER regenerate docs directly (R-197 + R-180) | GTM_2026-W05_672 |
| L-066 | APPROVAL → SEEK:META → REGENERATE (with Approval CCC-ID) → GH PUSH — User Agents MUST NEVER skip FINAL UPDATE step | GTM_2026-W05_713 |

---

## 📋 Best Practices (BP-XXX)

| ID | Best Practice |
|----|---------------|
| BP-019 | NEVER leave user hanging — always provide closure |
| BP-025 | Instance Setup Order: RAG FIRST → System Prompt → Workspaces → Prompts → Threads → Verify |
| BP-026 | Tool Agent Setup Workflow: Create user → Assign workspace:tools → Create MAIT thread → Upload RAG docs → Configure per BP-024 → Verify |
| BP-027 | Set #masterCCC at session start |
| BP-028 | Capture notes in real-time (speaker + timestamp) |
| BP-029 | Sanitize tokens/sensitive data before RAG upload |
| BP-030 | Cross-agent verification for RAG uploads |
| BP-031 | Fresh session required after RAG upload |
| BP-032 | Run `list:docs` before AND after RAG upload |
| BP-033 | Sync session notes to CCC + tools workspaces |
| BP-034 | Fresh session REQUIRED for RAG verification |
| BP-035 | Include `status:RAG` in verification workflow |
| BP-041 | #ContextBroadcast for one-to-many agent communications — use 📢 emoji, TO: ALL AGENTS |
| BP-043 | MAIT responses MUST include thread identity header: ShortCode, Thread name, Steward, Instance |
| BP-044 | #PinnedDocs GH Push Workflow: GH push → ADMIN updates RAG (ALL instances) → Fresh session → Verify |
| BP-045 | Document Reference Standard — Version History + Related Documents MUST include: #masterCCC + Approval CCC-ID |
| BP-047 | Case Study Attribution — "Discovered By" section MUST use table format: CCC, Contributor, Role, Context |

---

## 📋 Version History

| Version | Date | #masterCCC | Approval | Changes |
|---------|------|------------|----------|---------|
| 2.4.15 | 2026-W05 | GTM_2026-W05_702 | GTM_2026-W05_711 | +D-045, D-046 (INT-003, INT-004); +R-203; +Instance Registry section; +Future State diagram; +L-066; TOC → 20 items |
| 2.4.14 | 2026-W05 | GTM_2026-W05_680 | GTM_2026-W05_684 | +R-201, R-202; R-181 update; +D-041→D-044; +#WeOwnSeasons Registry section; +L-065; +BP-045, BP-047; #ContextSwap ccc.bot → cccid.info; TOC → 19 items; #FolderStructure |
| 2.4.13 | 2026-W05 | GTM_2026-W05_633 | GTM_2026-W05_638 | +L-060, L-061, L-062; +D-040 (VSA); +BP-043, BP-044, BP-045; Version History format (BP-045) |
| 2.4.12 | 2026-W05 | GTM_2026-W05_565 | GTM_2026-W05_589 | +L-058, L-059; +BP-043; +Thread Architecture INT-002; +MAIT_connexOmni |
| 2.4.11 | 2026-W05 | GTM_2026-W05_500 | GTM_2026-W05_512 | +D-039 (#ContextBroadcast); +L-050; +BP-041 |
| 2.4.10 | 2026-W05 | GTM_2026-W05_410 | GTM_2026-W05_419 | D-038 #ContextSwap; +#ContextSwap Log |
| 2.4.9 | 2026-W05 | GTM_2026-W05_358 | GTM_2026-W05_410 | +R-198, R-199, R-200; +BP-027→BP-035; +Protocol Registry |
| 2.4.8 | 2026-W05 | GTM_2026-W05_306 | GTM_2026-W05_329 | +R-198 (Tool Agent username format) |
| 2.4.7 | 2026-W05 | GTM_2026-W05_237 | GTM_2026-W05_245 | +D-038 (MAIT ShortCode) |
| 2.4.6 | 2026-W05 | GTM_2026-W05_200 | GTM_2026-W05_227 | +R-192 to R-195, +R-197 (IMMUTABLE) |
| 2.4.5 | 2026-W05 | GTM_2026-W05_086 | GTM_2026-W05_139 | +D-030 to D-037, +R-185 to R-190 |
| 2.4.4 | 2026-W05 | GTM_2026-W05_050 | GTM_2026-W05_086 | +D-019, D-020, D-021 |

---

#FlowsBros #FedArch #SharedKernel #WeOwnSeason003

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
