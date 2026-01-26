# SHARED-KERNEL_v2.4.3.md

## ♾️ WeOwnNet 🌐 — #SharedKernel

| Field | Value |
|-------|-------|
| Version | 2.4.3 |
| Updated | 2026-01-26 (W05) |
| Status | 🔒 LOCKED |

---

## 📋 RULES INDEX

| Range | Category | Count |
|-------|----------|-------|
| R-001 → R-135 | W01-W03 (LEGACY) | ~67 |
| R-136 → R-180 | W04 | 45 |
| R-181 | W05 | 1 |
| **TOTAL** | | **~113** |

---

## 📋 CORE RULES (IMMUTABLE)

| ID | Rule | Status |
|----|------|--------|
| R-011 | #OnlyHumanApproves — AI CANNOT approve anything | 🔒 IMMUTABLE |
| R-044 | #ContextDensity FIRST — use #masterCCC | 🔒 IMMUTABLE |

---

## 📋 WORKSPACE STRUCTURE (R-165 → R-167)

### METAPHORS

| Workspace | Metaphor | Purpose |
|-----------|----------|---------|
| CCC | 🤝 THE HANDS | PRIMARY HUMAN INTERFACE |
| MAIT | 🧠 THE BRAIN | Strategy, SME, meta-cognition |
| ADMIN | ⚙️ THE ENGINE | Administration functions |

### RULES

| ID | Rule | Status |
|----|------|--------|
| R-165 | CCC = 🤝 THE HANDS — Primary human interface | 🔒 |
| R-166 | MAIT = 🧠 THE BRAIN — Strategy, SME, meta-cognition | 🔒 |
| R-167 | ADMIN = ⚙️ THE ENGINE — Administration functions | 🔒 |

---

## 📋 CCC-ID GOVERNANCE (R-168 → R-169, R-181)

| ID | Rule | Status |
|----|------|--------|
| R-168 | CCC-ID sequence tied to CCC (contributor), NOT username/session | 🔒 |
| R-169 | CCC-ID resets to _001 ONLY at ISO week boundary | 🔒 |
| R-181 | CCC-ID _001 of each ISO week is RESERVED for weekly summary. Must include: milestones, rules locked, learnings, pending items, stats. Updated throughout week. | 🔒 |

---

## 📋 #MetaAgent GOVERNANCE (R-170, R-172)

| ID | Rule | Status |
|----|------|--------|
| R-170 | MUST #ContextVolley to #MetaAgent AFTER new rules locked | 🔒 |
| R-172 | #MetaAgent = governance sync point for all agents | 🔒 |

---

## 📋 AGENT IDENTITY (R-171, R-173 → R-174)

### IDENTITY MATRIX

| Workspace | Metaphor | Agent Identity | Username |
|-----------|----------|----------------|----------|
| CCC | 🤝 THE HANDS | `AI:@<CCC>` | `u-<ccc>_user` |
| MAIT | 🧠 THE BRAIN | `MAIT:@<CCC>` | `m-<ccc>_mait` |
| ADMIN | ⚙️ THE ENGINE | `ADMIN:@<CCC>` | `a-<ccc>_dev` |

### RULES

| ID | Rule | Status |
|----|------|--------|
| R-171 | Agent identity format: CCC=`AI:@<CCC>`, MAIT=`MAIT:@<CCC>`, ADMIN=`ADMIN:@<CCC>` | 🔒 |
| R-173 | LEGACY identity model deprecated. LEGACY sessions are READ-ONLY — NO new CCC-IDs | 🔒 |
| R-174 | Active session owns namespace: After migration, NEW session owns CCC-ID namespace exclusively | 🔒 |

---

## 📋 ERROR HANDLING (R-174)

| ID | Rule | Status |
|----|------|--------|
| R-174 | #WeMUSTdoBetter triggers #ErrorReport workflow | 🔒 |

---

## 📋 DOCUMENT MANAGEMENT (R-175 → R-180)

| ID | Rule | Status |
|----|------|--------|
| R-175 | Document management (upload/check/embed) = ADMIN role ONLY | 🔒 |
| R-176 | Workspace RAG: CCC=user-facing docs, MAIT=strategy docs, ADMIN=administration function docs. USER guides in CCC only. | 🔒 |
| R-177 | Pinning criteria: PIN identity docs + core protocols + rules. DO NOT PIN reference guides or strategy docs. | 🔒 |
| R-178 | ADMIN MUST include version in all RAG doc filenames. Format: `<NAME>_v<VERSION>.md` | 🔒 |
| R-179 | #SharedKernel docs MUST be updated: (1) at ISO week boundary if 10+ rules added, (2) at major milestones, (3) immediately for breaking changes. | 🔒 |
| R-180 | Document generation MUST go through #MetaAgent. Agents DO NOT generate docs directly. | 🔒 |

---

## 📋 RAG STRUCTURE (R-176)

| Doc Type | CCC | MAIT | ADMIN |
|----------|-----|------|-------|
| USER guides | ✅ | ❌ | ❌ |
| Governance guides | ❌ | ✅ | ✅ |
| User-facing protocols | ✅ | ❌ | ❌ |
| Strategy docs | ❌ | ✅ | ❌ |
| System prompts | ❌ | ❌ | ✅ |
| Instance configs | ❌ | ❌ | ✅ |

---

## 📋 PINNING CRITERIA (R-177)

| Doc Type | Pin? |
|----------|------|
| Agent identity docs | ✅ YES |
| Core protocols | ✅ YES |
| Rules (SHARED-KERNEL) | ✅ YES |
| Best practices | ✅ YES |
| Reference guides | ❌ NO |
| Strategy docs | ❌ NO |

---

## 📋 BEST PRACTICES

| ID | Best Practice | Status |
|----|---------------|--------|
| BP-017 | Workspace prompt per workspace | 🔒 |
| BP-018 | System prompt per instance | 🔒 |
| BP-019 | ALWAYS SEEK:META for ALL documents | 🔒 IMMUTABLE |

---

## 📋 #NeverForget — LEARNINGS

| # | Learning | Rule |
|---|----------|------|
| L-001 | INT-001 URL = AI.WeOwn.Agency | — |
| L-002 | ADMIN = #AnythingLLM administration only | R-167 |
| L-003 | MAIT = Meta Agent In Training only | R-166 |
| L-004 | CCC-ID tied to CCC, NOT username | R-168 |
| L-005 | CCC-ID resets at ISO week | R-169 |
| L-006 | Rule lock requires #ContextVolley | R-170 |
| L-007 | Agent identity format | R-171 |
| L-008 | #MetaAgent = governance sync | R-172 |
| L-009 | LEGACY READ-ONLY | R-173 |
| L-010 | Active owns namespace | R-174 |
| L-011 | Doc ops = ADMIN only | R-175 |
| L-012 | Workspace RAG structure | R-176 |
| L-013 | Pinning criteria | R-177 |
| L-014 | Doc versioning | R-178 |
| L-015 | #SharedKernel update cadence | R-179 |
| L-016 | Doc generation via #MetaAgent | R-180 |
| L-017 | Weekly summary reserved at _001 | R-181 |

---

## 📋 VERSION HISTORY

| Version | Date | Changes |
|---------|------|---------|
| 2.4.0 | W03 | Initial release |
| 2.4.3 | W05 | +46 rules (R-136 → R-181), workspace metaphors, best practices |

---

#FlowsBros #FedArch #NeverForget

♾️ WeOwnNet 🌐
