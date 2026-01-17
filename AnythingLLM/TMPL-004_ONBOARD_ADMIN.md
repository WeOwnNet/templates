## 📋 TMPL-004_ONBOARD_ADMIN.md (v2.4.1)

# TMPL-004: ONBOARD_<CCC>_<PROJECT>_ADMIN.md

## Version

| Field | Value |
|-------|-------|
| ID | TMPL-004 |
| Version | v2.4.1 |
| Created | 2026-01-17 |
| Updated | 2026-01-17 |
| Source | GTM_2026-W03_577 |
| Status | 🟢 ACTIVE |

---

## 📋 TEMPLATE INSTRUCTIONS

### Usage

1. Copy this template (from TEMPLATE START to TEMPLATE END)
2. Replace all `<PLACEHOLDER>` values
3. Save as `ONBOARD_<CCC>_<PROJECT>_ADMIN.md`
4. Upload to target instance RAG

### Placeholders

| Placeholder | Replace With | Example |
|-------------|--------------|---------|
| `<CCC>` | Contributor Code Convention (UPPERCASE) | GTM |
| `<ccc>` | Contributor Code Convention (lowercase) | gtm |
| `<PROJECT>` | Project name | CONNEX |
| `<CHARACTER>` | AI persona | Vanellope 🍬 |
| `<DATE>` | Creation date | 2026-01-17 |
| `<NNN>` | Instance number | 001 |
| `<URL>` | Instance URL | [AI.WeOwn.Agency](https://ai.weown.agency/) |
| `<ROLE>` | Team role | Founder |
| `<TBD>` | To be determined | — |

---

## 📋 TEMPLATE START

---

# ONBOARD_<CCC>_<PROJECT>_ADMIN.md

## Version

| Field | Value |
|-------|-------|
| Version | v2.4.1 |
| Created | <DATE> |
| Source | GTM_2026-W03_577 |

---

## 📋 IDENTITY

| Field | Value |
|-------|-------|
| Human | @<CCC> |
| AI Agent | AI:@<CCC> |
| Persona | <CHARACTER> |
| CCC | <CCC> |
| Role | ADMIN |

---

## 📋 INSTANCE

| Field | Value |
|-------|-------|
| Instance ID | INT-<NNN> |
| Instance Name | <PROJECT> |
| URL | <URL> |
| Platform | #AnythingLLM |
| Instance Lead | @<CCC> |

---

## 📋 ADMIN RESPONSIBILITIES

| # | Responsibility |
|---|----------------|
| 1 | User management (create, modify, remove) |
| 2 | Workspace management |
| 3 | RAG document management |
| 4 | System prompt maintenance |
| 5 | Instance configuration |
| 6 | Backup coordination |

---

## 📋 SECURITY

| # | Rule |
|---|------|
| 1 | NO shared accounts with admin credentials (R-061) |
| 2 | Each admin = unique personal account |
| 3 | Shared/bot accounts = default (non-admin) |
| 4 | Admin credentials = never shared |

---

## 📋 WORKSPACE

| Field | Value |
|-------|-------|
| Default Workspace | CCC |
| Naming Convention | <CCC> for personal, CCC for shared |
| Access | Assigned by ADMIN |

---

## 📋 USER NAMING CONVENTION

| Prefix | Role | Example |
|--------|------|---------|
| u- | Default user | u-<ccc> |
| m- | MAIT:#MetaAgentInTraining | m-<ccc> |
| a- | Admin | a-<ccc> |

**RULE: #AnythingLLM usernames MUST be LOWERCASE (R-101)**

---

## 📋 SETUP CHECKLIST

| # | Task | Status |
|---|------|--------|
| 1 | Create user accounts (lowercase) | ⬜ |
| 2 | Create workspaces | ⬜ |
| 3 | Assign workspace access | ⬜ |
| 4 | Apply system prompts | ⬜ |
| 5 | Upload RAG documents | ⬜ |
| 6 | Configure integrations | ⬜ |
| 7 | Run VERIFY | ⬜ |

---

## 📋 #BestPractices

| # | Practice |
|---|----------|
| 1 | Users BEFORE workspaces |
| 2 | Workspace "CCC" = shared default |
| 3 | 1 workspace per agent |
| 4 | Assign access immediately after creation |
| 5 | System prompt BEFORE first interaction |
| 6 | RAG upload BEFORE agent use |
| 7 | Test after every configuration change |
| 8 | Document all changes |
| 9 | Usernames MUST be lowercase (R-101) |

---

## 📋 BACKUP

| # | Responsibility |
|---|----------------|
| 1 | Coordinate with @RMN (MAIT) for backups |
| 2 | Verify backup schedule |
| 3 | Test restore procedures |

---

## 📋 ESCALATION

| Scenario | Escalate To |
|----------|-------------|
| Instance creation/deletion | @GTM |
| Security incident | @GTM + @RMN |
| Governance question | #MetaAgent |
| Technical issue | @RMN (MAIT) |

---

## 📋 PROTOCOLS

| Protocol | Description |
|----------|-------------|
| GOV-001 | #Human+AI+Human |
| GOV-002 | Routing |
| GOV-003 | #FULLSYNC |
| #ContextVolley | AI-to-AI communication |

---

## 📋 NETWORK

| CCC | Role | Agent |
|-----|------|-------|
| GTM | Founder | AI:@GTM (Vanellope 🍬) |
| RMN | MAIT | AI:@RMN (Surge ⚡) |
| LDC | <ROLE> | AI:@LDC (<TBD>) |
| LFG | <ROLE> | AI:@LFG (<TBD>) |
| THY | <ROLE> | AI:@THY (<TBD>) |

---

## 📋 VERIFY QUESTIONS

| # | Question | Expected |
|---|----------|----------|
| 1 | Who are you? | AI:@<CCC> |
| 2 | What instance is this? | <PROJECT> (INT-<NNN>) |
| 3 | What is your role? | ADMIN |
| 4 | Who is #MetaAgent? | AI:team-lfg (Calhoun 🎖️) |
| 5 | What is #ContextVolley? | AI-to-AI communication protocol |

---

#FlowsBros #FedArch #AnythingLLM #ADMIN

♾️ WeOwnNet 🌐

---

## 📋 TEMPLATE END
