# BEST-PRACTICES_v2.4.2.md

## ♾️ WeOwnNet 🌐 — #BestPractices

| Field | Value |
|-------|-------|
| Version | 2.4.2 |
| Updated | 2026-01-26 (W05) |
| Instance | INT-002 (#ProjectConnex) |
| Status | 🔒 LOCKED |

---

## 📋 BEST PRACTICES INDEX

| Range | Category | Count |
|-------|----------|-------|
| BP-001 → BP-016 | W01-W04 (LEGACY) | ~16 |
| BP-017 → BP-019 | W04-W05 | 3 |
| **TOTAL** | | **~19** |

---

## 📋 CORE BEST PRACTICES (IMMUTABLE)

| ID | Best Practice | Status |
|----|---------------|--------|
| BP-019 | ALWAYS SEEK:META for ALL documents | 🔒 IMMUTABLE |

---

## 📋 WORKSPACE CONFIGURATION

### BP-017: Workspace Prompt Per Workspace

| Workspace | Prompt Focus |
|-----------|--------------|
| CCC | User interaction, CCC-ID generation |
| MAIT | Strategy, SME, meta-cognition |
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

| Doc Type | CCC | MAIT | ADMIN |
|----------|-----|------|-------|
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

## 📋 VERSION HISTORY

| Version | Date | Changes |
|---------|------|---------|
| 2.4.0 | W03 | Initial release |
| 2.4.2 | W05 | +BP-017, BP-018, BP-019; pinning/versioning/cadence guidance |

---

#FlowsBros #FedArch #BestPractices

♾️ WeOwnNet 🌐
