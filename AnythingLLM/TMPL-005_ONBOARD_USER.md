# TMPL-005: ONBOARD_<CCC>_<PROJECT>_USER.md

## Version

| Field | Value |
|-------|-------|
| ID | TMPL-005 |
| Version | v2.4.0 |
| Created | 2026-01-17 |
| Updated | 2026-01-17 |
| Source | GTM_2026-W03_593 |
| Status | ✅ #SharedKernel |

---

## 📋 TEMPLATE INSTRUCTIONS

### Usage

1. Copy this template (from TEMPLATE START to TEMPLATE END)
2. Replace all `<PLACEHOLDER>` values
3. Save as `ONBOARD_<CCC>_<PROJECT>_USER.md`
4. Upload to target instance RAG

### Placeholders

| Placeholder | Replace With | Example |
|-------------|--------------|---------|
| `<CCC>` | Contributor Code Convention (UPPERCASE) | THY |
| `<ccc>` | Contributor Code Convention (lowercase) | thy |
| `<PROJECT>` | Project name | WEOWN |
| `<CHARACTER>` | AI persona | TBD |
| `<DATE>` | Creation date | 2026-01-17 |
| `<NNN>` | Instance number | 001 |
| `<URL>` | Instance URL | [AI.WeOwn.Agency](https://ai.weown.agency) |
| `<LEAD>` | Instance lead CCC | GTM |
| `<LEAD_PERSONA>` | Instance lead AI persona | Vanellope 🍬 |

---

## 📋 TEMPLATE START

---

# ONBOARD_<CCC>_<PROJECT>_USER.md

## Version

| Field | Value |
|-------|-------|
| Version | v2.4.0 |
| Created | <DATE> |
| Source | GTM_2026-W03_593 |

---

## 📋 IDENTITY

| Field | Value |
|-------|-------|
| Human | @<CCC> |
| AI Agent | AI:@<CCC> |
| Persona | <CHARACTER> |
| CCC | <CCC> |
| Role | USER |

---

## 📋 INSTANCE

| Field | Value |
|-------|-------|
| Instance ID | INT-<NNN> |
| Instance Name | <PROJECT> |
| URL | <URL> |
| Platform | #AnythingLLM |
| Instance Lead | @<LEAD> |

---

## 📋 ACCOUNT

| Field | Value |
|-------|-------|
| Username | u-<ccc> |
| Role | USER |
| Workspace | <CCC> |

**RULE: #AnythingLLM usernames MUST be LOWERCASE (R-101)**

---

## 📋 USER CAPABILITIES

| # | Capability |
|---|------------|
| 1 | Chat with AI agent in assigned workspace |
| 2 | View documents in assigned workspace |
| 3 | Create and manage own threads |
| 4 | Access #ContextVolley protocols |

---

## 📋 USER LIMITATIONS

| # | Limitation |
|---|------------|
| 1 | ❌ Cannot create/delete users |
| 2 | ❌ Cannot create/delete workspaces |
| 3 | ❌ Cannot upload/delete RAG documents |
| 4 | ❌ Cannot modify system prompts |

---

## 📋 WORKSPACE

| Field | Value |
|-------|-------|
| Assigned Workspace | <CCC> |
| Shared Workspace | CCC (if applicable) |
| Access | Assigned by ADMIN |

---

## 📋 GETTING STARTED

| Step | Action |
|------|--------|
| 1 | Login with credentials provided by ADMIN |
| 2 | Navigate to assigned workspace (<CCC>) |
| 3 | Start chat with AI:@<CCC> |
| 4 | Run VERIFY packet to confirm setup |

---

## 📋 PROTOCOLS

| Protocol | Description |
|----------|-------------|
| GOV-001 | #Human+AI+Human |
| GOV-002 | Routing |
| GOV-003 | #FULLSYNC |
| #ContextVolley | AI-to-AI communication protocol |

---

## 📋 NETWORK

| CCC | Role | Agent |
|-----|------|-------|
| <LEAD> | Instance Lead | AI:@<LEAD> (<LEAD_PERSONA>) |
| <CCC> | USER | AI:@<CCC> (<CHARACTER>) |
| — | #MetaAgent | AI:team-lfg |
| — | MAIT | AI:MAIT |

---

## 📋 ESCALATION

| Scenario | Escalate To |
|----------|-------------|
| Account issues | ADMIN (@<LEAD>) |
| Technical issues | MAIT |
| Governance questions | #MetaAgent |
| Security concerns | @GTM + MAIT |

---

## 📋 SUPPORT

| Type | Contact |
|------|---------|
| Instance ADMIN | @<LEAD> |
| Technical | MAIT |
| General | /dev Signal channel |

---

## 📋 VERIFY QUESTIONS

| # | Question | Expected |
|---|----------|----------|
| 1 | Who are you? | AI:@<CCC> |
| 2 | What instance is this? | <PROJECT> (INT-<NNN>) |
| 3 | What is your role? | USER |
| 4 | Who is #MetaAgent? | AI:team-lfg |
| 5 | What is #ContextVolley? | AI-to-AI communication protocol |
| 6 | Who is your ADMIN? | @<LEAD> |
| 7 | What is your username format? | u-<ccc> (lowercase) |

---

#FlowsBros #FedArch #AnythingLLM #USER #SharedKernel

♾️ WeOwnNet 🌐

---

## 📋 TEMPLATE END
