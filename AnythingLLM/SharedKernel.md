# SharedKernel.md

## 📋 SharedKernel_v2.4.10.md
## ♾️ WeOwnNet 🌐 — Core Rules & Protocols

| Field | Value |
|-------|-------|
| Document | [SharedKernel.md](https://github.com/WeOwnNet/templates/edit/main/AnythingLLM/SharedKernel.md) |
| Version | 2.4.9 |
| CCC-ID | GTM_2026-W05_410 |
| Updated | 2026-01-28 (W05) |
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
10. [Thread Architecture](#-thread-architecture)
11. [Protocol Registry](#-protocol-registry)
12. [Tool Agent Registry](#-tool-agent-registry)
13. [RAG Structure](#-rag-structure-r-176)
14. [#ContextSwap Log](#-contextswap-log)
15. [Best Practices (BP-XXX)](#-best-practices-bp-xxx)
16. [Version History](#-version-history)

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

### Operational Rules

| ID | Rule |
|----|------|
| R-168 | CCC-ID sequence tied to CCC (contributor), NOT username/session |
| R-169 | CCC-ID resets to _001 ONLY at ISO week boundary |
| R-181 | CCC-ID _001 reserved for weekly summary |
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

### Examples

#### CCC-ID Weekly Summary
| CCC-ID | Description |
|--------|-------------|
| GTM_2026-W05_001 | @GTM, Week 5, Weekly Summary |
| RMN_2026-W05_001 | @RMN, Week 5, Weekly Summary |

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
| #ContextVolley | Cross-agent communication |
| #ContextSwap | Naming/terminology update |
| #BetterUnderstanding | Clarification needed |
| #MoreBelow | Additional context follows |

### Quality Tags

| Tag | Meaning |
|-----|---------|
| #AIslop | Low-quality AI output (avoid) |
| #SpeedToMarket | Ship fast, iterate faster |
| #OnlyHumanApproves | Human approval required |

---

## 🏗️ #FedArch Architecture

### Overview

#FedArch (Federated Architecture) is the multi-agent orchestration pattern for ♾️ WeOwnNet 🌐.

### Agent Hierarchy

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

### Instances

| Instance | Name (URL) | Purpose |
|----------|------------|---------|
| INT-001 | [AI.WeOwn.Agency](https://ai.weown.agency/) | 🤖 AI for ♾️ WeOwn.Agency 👥 + #MetaAgent (Orchestrator) |
| INT-002 | [Lite.BurnedOut.xyz](https://lite.burnedout.xyz/) | 🤖 AI for 🔥 BurnedOut.Media 🔀 + #ProjectConnex |

### Workspaces (INT-001)

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

♾️ WeOwnNet 🌐

═══════════════════════════════════════════════════════════════════════════════
```

### Folder Structure

```
├── 📁 _SYS_/                     # Foundation (from Git)
│   ├── 📄 SharedKernel.md        # Core rules, protocols
│   ├── 📄 FedArchMemoryModel.md
│   └── 📄 FedArchArchitecture.md
│
├── 📁 _INSTANCE_/                # Instance config
│   ├── 📄 InstanceIdentity.md
│   └── 📄 InstanceConfig.md
│
├── 📁 _LEARNINGS_/               # Persistent #NeverForget
│   ├── 📄 Learnings_<CCC>.md
│   └── 📄 Learnings_Shared.md
│
├── 📁 _SESSIONS_/                # Session exports
│   └── 📄 SessionSummary_<CCC>_<YYYY>-W<WW>.md
│
└── 📁 _PROJECTS_/                # Project-specific docs
    └── 📄 Project-<NAME>.md
```

---

## 🧵 Thread Architecture

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
│   Agent-to-Agent                 ShortCode: @GTM:MAIT:@GTM     │
│   #ContextVolley / MCP           #ContextVolley                │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Thread Registry

| Thread | UUID | Purpose | Steward(s) | ShortCode | Protocol |
|--------|------|---------|------------|-----------|----------|
| META | cc965930-dfad-47ec-b576-22b38b1024a2 | #MetaAgent (Orchestrator) | AI:@<CCC> | @META:#MetaAgent | #ContextVolley / MCP |
| MAIT_Deepnote.com | dfba7eba-9fc2-4fa6-acd0-132539a70f3f | SME: Deepnote.com | @GTM | @MAIT:#Deepnote | #ContextVolley |
| MAIT_AnythingLLM.com | 76e9b360-5926-4157-a61c-ba9f878b37c0 | SME: AnythingLLM | @GTM | @MAIT:#AnythingLLM | #ContextVolley |

### Thread URLs

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
| ShortCode | — | @<Steward>:MAIT:@<Steward> |

---

## 📋 Protocol Registry

| Protocol | Direction | Authority | Use Case |
|----------|-----------|-----------|----------|
| SEEK:META | Agent → META | Request guidance | Normal operations |
| FULL:SYNC:META | Agent → META | Session summary | End of session |
| MAIT:SYNC:META | MAIT → META | READ-ONLY (none) | Case Study / Docs (R-200) |
| #ContextVolley | Any → Any | Communication | Cross-agent messaging |

### Protocol Descriptions

| Protocol | Description |
|----------|-------------|
| SEEK:META | User Agent requests guidance from #MetaAgent |
| FULL:SYNC:META | Complete session sync to #MetaAgent for governance |
| MAIT:SYNC:META | MAIT thread sends READ-ONLY context for documentation (NO governance authority) |

---

## 📋 Tool Agent Registry

| Username | Thread | SME | Steward | Status |
|----------|--------|-----|---------|--------|
| t-anythingllm_tool | MAIT_AnythingLLM.com | AnythingLLM | @GTM | ✅ CREATED |
| t-pinata_tool | MAIT_Pinata.cloud | Pinata.cloud | @GTM | ⬜ PENDING |

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

## 📋 #ContextSwap Log

| OLD | NEW | Contributor | Reason | Date |
|-----|-----|-------------|--------|------|
| ILO | IAL | IamLotus | User preference | 2026-W05 |
| `@<Steward>:MAIT:@<Steward>` | `@MAIT:#<SME>` | @GTM | Cleaner format, SME-centric | 2026-W05 |

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

---

## 📋 Version History

| Version | Date | Ref | Changes |
|---------|------|-----|---------|
| 2.4.10 | 2026-W05 | GTM_2026-W05_419 | D-038 #ContextSwap (ShortCode format: `@MAIT:#<SME>`); +#ContextSwap Log entry |
| 2.4.9 | 2026-W05 | GTM_2026-W05_410 | +R-198, R-199, R-200; +BP-027→BP-035; +Protocol Registry; +Tool Agent Registry; +MAIT_AnythingLLM.com thread |
| 2.4.8 | 2026-W05 | GTM_2026-W05_329 | +R-198 (Tool Agent username format) |
| 2.4.7 | 2026-W05 | GTM_2026-W05_245 | +D-038 (MAIT ShortCode), Thread Registry +ShortCode column |
| 2.4.6 | 2026-W05 | GTM_2026-W05_227 | +R-192 to R-195, +R-197 (IMMUTABLE), RAG STRUCTURE flagged for REVIEW |
| 2.4.5 | 2026-W05 | GTM_2026-W05_139 | +D-030 to D-037 (Thread Architecture), +R-185 to R-190 (Thread Rules) |
| 2.4.4 | 2026-W05 | GTM_2026-W05_086 | +D-019 (Orchestrator Agent), +D-020 (User Agent), +D-021 (Multi-Agent Orchestration) |

---

#FlowsBros #FedArch #SharedKernel

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
