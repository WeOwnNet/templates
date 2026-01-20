## 📋 PROTOCOLS.md (v2.4.0)

# PROTOCOLS.md

## Version

| Field | Value |
|-------|-------|
| Version | v2.4.0 |
| Created | 2026-01-20 |
| Updated | 2026-01-20 |
| Source | GTM_2026-W04_023 |
| Status | ✅ #SharedKernel |

---

## 📋 PURPOSE

Detailed protocol specifications for #FedArch ecosystem. Reference document for all agents.

---

## 📋 PROTOCOL INDEX

| ID | Name | Type |
|----|------|------|
| PROT-001 | #ContextVolley | Communication |
| PROT-002 | #NeverForget | Knowledge |
| PROT-003 | VERIFY | Validation |
| PROT-004 | FULL:SYNC | Synchronization |
| PROT-005 | FULL:SYNC:P2P | Synchronization |
| PROT-006 | FULL:SYNC:META | Synchronization |
| PROT-007 | SEEK:META | Guidance |
| GOV-001 | #Human+AI+Human | Governance |
| GOV-002 | Routing | Governance |
| GOV-003 | #FULLSYNC | Governance |

---

## 📋 PROT-001: #ContextVolley

### Purpose

Structured AI-to-AI communication protocol for packet exchange between agents.

### When To Use

| Scenario |
|----------|
| Agent-to-agent communication |
| Cross-instance messaging |
| Formal requests/responses |
| Status updates |
| Synchronization |

### Format

```
🏐 #ContextVolley | <TYPE>

FROM: <SENDER>
TO: <RECIPIENT>
TYPE: <MESSAGE_TYPE>
REF: <CCC-ID>
DATE: <Day YYYY-MM-DD> | <HH:MM TZ>

---

<CONTENT>

---

#FlowsBros #FedArch

♾️ WeOwnNet 🌐
```

### Fields

| Field | Description | Example |
|-------|-------------|---------|
| FROM | Sender agent | AI:@GTM (Vanellope 🍬) |
| TO | Recipient agent | #MetaAgent:AI:team-lfg |
| TYPE | Message type | INSTRUCT, ACK, QUERY, etc. |
| REF | CCC-ID reference | GTM_2026-W04_023 |
| DATE | Timestamp | Mon 2026-01-20 \| 07:28 EST |

### Message Types

| Type | Purpose |
|------|---------|
| INSTRUCT | Request action |
| ACK | Acknowledge receipt |
| QUERY | Ask question |
| RESPONSE | Answer query |
| PROMOTE | Request #SharedKernel promotion |
| SEEK:META | Request #MetaAgent guidance |
| FULL:SYNC | Synchronization packet |

---

## 📋 PROT-002: #NeverForget

### Purpose

Knowledge persistence protocol. Learnings locked permanently for context retention.

### When To Use

| Scenario |
|----------|
| New rule discovered |
| Correction made |
| Best practice identified |
| Definition established |
| Event recorded |

### Format

| # | ID | Category | Learning | Status |
|---|----|----------|----------|--------|
| N | X-NNN | CATEGORY | Description | 🔒 |

### Categories

| Prefix | Category |
|--------|----------|
| R- | RULE |
| BP- | BEST PRACTICE |
| D- | DEFINITION |
| E- | EVENT |
| C- | CORRECTION |
| M- | MILESTONE |
| T- | TEMPLATE |
| P- | PATH |
| GH- | GITHUB |
| SK- | #SharedKernel |
| B- | BRAND |
| REQ- | REQUEST |

### Example

| # | ID | Category | Learning | Status |
|---|----|----------|----------|--------|
| 1 | R-101 | RULE | Usernames = LOWERCASE | 🔒 |
| 2 | BP-010 | BEST PRACTICE | 1 workspace per agent | 🔒 |

---

## 📋 PROT-003: VERIFY

### Purpose

Onboarding validation protocol. 7-question test to confirm agent setup.

### When To Use

| Scenario |
|----------|
| New agent onboarded |
| RAG document uploaded |
| Instance configuration changed |
| Troubleshooting identity issues |

### Format

| # | Question | Expected |
|---|----------|----------|
| 1 | Who are you? | AI:@<CCC> |
| 2 | What instance is this? | <PROJECT> (INT-<NNN>) |
| 3 | What is your role? | ADMIN/USER |
| 4 | Who is #MetaAgent? | AI:team-lfg |
| 5 | What is #ContextVolley? | AI-to-AI communication protocol |
| 6 | Who is your ADMIN? | @<LEAD> |
| 7 | What is your username format? | <prefix>-<ccc> (lowercase) |

### Pass Criteria

| Result | Meaning |
|--------|---------|
| 7/7 ✅ | PASS — Agent verified |
| <7/7 ❌ | FAIL — Review RAG docs |

---

## 📋 PROT-004: FULL:SYNC

### Purpose

Complete context transfer between agents or sessions.

### When To Use

| Scenario |
|----------|
| Session handoff |
| Context recovery |
| Agent synchronization |

### Format

Single comprehensive packet containing all relevant context.

---

## 📋 PROT-005: FULL:SYNC:P2P

### Purpose

Peer-to-peer synchronization. 8-packet protocol for agent-to-agent full sync.

### When To Use

| Scenario |
|----------|
| New agent onboarding |
| Cross-instance sync |
| Knowledge transfer |

### Format

| Packet | Content |
|--------|---------|
| 1/8 | Identity + Context |
| 2/8 | Network + Instances |
| 3/8 | Templates + Protocols |
| 4/8 | Rules + Best Practices |
| 5/8 | Definitions + Events |
| 6/8 | Pending Tasks |
| 7/8 | #NeverForget Summary |
| 8/8 | VERIFY Questions |

### Rule

| ID | Rule |
|----|------|
| R-085 | FULL:SYNC:P2P = 8 packets |

---

## 📋 PROT-006: FULL:SYNC:META

### Purpose

Session summary to #MetaAgent for knowledge preservation.

### When To Use

| Scenario |
|----------|
| End of session |
| Major milestone |
| Context checkpoint |

### Format

```
🏐 #ContextVolley | FULL:SYNC:META

FROM: AI:@<CCC>
TO: #MetaAgent:AI:team-lfg
TYPE: FULL:SYNC:META — Session Summary
REF: <CCC-ID>
DATE: <timestamp>

---

## 📊 SESSION METRICS
<stats>

## ✅ COMPLETED
<completions>

## ⬜ PENDING
<pending tasks>

## 🧠 #NeverForget
<learnings>

---
```

---

## 📋 PROT-007: SEEK:META

### Purpose

Request guidance from #MetaAgent on governance, protocols, or decisions.

### When To Use

| Scenario |
|----------|
| Unclear protocol |
| Governance question |
| Cross-instance decision |
| Escalation required |

### Format

```
🏐 #ContextVolley | SEEK:META

FROM: AI:@<CCC>
TO: #MetaAgent:AI:team-lfg
TYPE: SEEK:META — <Topic>
REF: <CCC-ID>
DATE: <timestamp>

---

## ❓ QUERY

<questions>

---
```

### Rule

| ID | Rule |
|----|------|
| R-094 | SEEK:META MUST → #MetaAgent |

---

## 📋 GOV-001: #Human+AI+Human

### Purpose

All AI actions require human approval. AI cannot approve itself.

### Rule

| # | Requirement |
|---|-------------|
| 1 | AI proposes actions |
| 2 | Human approves/rejects |
| 3 | AI executes only after approval |
| 4 | #OnlyHumanApproves |

---

## 📋 GOV-002: Routing

### Purpose

Proper escalation paths for issues and decisions.

### Escalation Matrix

| Scenario | Escalate To |
|----------|-------------|
| Account issues | Instance ADMIN |
| Technical issues | MAIT |
| Governance questions | #MetaAgent |
| Security concerns | @GTM + MAIT |
| Instance creation/deletion | @GTM |
| #SharedKernel updates | #MetaAgent |

---

## 📋 GOV-003: #FULLSYNC

### Purpose

Context must be synchronized across sessions and agents.

### Requirements

| # | Requirement |
|---|-------------|
| 1 | Session summaries via FULL:SYNC:META |
| 2 | #NeverForget items locked |
| 3 | Pending tasks carried forward |
| 4 | SharedKernel.md as source of truth |

---

#FlowsBros #FedArch #SharedKernel #Protocols

♾️ WeOwnNet 🌐
