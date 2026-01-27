# CASE-STUDY: #AnythingLLM RAG Verification

## 📋 CASE-STUDY_AnythingLLM-RAG-Verification_v2.4.0.md
## ♾️ WeOwnNet 🌐 — #YonksPromptingAcademy

| Field | Value |
|-------|-------|
| Document | CASE-STUDY_AnythingLLM-RAG-Verification.md |
| Version | 2.4.0 |
| CCC-ID | GTM_2026-W05_253 |
| Created | 2026-01-27 (W05) |
| Status | 🔒 LOCKED |
| Audience | Admins / Stewards |
| Source of Truth | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/case-studies/CASE-STUDY_AnythingLLM-RAG-Verification_v2.4.0.md) |

---

## 📖 Table of Contents

1. [Overview](#-1-overview)
2. [Problem](#-2-problem)
3. [Solution](#-3-solution)
4. [RAG Update Checklist](#-4-rag-update-checklist)
5. [Verification Steps](#-5-verification-steps)
6. [Best Practices](#-6-best-practices)
7. [Troubleshooting](#-7-troubleshooting)
8. [Version History](#-version-history)

---

## 📋 1. Overview

### What This Covers

| Field | Value |
|-------|-------|
| Topic | RAG document management in #AnythingLLM |
| Scenario | Updating RAG after publishing new doc versions to GitHub |
| Instance | INT-001 (AI.WeOwn.Agency) |
| Workspace | tools (🧠 THE BRAIN) |

### When to Use

| Trigger | Action |
|---------|--------|
| New doc version published to GitHub | Follow RAG Update Checklist |
| Stale docs detected in workspace | Remove old → Upload new |
| RAG audit shows outdated content | Execute full refresh |

---

## 📋 2. Problem

### Scenario

| Field | Value |
|-------|-------|
| Issue | Stale docs in RAG after GitHub publish |
| Impact | AI responses based on outdated information |
| Root Cause | RAG not automatically synced with GitHub |

### Symptoms

| # | Symptom |
|---|---------|
| 1 | AI references old version numbers |
| 2 | AI missing new rules/BPs |
| 3 | AI contradicts current TRUTH (GitHub) |
| 4 | Version mismatch between RAG and GitHub |

### Example

| Location | Version | Status |
|----------|---------|--------|
| GitHub (TRUTH) | v2.4.7 | ✅ Current |
| RAG (workspace:tools) | v2.4.5 | ❌ Stale |

---

## 📋 3. Solution

### Key Principle

| Principle | Description |
|-----------|-------------|
| TRUTH = GitHub | GitHub is the Source of Truth |
| RAG = Copy | RAG contains copies of TRUTH |
| Manual Sync | Human must sync RAG with GitHub |

### Solution Overview

| Step | Action |
|------|--------|
| 1 | Download new version(s) from GitHub |
| 2 | Access workspace RAG settings |
| 3 | Remove stale doc(s) |
| 4 | Upload new doc(s) |
| 5 | Verify indexing complete |

---

## 📋 4. RAG Update Checklist

### Pre-Update

| # | Step | Status |
|---|------|--------|
| 1 | Identify docs to update | ⬜ |
| 2 | Confirm new versions on GitHub (TRUTH) | ⬜ |
| 3 | Note current RAG versions | ⬜ |

### Download Phase

| # | Step | Description | Status |
|---|------|-------------|--------|
| 1 | Navigate to GitHub | Source of Truth |⬜ |
| 2 | Download new version | Click Raw → Save As | ⬜ |
| 3 | Repeat for each doc | All docs needing update | ⬜ |

### RAG Update Phase

| # | Step | Description | Status |
|---|------|-------------|--------|
| 4 | Access RAG settings | Workspace → Settings → Documents | ⬜ |
| 5 | Remove stale doc | Click X on old version | ⬜ |
| 6 | Repeat for each | All stale docs | ⬜ |
| 7 | Upload new doc | Drag/drop or Browse | ⬜ |
| 8 | Repeat for each | All new docs | ⬜ |

### Verification Phase

| # | Step | Description | Status |
|---|------|-------------|--------|
| 9 | Wait for indexing | Progress indicator | ⬜ |
| 10 | Verify indexing complete | See Section 5 | ⬜ |
| 11 | Test with query | Ask about new content | ⬜ |

---

## 📋 5. Verification Steps

### How to Verify RAG Indexing Complete

| # | Method | Description |
|---|--------|-------------|
| 1 | Visual indicator | Check for "Indexed" status in document list |
| 2 | Query test | Ask AI about content from new doc |
| 3 | Version check | Ask AI "What version is SharedKernel?" |

### Verification Query Examples

| Query | Expected Response |
|-------|-------------------|
| "What version is SharedKernel?" | "v2.4.7" (or current) |
| "What is R-197?" | Correct rule text |
| "What is D-038?" | MAIT ShortCode definition |

### Indexing Status Indicators

| Status | Meaning |
|--------|---------|
| ⏳ Processing | Indexing in progress |
| ✅ Indexed | Ready for queries |
| ❌ Failed | Error — retry upload |

### Wait Times

| Doc Size | Approximate Wait |
|----------|------------------|
| Small (<10KB) | 5-15 seconds |
| Medium (10-50KB) | 15-30 seconds |
| Large (>50KB) | 30-60 seconds |

---

## 📋 6. Best Practices

### Naming Convention

| Practice | Example |
|----------|---------|
| Include version in filename | SharedKernel_v2.4.7.md |
| Use consistent naming | BEST-PRACTICES_v2.4.5.md |

### Update Cadence

| Trigger | Action |
|---------|--------|
| After GitHub publish | Update RAG same session |
| ISO week boundary | Audit RAG versions |
| Major milestone | Full RAG refresh |

### Documentation

| Practice | Description |
|----------|-------------|
| Log updates | Note CCC-ID for RAG updates |
| Track versions | Maintain version registry |
| Audit regularly | Weekly RAG health check |

### TRUTH Hierarchy

| Priority | Source | Purpose |
|----------|--------|---------|
| 1 | GitHub | Source of Truth |
| 2 | RAG | Working copy for AI |
| 3 | Session context | Temporary override |

---

## 📋 7. Troubleshooting

### Common Issues

| Issue | Cause | Solution |
|-------|-------|----------|
| Doc not appearing | Upload failed | Re-upload |
| Indexing stuck | Large file / system load | Wait or retry |
| AI still uses old version | Cache / context | New thread |
| Version mismatch | Incomplete update | Verify all docs updated |

### Recovery Steps

| # | Step | Description |
|---|------|-------------|
| 1 | Clear workspace cache | Settings → Clear cache |
| 2 | Remove all stale docs | Full cleanup |
| 3 | Re-upload from GitHub | Fresh copies |
| 4 | Verify in new thread | Clean context |

### Escalation

| Issue | Escalate To |
|-------|-------------|
| Persistent indexing failure | @RMN (AI Platform Engineer) |
| System-wide RAG issues | ADMIN workspace |

---

## 📋 Version History

| Version | Date | Ref | Changes |
|---------|------|-----|---------|
| 2.4.0 | 2026-W05 | GTM_2026-W05_253 | Initial release |

---

## 📋 Related Documents

| Document | Version | URL |
|----------|---------|-----|
| SharedKernel | v2.4.7 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |
| BEST-PRACTICES | v2.4.5 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/BEST-PRACTICES.md) |
| CASE-STUDY_GapAnalysis-BP-Recovery | v2.4.0 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/case-studies/CASE-STUDY_GapAnalysis-BP-Recovery_v2.4.0.md) |

---

#FlowsBros #FedArch #AnythingLLM #YonksPromptingAcademy #HumanTraining

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
