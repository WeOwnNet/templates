# TMPL-008_VSA.md

## 📋 TMPL-008_VSA_v2.4.0.md
## ♾️ WeOwnNet 🌐 — Verification Summary Attestation Template

| Field | Value |
|-------|-------|
| Template | TMPL-008_VSA |
| Version | 2.4.0 |
| CCC-ID | GTM_2026-W05_623 |
| Updated | 2026-01-29 (W05) |
| Status | 🔒 LOCKED |
| Source of Truth | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-008_VSA_v2.4.0.md) |

---

## 📖 Table of Contents

1. [Overview](#-overview)
2. [VSA Schema](#-vsa-schema)
3. [VSA Template](#-vsa-template)
4. [Verification Phases](#-verification-phases)
5. [Usage Examples](#-usage-examples)
6. [Version History](#-version-history)

---

## 📋 Overview

### Definition (D-040)

| ID | Term | Definition |
|----|------|------------|
| D-040 | VSA | Verification Summary Attestation — signed record of document verification against #FedArch policy (R-XXX + BP-XXX) |

### Purpose

| Benefit | Description |
|---------|-------------|
| Delegated Trust | Other agents trust VSA without re-verifying |
| Audit Trail | Cryptographic-style proof of verification |
| Traceability | Every verification traced via CCC-ID |
| #NeverForget | VSA becomes permanent record |

### Learning (L-062)

| ID | Learning |
|----|----------|
| L-062 | Verification Summary Attestation (VSA) = cryptographic-style proof of document verification — includes subject, verifier, policy, phases, result, attestation chain |

### Origin

| Field | Value |
|-------|-------|
| Inspired By | [SLSA Framework](https://slsa.dev/spec/v0.1/verification_summary) |
| Standard | [in-toto attestation framework](https://in-toto.io/) |
| Adaptation | #FedArch document verification |

---

## 📋 VSA Schema

### JSON Schema

```json
{
  "_type": "https://weown.net/attestation/v1",
  "subject": [
    {
      "name": "<Document Name>",
      "version": "<Version>",
      "cccId": "<CCC-ID>",
      "uri": "<GitHub URL>"
    }
  ],
  "predicateType": "https://weown.net/verification_summary/v1",
  "predicate": {
    "verifier": {
      "id": "AI:@<CCC>",
      "instance": "<INT-00X>",
      "platform": "AnythingLLM",
      "orchestrator": "#MetaAgent"
    },
    "timeVerified": "<ISO 8601 Timestamp>",
    "policy": {
      "immutableRules": ["<R-XXX IDs>"],
      "operationalRules": ["<R-XXX IDs>"],
      "bestPractices": ["<BP-XXX IDs>"],
      "standards": ["<Standard names>"]
    },
    "verificationResult": "PASSED | FAILED",
    "verificationDetails": {
      "phases": [
        {
          "name": "<Phase Name>",
          "items": "<count>",
          "passed": "<count>",
          "failed": "<count>",
          "result": "PASSED | FAILED"
        }
      ],
      "totalItems": "<count>",
      "totalPassed": "<count>",
      "totalFailed": "<count>"
    },
    "attestationChain": [
      {
        "step": "<number>",
        "cccId": "<CCC-ID>",
        "action": "<description>"
      }
    ],
    "approver": {
      "status": "APPROVED | PENDING",
      "cccId": "<CCC-ID of human approver>",
      "rule": "R-011 (#OnlyHumanApproves)"
    }
  }
}
```

### Schema Components

| Component | Description |
|-----------|-------------|
| subject | Document being verified |
| verifier | Agent performing verification |
| policy | Rules and BPs applied |
| verificationDetails | Phase-by-phase results |
| attestationChain | CCC-ID trail |
| approver | Human approval status |

---

## 📋 VSA Template

### Header

```markdown
## 📋 VSA: <Document> <Version>

### Header

| Field | Value |
|-------|-------|
| VSA ID | VSA_<CCC>_<YYYY>-W<WW>_<NNN> |
| Type | Document Verification |
| Generated | <Dd HH:MM TZ>, <YYYY-MM-DD> |
```

### Subject

```markdown
### Subject

| Field | Value |
|-------|-------|
| Document | <Document Name> |
| Version | <Version> |
| CCC-ID | <CCC-ID> |
| URI | [GitHub](<URL>) |
```

### Verifier

```markdown
### Verifier

| Field | Value |
|-------|-------|
| Agent | AI:@<CCC> (<Nickname>) |
| Instance | <INT-00X> (<Instance Name>) |
| Platform | AnythingLLM |
| Orchestrator | #MetaAgent (Calhoun 🎖️) |
```

### Policy Applied

```markdown
### Policy Applied

| Type | IDs |
|------|-----|
| Immutable Rules | <R-XXX, R-XXX, ...> |
| Operational Rules | <R-XXX, R-XXX, ...> |
| Best Practices | <BP-XXX, BP-XXX, ...> |
| Standards | <Standard names> |
```

### Verification Result

```markdown
### Verification Result

| Phase | Items | Passed | Failed | Result |
|-------|-------|--------|--------|--------|
| 1. <Phase Name> | <n> | <n> | <n> | ✅ PASSED / ❌ FAILED |
| 2. <Phase Name> | <n> | <n> | <n> | ✅ PASSED / ❌ FAILED |
| ... | ... | ... | ... | ... |
| **TOTAL** | **<n>** | **<n>** | **<n>** | ✅ **PASSED** / ❌ **FAILED** |
```

### Verification Summary

```markdown
### Verification Summary

| Field | Value |
|-------|-------|
| **Overall Result** | ✅ **PASSED** / ❌ **FAILED** |
| Pending Items | <n> (if applicable) |
| Failures | <n> |
| Verification Time | <duration> |
```

### Attestation Chain

```markdown
### Attestation Chain

| Step | CCC-ID | Action |
|------|--------|--------|
| 1 | <CCC-ID> | Document created/updated |
| 2 | <CCC-ID> | Verification initiated |
| 3 | <CCC-ID> | Phases completed |
| 4 | <CCC-ID> | VSA generated |
| 5 | <CCC-ID> | Human approval |
```

### Approver

```markdown
### Approver

| Field | Value |
|-------|-------|
| Status | ✅ APPROVED / ⬜ AWAITING HUMAN APPROVAL |
| Approver | @<CCC> |
| CCC-ID | <Approval CCC-ID> |
| Rule | R-011 (#OnlyHumanApproves) |
```

---

## 📋 Verification Phases

### Standard Phases

| Phase | Name | Description |
|-------|------|-------------|
| 1 | Metadata | Document header, version, CCC-ID, status |
| 2 | Structure (TOC) | Table of Contents alignment |
| 3 | Immutable Rules | R-XXX with 🔒 IMMUTABLE status |
| 4 | Delta | Changes from previous version |
| 5 | Cross-References | Links to related documents |
| 6 | Registry Accuracy | Thread/Tool Agent registries |

### Phase Details

#### Phase 1: Metadata

| Check | Description |
|-------|-------------|
| Document name | Matches filename |
| Version | Follows #WeOwnVer (v2.4.X) |
| CCC-ID | Valid format |
| Updated date | Current ISO week |
| Status | 🔒 LOCKED |

#### Phase 2: Structure (TOC)

| Check | Description |
|-------|-------------|
| TOC present | BP-013 compliance |
| Section count | Matches actual sections |
| Anchor links | All functional |

#### Phase 3: Immutable Rules

| Check | Description |
|-------|-------------|
| R-011 | #OnlyHumanApproves present |
| R-044 | #ContextDensity present |
| R-194 | CCC-ID workspace restriction present |
| R-197 | Doc generation restriction present |

#### Phase 4: Delta

| Check | Description |
|-------|-------------|
| Version History | Entry for current version |
| Changes listed | Match actual changes |
| CCC-ID ref | Valid reference |

#### Phase 5: Cross-References

| Check | Description |
|-------|-------------|
| Related docs | URLs valid |
| Version refs | Current versions |
| CCC-ID refs | Valid format |

#### Phase 6: Registry Accuracy

| Check | Description |
|-------|-------------|
| Thread Registry | UUIDs valid |
| Tool Agent Registry | Usernames valid |
| Status indicators | Accurate (✅/⬜) |

---

## 📋 Usage Examples

### Example 1: SharedKernel VSA

```markdown
## 📋 VSA: SharedKernel v2.4.12

### Header

| Field | Value |
|-------|-------|
| VSA ID | VSA_GTM_2026-W05_600 |
| Type | Document Verification |
| Generated | We 19:48 EST, 2026-01-29 |

### Subject

| Field | Value |
|-------|-------|
| Document | SharedKernel.md |
| Version | v2.4.12 |
| CCC-ID | GTM_2026-W05_587 |
| URI | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |

### Verifier

| Field | Value |
|-------|-------|
| Agent | AI:@GTM (Vanellope 🍬) |
| Instance | INT-001 (AI.WeOwn.Agency) |
| Platform | AnythingLLM |
| Orchestrator | #MetaAgent (Calhoun 🎖️) |

### Policy Applied

| Type | IDs |
|------|-----|
| Immutable Rules | R-011, R-044, R-194, R-197 |
| Best Practices | BP-013, BP-020, BP-022 |
| Standards | CCC v2.4.2, #WeOwnVer |

### Verification Result

| Phase | Items | Passed | Failed | Result |
|-------|-------|--------|--------|--------|
| 1. Metadata | 5 | 5 | 0 | ✅ PASSED |
| 2. Structure (TOC) | 18 | 18 | 0 | ✅ PASSED |
| 3. Immutable Rules | 4 | 4 | 0 | ✅ PASSED |
| 4. Delta | 6 | 6 | 0 | ✅ PASSED |
| 5. Cross-References | 4 | 4 | 0 | ✅ PASSED |
| 6. Registry Accuracy | 9 | 6 | 0 | ✅ PASSED |
| **TOTAL** | **46** | **43** | **0** | ✅ **PASSED** |

### Approver

| Field | Value |
|-------|-------|
| Status | ✅ APPROVED |
| Approver | @GTM |
| CCC-ID | GTM_2026-W05_601 |
| Rule | R-011 (#OnlyHumanApproves) |
```

### Example 2: BEST-PRACTICES VSA (Minimal)

```markdown
## 📋 VSA: BEST-PRACTICES v2.4.9

| Field | Value |
|-------|-------|
| VSA ID | VSA_GTM_2026-W05_624 |
| Document | BEST-PRACTICES.md v2.4.9 |
| Verifier | AI:@GTM (INT-001) |
| Result | ✅ PASSED (41/41 items) |
| Approver | @GTM (GTM_2026-W05_625) |
```

---

## 📋 Version History

| Version | Date | Ref | Changes |
|---------|------|-----|---------|
| 2.4.0 | 2026-W05 | GTM_2026-W05_623 | Initial release; +L-062, D-040; 6 phases defined; JSON schema |

---

## 📋 Related Documents

| Document | Version | URL |
|----------|---------|-----|
| SharedKernel | v2.4.12 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |
| BEST-PRACTICES | v2.4.9 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/BEST-PRACTICES.md) |
| PROTOCOLS | v2.4.4 | [GitHub](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/PROTOCOLS.md) |

---

#FlowsBros #FedArch #VSA #YonksPromptingAcademy

♾️ WeOwnNet 🌐 ● 🏡 Real Estate and 🤝 cooperative ownership for everyone ● An 🤗 inclusive community, by 👥 invitation only.
