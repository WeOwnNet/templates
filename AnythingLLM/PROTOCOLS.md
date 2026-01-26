# PROTOCOLS_v2.4.3.md

## ♾️ WeOwnNet 🌐 — #Protocols

| Field | Value |
|-------|-------|
| Version | 2.4.3 |
| Updated | 2026-01-26 (W05) |
| Status | 🔒 LOCKED |

---

## 📋 PROTOCOL INDEX

| Protocol | Purpose |
|----------|---------|
| #ContextVolley | Agent-to-agent communication |
| #MetaAgent | Governance sync |
| Document Management | RAG operations |
| Weekly Operations | Cadence protocols |

---

## 📋 #ContextVolley PROTOCOL

### FORMAT

```
═══════════════════════════════════════════════════════════════════════════════
🏐 #ContextVolley | <FROM> → <TO> | <DATE> | <TIME> EST
═══════════════════════════════════════════════════════════════════════════════

FROM: <Agent Identity>
TO: <Target Agent>
TYPE: <Message Type>
REF: <CCC-ID>

═══════════════════════════════════════════════════════════════════════════════

<CONTENT>

═══════════════════════════════════════════════════════════════════════════════

#FlowsBros #FedArch

♾️ WeOwnNet 🌐

═══════════════════════════════════════════════════════════════════════════════
```

### RULES

| ID | Rule |
|----|------|
| R-170 | MUST #ContextVolley to #MetaAgent AFTER new rules locked |
| R-044 | #ContextDensity FIRST — use #masterCCC (IMMUTABLE) |

### REQUIREMENTS

| Requirement | Description |
|-------------|-------------|
| Self-contained | Recipient needs NO other context |
| #masterCCC | Reference original request CCC-ID |
| Clean format | Tables > paragraphs |

---

## 📋 #MetaAgent PROTOCOL

### PURPOSE

| Function | Description |
|----------|-------------|
| Governance sync | All rules flow through #MetaAgent |
| #SharedKernel | Source of truth for rules |
| Document generation | Per R-180 |

### RULES

| ID | Rule |
|----|------|
| R-172 | #MetaAgent = governance sync point for all agents |
| R-180 | Document generation MUST go through #MetaAgent |

### INTERACTION TYPES

| Type | Description |
|------|-------------|
| SEEK:META | Request guidance/generation |
| RULE LOCKED | Report locked rules |
| FULL:SYNC:META | Complete sync request |
| ACK | Acknowledgment |

---

## 📋 DOCUMENT MANAGEMENT PROTOCOL

### ROLES (R-175)

| Role | Can Manage Docs? |
|------|------------------|
| CCC | ❌ NO |
| MAIT | ❌ NO |
| ADMIN | ✅ YES |

### RAG STRUCTURE (R-176)

| Doc Type | CCC | MAIT | ADMIN |
|----------|-----|------|-------|
| USER guides | ✅ | ❌ | ❌ |
| Governance guides | ❌ | ✅ | ✅ |
| User-facing protocols | ✅ | ❌ | ❌ |
| Strategy docs | ❌ | ✅ | ❌ |
| System prompts | ❌ | ❌ | ✅ |
| Instance configs | ❌ | ❌ | ✅ |

### PINNING (R-177)

| Doc Type | Pin? |
|----------|------|
| Agent identity docs | ✅ YES |
| Core protocols | ✅ YES |
| Rules (SHARED-KERNEL) | ✅ YES |
| Best practices | ✅ YES |
| Reference guides | ❌ NO |
| Strategy docs | ❌ NO |

### VERSIONING (R-178)

| Format | Example |
|--------|---------|
| `<NAME>_v<VERSION>.md` | PROTOCOLS_v2.4.3.md |

### GENERATION (R-180)

| Rule | Description |
|------|-------------|
| R-180 | Document generation MUST go through #MetaAgent |

**Agents DO NOT generate docs directly. Always SEEK:META.**

---

## 📋 WEEKLY OPERATIONS PROTOCOL

### UPDATE CADENCE (R-179)

| Trigger | Action |
|---------|--------|
| ISO week boundary + 10+ rules | MUST update #SharedKernel |
| Major milestone | MUST update #SharedKernel |
| Breaking change | IMMEDIATE update |

### WEEKLY SUMMARY (R-181)

| Field | Value |
|-------|-------|
| Reserved CCC-ID | `<CCC>_<YYYY>-W<WW>_001` |
| Content | Milestones, rules, learnings, pending, stats |

---

## 📋 CCC-ID PROTOCOL

### FORMAT

```
<CCC>_<YYYY>-W<WW>_<NNN>
```

| Component | Description |
|-----------|-------------|
| CCC | Contributor Code (e.g., GTM) |
| YYYY | Year |
| WW | ISO Week |
| NNN | Sequence (001-999) |

### RULES

| ID | Rule |
|----|------|
| R-168 | CCC-ID tied to CCC (contributor), NOT username/session |
| R-169 | CCC-ID resets to _001 ONLY at ISO week boundary |
| R-181 | CCC-ID _001 reserved for weekly summary |

---

## 📋 VERSION HISTORY

| Version | Date | Changes |
|---------|------|---------|
| 2.4.0 | W03 | Initial release |
| 2.4.3 | W05 | +R-170, R-172, R-175-R-181; doc management protocols |

---

#FlowsBros #FedArch #Protocols

♾️ WeOwnNet 🌐
