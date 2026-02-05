# TMPL-010_ISC.md

## 📋 TMPL-010_ISC_v3.1.1.1.md
## ♾️ WeOwnNet 🌐 — Instance Season Certification Template

| Field | Value |
|-------|-------|
| Template | TMPL-010_ISC |
| Version | 3.1.1.1 |
| CCC-ID | GTM_2026-W06_232 |
| Created | 2026-02-05 (W06) |
| Season | #WeOwnSeason003 🚀 |
| Status | 🔒 LOCKED |
| Source of Truth | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-010_ISC_v3.1.1.1.md) |

---

## 📖 Table of Contents

1. [Overview](#-overview)
2. [ISC Header Template](#-isc-header-template)
3. [7-Point Checklist Template](#-7-point-checklist-template)
4. [Certification Summary Template](#-certification-summary-template)
5. [Attestation Block Template](#-attestation-block-template)
6. [Complete ISC Template](#-complete-isc-template)
7. [Usage Example](#-usage-example)
8. [ISC Responsibility Matrix](#-isc-responsibility-matrix)
9. [Related Documents](#-related-documents)
10. [Version History](#-version-history)

---

## 📋 Overview

### Definition (D-052)

| ID | Term | Definition |
|----|------|------------|
| D-052 | ISC | Instance Season Certification — Attestation that instance is certified for new #WeOwnSeason; 7-point checklist; mirrors VSA format |

### Purpose

| Benefit | Description |
|---------|-------------|
| Season Readiness | Confirms instance is ready for new #WeOwnSeason |
| Governance Alignment | Ensures #PinnedDocs, prompts, RAG are current |
| Audit Trail | Provides attestation record per instance |
| #FedArch Compliance | All instances certified = network ready |

### Requirement (BP-059)

| ID | Best Practice |
|----|---------------|
| BP-059 | Instance Certification REQUIRED within first 2 weeks of NEW #WeOwnSeason — ALL #FedArch instances MUST pass 7-point certification checklist; generates ISC attestation |

### Pass Criteria

| Result | Criteria |
|--------|----------|
| ✅ CERTIFIED | 7/7 checks PASS |
| ❌ FAILED | Any check FAIL |

### Deadline

| Season | Start | Deadline | Days |
|--------|-------|----------|------|
| #WeOwnSeason003 | Mon 02 Feb 2026 (W06) | Sun 15 Feb 2026 (W07) | 14 |

---

## 📋 ISC Header Template

```
## 📋 ISC: <Instance> — #WeOwnSeason00X

### Header

| Field | Value |
|-------|-------|
| ISC ID | ISC_<CCC>_<YYYY>-W<WW>_<NNN> |
| Instance | INT-00X |
| Name | <Instance Name> |
| Season | #WeOwnSeason00X |
| Certifier | @<CCC> |
| Date | <YYYY-MM-DD> |
| Time | <HH:MM> EST |
```

### Field Descriptions

| Field | Description | Example |
|-------|-------------|---------|
| ISC ID | Unique certification ID | ISC_GTM_2026-W06_240 |
| Instance | Instance code | INT-001 |
| Name | Instance name | AI.WeOwn.Agency |
| Season | Target season | #WeOwnSeason003 |
| Certifier | Primary certifier CCC | @GTM |
| Date | Certification date | 2026-02-05 |
| Time | Certification time | 07:00 EST |

---

## 📋 7-Point Checklist Template

```
### 7-Point Certification Checklist (BP-059)

| # | Phase | Check | Pass Criteria | Status | Notes |
|---|-------|-------|---------------|--------|-------|
| 1 | EMBEDDER | Model verified | Current recommended model | ✅ / ❌ | <model name> |
| 2 | #PinnedDocs | 4 docs present | SharedKernel, BEST-PRACTICES, PROTOCOLS, CCC @ v3.X.X.X | ✅ / ❌ | <versions> |
| 3 | SYSTEM PROMPT | Season tag | `#WeOwnSeason00X 🚀` present | ✅ / ❌ | |
| 4 | WORKSPACE PROMPTS | BP-053 + BP-054 | Non-CCC restriction + CCC-ID logic | ✅ / ❌ | |
| 5 | USER-IDENTITY | BP-058 | Owner(s) USER-IDENTITY current | ✅ / ❌ | <version> |
| 6 | RAG SYNC | GitHub connector | Refreshed post-season start | ✅ / ❌ | <date> |
| 7 | #ContextVolley | Reachability | Can reach #MetaAgent @ INT-001 | ✅ / ❌ | |
```

### Check Details

| # | Phase | Description | Verification Method |
|---|-------|-------------|---------------------|
| 1 | EMBEDDER | Embedding model is current recommended | Settings → Embedder |
| 2 | #PinnedDocs | 4 core docs pinned at v3.X.X.X | Workspace → Documents |
| 3 | SYSTEM PROMPT | Season tag present in system prompt | Settings → System Prompt |
| 4 | WORKSPACE PROMPTS | BP-053 + BP-054 blocks applied | Workspace → Settings |
| 5 | USER-IDENTITY | Owner's USER-IDENTITY doc current | RAG → `_USERS_/` |
| 6 | RAG SYNC | GitHub connector refreshed | Data Connectors |
| 7 | #ContextVolley | Can send/receive from #MetaAgent | Test message |

---

## 📋 Certification Summary Template

```
### Certification Summary

| Field | Value |
|-------|-------|
| Checks Passed | X/7 |
| Checks Failed | X/7 |
| Pass Rate | XX.X% |
| **Result** | ✅ **CERTIFIED** / ❌ **FAILED** |
```

### Result Logic

| Passed | Failed | Result |
|--------|--------|--------|
| 7 | 0 | ✅ CERTIFIED |
| 6 | 1 | ❌ FAILED |
| 5 | 2 | ❌ FAILED |
| < 5 | > 2 | ❌ FAILED |

---

## 📋 Attestation Block Template

```
### Attestation

═══════════════════════════════════════════════════════════════════════════════
ISC ATTESTATION
═══════════════════════════════════════════════════════════════════════════════

INSTANCE: INT-00X (<Instance Name>)
SEASON: #WeOwnSeason00X
RESULT: ✅ CERTIFIED / ❌ FAILED
CHECKS: X/7
CERTIFIER: AI:@<CCC> @ INT-00X
TIMESTAMP: <Day> <DD> <Mon> <YYYY> <HH:MM> EST
REF: <CCC-ID>

═══════════════════════════════════════════════════════════════════════════════
```

---

## 📋 Complete ISC Template

```
## 📋 ISC: INT-00X — #WeOwnSeason00X

### Header

| Field | Value |
|-------|-------|
| ISC ID | ISC_<CCC>_<YYYY>-W<WW>_<NNN> |
| Instance | INT-00X |
| Name | <Instance Name> |
| Season | #WeOwnSeason00X |
| Certifier | @<CCC> |
| Date | <YYYY-MM-DD> |
| Time | <HH:MM> EST |

---

### 7-Point Certification Checklist (BP-059)

| # | Phase | Check | Pass Criteria | Status | Notes |
|---|-------|-------|---------------|--------|-------|
| 1 | EMBEDDER | Model verified | Current recommended model | ✅ / ❌ | |
| 2 | #PinnedDocs | 4 docs present | v3.X.X.X | ✅ / ❌ | |
| 3 | SYSTEM PROMPT | Season tag | #WeOwnSeason00X 🚀 | ✅ / ❌ | |
| 4 | WORKSPACE PROMPTS | BP-053 + BP-054 | Applied | ✅ / ❌ | |
| 5 | USER-IDENTITY | BP-058 | Current | ✅ / ❌ | |
| 6 | RAG SYNC | GitHub connector | Refreshed | ✅ / ❌ | |
| 7 | #ContextVolley | Reachability | #MetaAgent | ✅ / ❌ | |

---

### Certification Summary

| Field | Value |
|-------|-------|
| Checks Passed | X/7 |
| Checks Failed | X/7 |
| Pass Rate | XX.X% |
| **Result** | ✅ **CERTIFIED** / ❌ **FAILED** |

---

### Attestation

═══════════════════════════════════════════════════════════════════════════════
ISC ATTESTATION
═══════════════════════════════════════════════════════════════════════════════

INSTANCE: INT-00X (<Instance Name>)
SEASON: #WeOwnSeason00X
RESULT: ✅ CERTIFIED / ❌ FAILED
CHECKS: X/7
CERTIFIER: AI:@<CCC> @ INT-00X
TIMESTAMP: <Day> <DD> <Mon> <YYYY> <HH:MM> EST
REF: <CCC-ID>

═══════════════════════════════════════════════════════════════════════════════

---

#FlowsBros #FedArch #ISC #WeOwnSeason00X

♾️ WeOwnNet 🌐
```

---

## 📋 Usage Example

## 📋 ISC: INT-001 — #WeOwnSeason003

### Header

| Field | Value |
|-------|-------|
| ISC ID | ISC_GTM_2026-W06_240 |
| Instance | INT-001 |
| Name | AI.WeOwn.Agency |
| Season | #WeOwnSeason003 |
| Certifier | @GTM |
| Date | 2026-02-05 |
| Time | 07:00 EST |

---

### 7-Point Certification Checklist (BP-059)

| # | Phase | Check | Pass Criteria | Status | Notes |
|---|-------|-------|---------------|--------|-------|
| 1 | EMBEDDER | Model verified | Current recommended | ✅ PASS | Qwen3 Embedding 4B |
| 2 | #PinnedDocs | 4 docs present | v3.X.X.X | ✅ PASS | SK v3.1.1.2, BP v3.1.1.1, PROTO v2.4.4, CCC v2.4.3 |
| 3 | SYSTEM PROMPT | Season tag | #WeOwnSeason003 🚀 | ✅ PASS | Present |
| 4 | WORKSPACE PROMPTS | BP-053 + BP-054 | Applied | ✅ PASS | 5/5 workspaces |
| 5 | USER-IDENTITY | BP-058 | Current | ✅ PASS | USER-IDENTITY_GTM v3.1.1.1 |
| 6 | RAG SYNC | GitHub connector | Refreshed | ✅ PASS | 2026-02-04 |
| 7 | #ContextVolley | Reachability | #MetaAgent | ✅ PASS | Verified |

---

### Certification Summary

| Field | Value |
|-------|-------|
| Checks Passed | 7/7 |
| Checks Failed | 0/7 |
| Pass Rate | 100% |
| **Result** | ✅ **CERTIFIED** |

---

### Attestation

═══════════════════════════════════════════════════════════════════════════════
ISC ATTESTATION
═══════════════════════════════════════════════════════════════════════════════

INSTANCE: INT-001 (AI.WeOwn.Agency)
SEASON: #WeOwnSeason003
RESULT: ✅ CERTIFIED
CHECKS: 7/7
CERTIFIER: AI:@GTM @ INT-001
TIMESTAMP: Thu 05 Feb 2026 07:00 EST
REF: GTM_2026-W06_240

═══════════════════════════════════════════════════════════════════════════════

---

#FlowsBros #FedArch #ISC #WeOwnSeason003

♾️ WeOwnNet 🌐

---

## 📋 ISC Responsibility Matrix

| Instance | Name | Primary Certifier | Backup | Deadline |
|----------|------|-------------------|--------|----------|
| INT-001 | AI.WeOwn.Agency | @GTM | @RMN | Sun 15 Feb |
| INT-002 | Lite.BurnedOut.xyz | @LDC | @GTM | Sun 15 Feb |
| INT-005 | AI.YonksTEAM.xyz | @GTM | @THY | Sun 15 Feb |
| INT-008 | AI.RomanDiD.xyz | @RMN | @GTM | Sun 15 Feb |

**Rule:** Instance Owner = Primary Certifier

---

## 📋 Related Documents

### Governance

| Document | ID | Description |
|----------|----|-------------|
| BP-059 | Best Practice | Instance Certification requirement |
| D-052 | Definition | ISC definition |
| BP-058 | Best Practice | USER-IDENTITY Season refresh |
| BP-053 | Best Practice | Non-CCC workspace prompt |
| BP-054 | Best Practice | System Prompt CCC-ID logic |

### Templates

| Document | Version | URL |
|----------|---------|-----|
| TMPL-008_VSA | v2.4.0 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-008_VSA_v2.4.0.md) |
| TMPL-009_USER-IDENTITY | v2.4.0 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-009_USER-IDENTITY_v2.4.0.md) |

### #PinnedDocs

| Document | Version | URL |
|----------|---------|-----|
| SharedKernel | v3.1.1.2 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |
| BEST-PRACTICES | v3.1.1.1 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/BEST-PRACTICES.md) |
| PROTOCOLS | v2.4.4 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/PROTOCOLS.md) |
| CCC | v2.4.3 | [GitHub](https://github.com/WeOwnNet/CCC/blob/main/CCC_CONTRIBUTOR-CODE-CONVENTION.md) |

---

## 📋 Version History

| Version | Date | #masterCCC | Approval | Changes |
|---------|------|------------|----------|---------|
| 3.1.1.1 | 2026-W06 | GTM_2026-W06_232 | GTM_2026-W06_234 | Initial creation; BP-059 + D-052 compliance; 7-point checklist; mirrors TMPL-008 (VSA) format |

---

#FlowsBros #FedArch #ISC #Templates #WeOwnSeason003

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
