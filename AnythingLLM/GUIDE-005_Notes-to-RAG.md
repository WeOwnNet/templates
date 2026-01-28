# GUIDE-005: Notes-to-RAG Workflow

## 📋 GUIDE-005_Notes-to-RAG_v2.4.0.md
## ♾️ WeOwnNet 🌐 — Session Notes to RAG Upload

| Field | Value |
|-------|-------|
| Document | GUIDE-005_Notes-to-RAG.md |
| Version | 2.4.0 |
| CCC-ID | GTM_2026-W05_391 |
| Created | 2026-01-28 (W05) |
| Status | 🔒 LOCKED |
| Audience | All Contributors |
| Tags | #AnythingLLM #RAG #YonksPromptingAcademy |

---

## 📖 Table of Contents

1. [Overview](#-1-overview)
2. [When to Use This Guide](#-2-when-to-use-this-guide)
3. [Pre-Session Setup](#-3-pre-session-setup)
4. [During Session (Capture)](#-4-during-session-capture)
5. [Post-Session (Export)](#-5-post-session-export)
6. [Sanitization Checklist](#-6-sanitization-checklist)
7. [RAG Upload Steps](#-7-rag-upload-steps)
8. [Verification Test](#-8-verification-test)
9. [Troubleshooting](#-9-troubleshooting)
10. [Related Documents](#-10-related-documents)
11. [Version History](#-11-version-history)

---

## 📋 1. Overview

### Purpose

This guide provides the standard workflow for capturing session notes and uploading them to RAG.

### Key Principle

| Principle | Description |
|-----------|-------------|
| R-199 | Session/meeting/webinar notes = RAG ONLY (not GitHub) |
| Sanitize First | Remove tokens and sensitive data before upload |
| Verify Always | Cross-agent verification required |

### Applies To

| Session Type | Example |
|--------------|---------|
| Webinars | FinStack, industry events |
| Meetings | Team calls, client meetings |
| Workshops | Training sessions |
| Conferences | Live event notes |

---

## 📋 2. When to Use This Guide

| Scenario | Use This Guide? |
|----------|-----------------|
| Live webinar notes | ✅ YES |
| Team meeting notes | ✅ YES |
| Client call summary | ✅ YES |
| Governance documents | ❌ NO (use SharedKernel process) |
| Reusable guides | ❌ NO (use GUIDE template) |

---

## 📋 3. Pre-Session Setup

| # | Step | Action |
|---|------|--------|
| 1 | Create #masterCCC | `<CCC>_<YYYY>-W<WW>_<NNN>` |
| 2 | Open notes template | Use TEMPLATE_NOTES.md |
| 3 | Fill metadata | Event, date, attendees |
| 4 | Prepare capture format | Speaker + timestamp columns |

### Metadata Template

| Field | Value |
|-------|-------|
| Event | [Event Name] |
| Type | Webinar / Meeting / Workshop |
| Date | YYYY-MM-DD |
| #masterCCC | <CCC>_<YYYY>-W<WW>_<NNN> |
| Storage | RAG ONLY (R-199) |

---

## 📋 4. During Session (Capture)

| # | Action | Format |
|---|--------|--------|
| 1 | Log speaker changes | `## [Speaker Name]` |
| 2 | Timestamp key points | `[HH:MM]` prefix |
| 3 | Use CCC-IDs | Track significant items |
| 4 | Mark insights | 🔥 for #NeverForget items |

### Capture Format

```markdown
## [Speaker Name] — [Company/Role]

| Time | Note |
|------|------|
| 14:05 | Key point 1 |
| 14:12 | Key point 2 |
| 14:18 | 🔥 Critical insight |
```

---

## 📋 5. Post-Session (Export)

| # | Step | Action |
|---|------|--------|
| 1 | Request full export | Ask AI for complete notes |
| 2 | Review for completeness | Check all speakers covered |
| 3 | Add action items | Extract follow-ups |
| 4 | Proceed to sanitization | BEFORE upload |

---

## 📋 6. Sanitization Checklist

| Item | Check | Action if Found |
|------|-------|-----------------|
| Event tokens | `?tk=` in URLs | Remove parameter |
| Personal emails | `@domain.com` | Redact or remove |
| Phone numbers | `+1-XXX-XXX-XXXX` | Redact |
| API keys | `sk-`, `pk_` | NEVER include |
| Internal URLs | `/admin/`, `/internal/` | Evaluate necessity |
| Passwords | Any credentials | NEVER include |
| Private IPs | `192.168.x.x`, `10.x.x.x` | Remove |

### Pre-Upload Verification

| Item | Status |
|------|--------|
| Event tokens removed | ⬜ |
| Personal info redacted | ⬜ |
| URLs sanitized | ⬜ |
| API keys checked | ⬜ |
| Ready for upload | ⬜ |

---

## 📋 7. RAG Upload Steps

| # | Step | Command/Action | Expected |
|---|------|----------------|----------|
| 1 | Pre-check | `list:docs` | Baseline count |
| 2 | Upload | UI → Documents → Upload | File added |
| 3 | Embed | Move to Workspace → Save and Embed | Processing |
| 4 | Verify | `status:RAG` | 🟢 HEALTHY |
| 5 | Confirm | `list:docs` | Count +1 |
| 6 | Test Query | Ask about content | ✅ Retrieved |

### Workspace Assignment

| Workspace | Upload? | Rationale |
|-----------|---------|-----------|
| CCC | ✅ YES | User reference |
| tools | ✅ YES | Admin/SME reference |
| ADMIN | ❌ NO | Not admin-specific |

---

## 📋 8. Verification Test

### Requirements

| Requirement | Description |
|-------------|-------------|
| Fresh session | New thread/session REQUIRED |
| Cross-agent | Different user recommended |
| Content query | Ask specific question about notes |

### Verification Steps

| # | Step | Actor | Action |
|---|------|-------|--------|
| 1 | Upload complete | Uploader | Confirm embed |
| 2 | Start fresh session | Verifier | New thread |
| 3 | Run `list:docs` | Verifier | Confirm presence |
| 4 | Query content | Verifier | Ask about notes |
| 5 | Confirm match | Verifier | Content accurate |

### Verification Commands

| Command | Purpose |
|---------|---------|
| `list:docs` | Show all RAG documents |
| `status:RAG` | Check RAG health |
| `[query about content]` | Test retrieval |

---

## 📋 9. Troubleshooting

| Issue | Symptom | Resolution |
|-------|---------|------------|
| Doc not found in query | RAG returns no context | Verify embed complete; fresh session |
| Stale context | Old version returned | Re-embed; `status:RAG` |
| Cross-workspace mismatch | CCC has, tools doesn't | Sync to both workspaces |
| Token leak | Sensitive URL in RAG | Remove doc, sanitize, re-upload |
| Embed stuck | Processing indefinitely | Cancel, re-upload |
| Wrong workspace | Doc in wrong location | Move to correct workspace |

### Escalation

| Issue | Escalate To |
|-------|-------------|
| Persistent RAG issues | @RMN |
| Security concern (token leak) | @GTM + @RMN |
| Cross-agent verification failure | ADMIN workspace |

---

## 📋 10. Related Documents

| Document | Version | URL |
|----------|---------|-----|
| CASE-STUDY-001_Notes-to-RAG-Workflow | v2.4.0 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/case-studies/CASE-STUDY-001_Notes-to-RAG-Workflow_v2.4.0.md) |
| TEMPLATE_NOTES | v2.4.0 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TEMPLATE_NOTES_v2.4.0.md) |
| SharedKernel | v2.4.8 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |
| CASE-STUDY_AnythingLLM-RAG-Verification | v2.4.0 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/case-studies/CASE-STUDY_AnythingLLM-RAG-Verification_v2.4.0.md) |

---

## 📋 11. Version History

| Version | Date | Ref | Changes |
|---------|------|-----|---------|
| 2.4.0 | 2026-W05 | GTM_2026-W05_391 | Initial release |

---

#FlowsBros #FedArch #AnythingLLM #YonksPromptingAcademy

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
