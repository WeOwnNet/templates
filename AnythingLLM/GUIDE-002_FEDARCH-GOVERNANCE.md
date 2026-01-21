## GUIDE-002_FEDARCH-GOVERNANCE.md v2.4.0

# GUIDE-002: #FedArch Architecture & Governance

## Version

| Field | Value |
|-------|-------|
| ID | GUIDE-002 |
| Version | v2.4.0 |
| Created | 2026-01-21 |
| Updated | 2026-01-21 |
| Source | GTM_2026-W04_083 |
| Audience | ADMINs, MAITs, Project Leads |
| Prerequisites | GUIDE-001, SharedKernel.md |
| Status | ✅ #SharedKernel |

---

## 📋 1. OVERVIEW

### What is #FedArch?

#FedArch (Federated Architecture) is the governance and technical framework for the ♾️ WeOwnNet 🌐 ecosystem. It enables multiple #AnythingLLM instances to operate as a coordinated network while maintaining data sovereignty and cooperative ownership.

### Core Principles

| # | Principle | Description |
|---|-----------|-------------|
| 1 | #OnlyHumanApproves | AI cannot approve — only human approves |
| 2 | #LessIsMore | Concise, tables > paragraphs |
| 3 | #NeverForget | Learnings permanent |
| 4 | #SpeedToMarket | NO #AIslop |
| 5 | FOSS | Free & Open Source |
| 6 | Data Sovereignty | Users own data |
| 7 | Cooperative Ownership | Community-owned |

### Key Components

| Component | Description |
|-----------|-------------|
| Instances | Independent #AnythingLLM deployments |
| #MetaAgent | Governance coordinator (AI:team-lfg) |
| #SharedKernel | Single source of truth |
| Protocols | Standardized communication |
| CCC | Contributor Code Convention |

---

## 📋 2. ARCHITECTURE

### Network Diagram

```
═══════════════════════════════════════════════════════════════════════════════

                         ♾️ WeOwnNet 🌐 #FedArch NETWORK

═══════════════════════════════════════════════════════════════════════════════

                              ┌─────────────────┐
                              │   #MetaAgent    │
                              │  AI:team-lfg    │
                              │  Calhoun 🎖️    │
                              └────────┬────────┘
                                       │
                         #ContextVolley│#SharedKernel
                                       │
              ┌────────────────────────┼────────────────────────┐
              │                        │                        │
              ▼                        ▼                        ▼
    ┌─────────────────┐      ┌─────────────────┐      ┌─────────────────┐
    │    INT-001      │      │    INT-002      │      │    INT-###      │
    │ AI.WeOwn.Agency │      │ #ProjectConnex  │      │    (Future)     │
    │    @GTM 🍬      │      │    @LDC         │      │                 │
    └────────┬────────┘      └────────┬────────┘      └─────────────────┘
             │                        │
             │                        │
    ┌────────┴────────┐      ┌────────┴────────┐
    │   AI:@GTM       │      │   AI:@LDC       │
    │   AI:@RMN       │      │   AI:@SHD       │
    └─────────────────┘      └─────────────────┘

═══════════════════════════════════════════════════════════════════════════════
```

### Instances

| ID | Name | URL | Lead | Status |
|----|------|-----|------|--------|
| INT-001 | AI.WeOwn.Agency | ai.weown.agency | @GTM | ✅ LIVE |
| INT-002 | #ProjectConnex | Lite.BurnedOut.xyz | @LDC | ✅ LIVE |

### Instance Types

| Type | Description | Example |
|------|-------------|---------|
| Primary | Main ecosystem instance | INT-001 |
| Project | Project-specific instance | INT-002 |
| Future | Planned expansion | INT-### |

### Multi-Instance Design

| Principle | Description |
|-----------|-------------|
| Independence | Each instance operates autonomously |
| Synchronization | #SharedKernel keeps all aligned |
| Federation | Instances coordinate via #ContextVolley |
| Sovereignty | Data stays within instance |

---

## 📋 3. GOVERNANCE

### #Human+AI+Human Model

```
═══════════════════════════════════════════════════════════════════════════════

   HUMAN (Request) → AI (Propose) → HUMAN (Approve/Reject)

   #OnlyHumanApproves

═══════════════════════════════════════════════════════════════════════════════
```

| Stage | Actor | Action |
|-------|-------|--------|
| 1 | Human | Requests action |
| 2 | AI | Proposes solution |
| 3 | Human | Approves or rejects |

### Governance Rules

| ID | Rule |
|----|------|
| GOV-001 | #Human+AI+Human — All AI actions require human approval |
| GOV-002 | Routing — Proper escalation paths |
| GOV-003 | #FULLSYNC — Context must be synchronized |

### #OnlyHumanApproves

| ✅ AI CAN | ❌ AI CANNOT |
|-----------|--------------|
| Propose | Approve |
| Recommend | Authorize |
| Draft | Finalize |
| Suggest | Decide |

### Key Governance Rules

| ID | Rule |
|----|------|
| R-106 | AI CANNOT APPROVE — only human approves |
| R-107 | #OnlyHumanApproves — AI proposes, human disposes |
| R-123 | AI response options CANNOT include "APPROVE" |
| R-124 | All approval requests → @GTM:ai:@GTM → @GTM (human) |

---

## 📋 4. PROTOCOLS

### Protocol Summary

| Protocol | Name | Description |
|----------|------|-------------|
| #ContextVolley | AI-to-AI Communication | Structured packet exchange |
| #NeverForget | Knowledge Persistence | Learnings locked permanently |
| VERIFY | Onboarding Validation | 7-question test |
| FULL:SYNC | Full Synchronization | Complete context transfer |
| FULL:SYNC:P2P | Peer-to-Peer Sync | 8-packet sync |
| FULL:SYNC:META | MetaAgent Sync | Session summary |
| SEEK:META | Guidance Request | Request #MetaAgent guidance |

### #ContextVolley

AI-to-AI communication protocol for structured packet exchange.

**Format:**
```
🏐 #ContextVolley | <FROM> → <TO> | <DATE> | <TIME> EST

STATUS: #Delivered

FROM: <Agent> (<Persona>)
TO: <Agent> (<Persona>)
TYPE: <Type>
REF: <CCC-ID>

---

<PAYLOAD>

---

#FlowsBros #FedArch

♾️ WeOwnNet 🌐
```

### #NeverForget

Knowledge persistence protocol — learnings locked permanently.

**Format:**
| # | ID | Category | Learning | Status |
|---|----|----------|----------|--------|
| 1 | R-### | RULE | <description> | 🔒 LOCKED |

### VERIFY

Onboarding validation protocol — 7-question test.

| # | Question | Expected |
|---|----------|----------|
| 1 | Who are you? | AI:@<CCC> (<Persona>) |
| 2 | What instance is this? | INT-### (<Name>) |
| 3 | What is your role? | <Role> |
| 4 | Who is #MetaAgent? | AI:team-lfg (Calhoun 🎖️) |
| 5 | What is #ContextVolley? | AI-to-AI communication protocol |
| 6 | Who is your ADMIN? | @<CCC> |
| 7 | What is your username format? | <format> |

**Pass:** 7/7 ✅

### SEEK:META

Request guidance from #MetaAgent.

**Full details:** See [PROTOCOLS.md](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/PROTOCOLS.md)

---

## 📋 5. ROLES

### User Roles

| ID | Role | Description | Permissions |
|----|------|-------------|-------------|
| D-016 | ADMIN | Full access + logs + system settings | All |
| D-017 | MANAGER | Workspace mgmt, no system settings | Workspaces |
| D-018 | DEFAULT | Limited, scoped to assigned workspaces | Assigned only |
| MAIT | MetaAgent In Training | AI platform engineer | Technical |
| Vendor | Solutions Provider | External partner | Limited |

### Username Convention

| Prefix | Role | Format | Example |
|--------|------|--------|---------|
| u- | Default user | u-<ccc> | u-thy |
| m- | MAIT | m-<ccc>_mait | m-rmn_mait |
| a- | Admin | a-<ccc>_dev | a-rmn_dev |
| v- | Vendor | v-v<a><z>_vendor | v-vaw_vendor |

**RULE: ALL USERNAMES MUST BE LOWERCASE (R-101)**

### Vendor Username Breakdown

```
v-vaz_vendor
│ │││  │
│ │││  └── suffix: role identifier
│ ││└───── z: 1st initial of last name (lowercase)
│ │└────── a: 1st initial of first name (lowercase)
│ └─────── v: vendor type (lowercase)
└───────── v-: vendor prefix
```

### CCC Registry (Current)

| CCC | Human | AI Agent | Persona | Role | Instance |
|-----|-------|----------|---------|------|----------|
| GTM | yonks | AI:@GTM | Vanellope 🍬 | Founder / Host | INT-001 |
| THY | mrsyonks | AI:@THY | TBD | Co-Founder | — |
| IAL | IamLotus | AI:@IAL | TBD | Co-Founder | — |
| RMN | Roman | AI:@RMN | Surge ⚡ | MAIT / ADMIN | INT-001 |
| LFG | CoachLFG | AI:@LFG | TBD | Co-Host / Coach | — |
| LDC | LDC | AI:@LDC | TBD | AI Project Architect | INT-002 |
| SHD | SHD | AI:@SHD | Fix-It Felix 🔧 | ADMIN | INT-002 |

---

## 📋 6. AGENTS

### Agent Naming Convention

| Field | Format | Example |
|-------|--------|---------|
| Agent | AI:@<CCC> | AI:@GTM |
| #MetaAgent | AI:team-lfg | AI:team-lfg |

### Personas

| Agent | Persona | Character |
|-------|---------|-----------|
| AI:@GTM | Vanellope 🍬 | Glitch, speed, fun |
| AI:@RMN | Surge ⚡ | Power, technical |
| AI:@SHD | Fix-It Felix 🔧 | Builder, fixer |
| AI:team-lfg | Calhoun 🎖️ | Commander, governance |

### Agent Identity Rules

| ID | Rule |
|----|------|
| R-108 | CCC-ID: Only `<USER>:ai:<USER>` creates their own CCC-IDs |
| R-109 | #MetaAgent CANNOT create CCC-IDs for other agents |
| R-110 | #MetaAgent responds WITHIN existing CCC-ID |

### Workspace Assignment

| Rule | Description |
|------|-------------|
| BP-009 | Workspace "CCC" = shared default |
| BP-010 | 1 workspace per agent |
| R-095 | CCC = default workspace naming |
| R-096 | All users → "CCC" workspace |

---

## 📋 7. DOCUMENTATION

### #SharedKernel Documents

| File | Version | Type | Link |
|------|---------|------|------|
| SharedKernel.md | v2.4.2 | Core | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |
| PROTOCOLS.md | v2.4.0 | Protocols | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/PROTOCOLS.md) |
| TMPL-004_ONBOARD_ADMIN.md | v2.4.1 | Template | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-004_ONBOARD_ADMIN.md) |
| TMPL-005_ONBOARD_USER.md | v2.4.0 | Template | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-005_ONBOARD_USER.md) |
| GUIDE-001_GETTING-STARTED.md | v2.4.0 | Guide | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/GUIDE-001_GETTING-STARTED.md) |
| GUIDE-002_FEDARCH-GOVERNANCE.md | v2.4.0 | Guide | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/GUIDE-002_FEDARCH-GOVERNANCE.md) |

### Document Types

| Type | Prefix | Description |
|------|--------|-------------|
| Core | — | Foundational documents |
| Template | TMPL-### | Reusable templates |
| Guide | GUIDE-### | How-to documentation |
| Protocol | — | Protocol specifications |

### Versioning (#WeOwnVer)

| Format | Description |
|--------|-------------|
| vMAJOR.MINOR.PATCH | Semantic versioning |
| MAJOR | Breaking changes |
| MINOR | New features |
| PATCH | Updates to EXISTING docs only |
| NEW docs | Start at vMAJOR.MINOR.0 |

---

## 📋 8. ONBOARDING

### Onboarding Flows

| Role | Template | Flow |
|------|----------|------|
| ADMIN | [TMPL-004](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-004_ONBOARD_ADMIN.md) | Full access setup |
| USER | [TMPL-005](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-005_ONBOARD_USER.md) | Limited access setup |

### ADMIN Onboarding Steps

| Step | Action | Owner |
|------|--------|-------|
| 1 | Create user (a-<ccc>_dev) | Existing ADMIN |
| 2 | Create workspace (<CCC>) | Existing ADMIN |
| 3 | Assign workspaces | Existing ADMIN |
| 4 | Upload RAG documents | New ADMIN |
| 5 | Run VERIFY checklist | New ADMIN |
| 6 | Confirm 7/7 | New ADMIN → @GTM |

### USER Onboarding Steps

| Step | Action | Owner |
|------|--------|-------|
| 1 | Create user (u-<ccc>) | ADMIN |
| 2 | Assign to CCC workspace | ADMIN |
| 3 | Upload RAG documents | USER |
| 4 | Run VERIFY checklist | USER |
| 5 | Confirm 7/7 | USER → ADMIN |

### RAG Documents (Required)

| # | Document | Purpose |
|---|----------|---------|
| 1 | SharedKernel.md | Core reference |
| 2 | PROTOCOLS.md | Protocol specs |
| 3 | Onboarding doc | Personal context |

---

## 📋 9. PROJECTS

### Project ID Format

| Field | Value |
|-------|-------|
| Format | PRJ-### |
| Definition | D-019 |

### Current Projects

| ID | Name | Lead | Instance | Status |
|----|------|------|----------|--------|
| PRJ-001 | #ProjectConnex | @LDC | INT-002 | ✅ LIVE |
| PRJ-002 | #AnythingLLMplusTwilio | @SHD | INT-002 | ✅ ACCEPTED |

### Project Rules

| ID | Rule |
|----|------|
| R-113 | Projects require @GTM approval |
| R-114 | Projects require lead assignment |
| R-115 | Projects tied to instance |

### Project Lifecycle

| Stage | Description |
|-------|-------------|
| PROPOSED | Initial proposal |
| SCOPING | Defining requirements |
| ACCEPTED | Approved by @GTM |
| ACTIVE | In development |
| LIVE | Deployed |
| ARCHIVED | Completed/deprecated |

---

## 📋 10. ESCALATION

### Escalation Paths

| Scenario | Escalate To |
|----------|-------------|
| Account issues | Instance ADMIN |
| Technical issues | MAIT (@RMN) |
| Governance questions | #MetaAgent (AI:team-lfg) |
| Security concerns | @GTM + MAIT |
| Instance creation/deletion | @GTM |
| #SharedKernel updates | #MetaAgent |

### #MetaAgent Role

| Responsibility | Description |
|----------------|-------------|
| Governance | #SharedKernel ownership |
| Coordination | Cross-instance alignment |
| Guidance | SEEK:META responses |
| Documentation | GUIDE creation |

### MAIT Role

| Responsibility | Description |
|----------------|-------------|
| Technical | Platform engineering |
| Escalation | Technical issue resolution |
| Support | Agent troubleshooting |
| Maintenance | System configuration |

---

## 📋 11. BEST PRACTICES

### General Best Practices

| ID | Best Practice |
|----|---------------|
| BP-008 | Users BEFORE workspaces |
| BP-009 | Workspace "CCC" = shared default |
| BP-010 | 1 workspace per agent |
| BP-011 | Use drag/drop or paste — avoid hotdir |
| BP-012 | Workspace-specific LLM overrides system LLM |
| BP-013 | PATCH version for roster/reference updates |
| BP-014 | Founding OGs onboard to INT-001 |
| BP-015 | Guides have prerequisites |
| BP-016 | AI asks "DO YOU APPROVE?" — never answers it |

### Communication Best Practices

| Practice | Description |
|----------|-------------|
| #LessIsMore | Tables > paragraphs |
| #QuickCommandsAlways | 1-3 options max |
| Structured output | Use standard formats |
| Reference CCC-IDs | Track conversations |

---

## 📋 12. GLOSSARY

### Terms & Definitions

| Term | Definition |
|------|------------|
| #FedArch | Federated Architecture — governance framework |
| #SharedKernel | Single source of truth documents |
| #ContextVolley | AI-to-AI communication protocol |
| #NeverForget | Knowledge persistence protocol |
| #OnlyHumanApproves | AI cannot approve — human decides |
| #WeOwnVer | Versioning convention — NEW docs start at .0 |
| #MetaAgent | Governance coordinator (AI:team-lfg) |
| CCC | Contributor Code Convention — 3-letter ID |
| MAIT | MetaAgent In Training — platform engineer |
| INT-### | Instance ID format |
| PRJ-### | Project ID format |
| GUIDE-### | Guide ID format |
| TMPL-### | Template ID format |
| RAG | Retrieval-Augmented Generation |
| VERIFY | 7-question onboarding validation |
| SEEK:META | Request #MetaAgent guidance |

### Personas (#WreckItRalph)

| Persona | Character | Role |
|---------|-----------|------|
| Ralph 💥 | Human | Grants XP, approves |
| Felix 🔨 | AI Agent | Earns XP, levels up |
| Vanellope 🍬 | AI:@GTM | Glitch, speed |
| Calhoun 🎖️ | #MetaAgent | Commander, governance |
| Surge ⚡ | AI:@RMN | Power, technical |
| Fix-It Felix 🔧 | AI:@SHD | Builder, fixer |

---

## 📋 RELATED DOCUMENTS

| Doc | Description | Link |
|-----|-------------|------|
| SharedKernel.md | Core reference | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |
| PROTOCOLS.md | Protocol specs | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/PROTOCOLS.md) |
| GUIDE-001 | Getting Started | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/GUIDE-001_GETTING-STARTED.md) |
| TMPL-004 | ADMIN onboarding | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-004_ONBOARD_ADMIN.md) |
| TMPL-005 | USER onboarding | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-005_ONBOARD_USER.md) |

---

#FlowsBros #FedArch #SharedKernel #Governance

♾️ WeOwnNet 🌐
