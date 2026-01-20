## GUIDE-001_GETTING-STARTED.md v2.4.0

# GUIDE-001: Getting Started with #AnythingLLM

## Version

| Field | Value |
|-------|-------|
| ID | GUIDE-001 |
| Version | v2.4.0 |
| Created | 2026-01-20 |
| Updated | 2026-01-20 |
| Source | GTM_2026-W04_058 |
| Audience | New Users, ADMINs |
| Status | ✅ #SharedKernel |

---

## 📋 1. OVERVIEW

### What is #AnythingLLM?

AnythingLLM Desktop is a "single-player" application you can install on any Mac, Windows, or Linux operating system and get local LLMs, RAG, and Agents with little to zero configuration and full privacy.

### Core Features

| Feature | Benefit |
|---------|---------|
| No-Code RAG | Makes document-based chat accessible to non-developers |
| AI Agents & Flows | Automates tasks and creates complex workflows |
| Multi-Modal Input | Processes images and audio, not just text |
| Multi-User & Permissions | Enables secure team collaboration (Docker) |
| Developer API Access | Allows for programmatic integration and customization |
| Local-First Privacy | Keeps your data on your own hardware |

### Two Deployment Options

| Option | Best For |
|--------|----------|
| Desktop | One-click installable app to use local LLMs, RAG, and Agents locally |
| Docker | Server-based service that many people can use at the same time with admin and rule-based access |

---

## 📋 2. PREREQUISITES

### System Requirements

| Component | Minimum |
|-----------|---------|
| RAM | At least 2 GB |
| CPU | 2-core CPU |
| Storage | 5 GB |

### Supported Platforms

| Platform | Supported |
|----------|-----------|
| macOS (Intel) | ✅ |
| macOS (Apple Silicon M1/M2/M3) | ✅ |
| Windows | ✅ |
| Linux | ✅ |
| Docker | ✅ |

---

## 📋 3. INSTALLATION

### Desktop Installation

| Step | Action |
|------|--------|
| 1 | Navigate to the homepage, download the desktop application for your device |
| 2 | Follow the installation instructions |
| 3 | Launch AnythingLLM |

### Mac Users

| Chip | File |
|------|------|
| Apple Silicon (M1/M2/M3) | AnythingLLMDesktop-AppleSilicon.dmg |
| Intel | AnythingLLMDesktop.dmg |

### Docker Installation

For multi-user environments, use Docker deployment. See official docs for Docker setup.

**#FedArch Note:** INT-001 (AI.WeOwn.Agency) and INT-002 (#ProjectConnex) use Docker deployment.

---

## 📋 4. FIRST STEPS

### Initial Setup

| Step | Action |
|------|--------|
| 1 | Launch AnythingLLM desktop and click Get Started |
| 2 | You will then be prompted to search for an LLM provider |
| 3 | Select your LLM provider |
| 4 | Configure embedding model |
| 5 | Create your first workspace |

### LLM Provider Options

| Provider | Description |
|----------|-------------|
| AnythingLLM Built-in | Collection of open source models, including Llama3.2 and Gemma, that do not require any additional setup and are free to use |
| External Providers | Connect to external, third-party providers such as OpenAI and HuggingFace, through API keys or self-hosted endpoints |

---

## 📋 5. WORKSPACES

### What are Workspaces?

AnythingLLM organizes your documents into workspaces. Workspaces are like a conversation thread that keeps your documents containerized. You can share documents between workspaces, but they won't interfere with each other, helping you maintain a clean context.

### Workspace Best Practices (#FedArch)

| ID | Best Practice |
|----|---------------|
| BP-009 | Workspace "CCC" = shared default |
| BP-010 | 1 workspace per agent |
| R-095 | CCC = default workspace naming (PROTOCOL) |
| R-096 | All users → "CCC" workspace (literal) |

### Creating a Workspace

| Step | Action |
|------|--------|
| 1 | Click "+ New Workspace" |
| 2 | Enter workspace name (use CCC for #FedArch) |
| 3 | Configure workspace settings |
| 4 | Assign users (multi-user mode) |

---

## 📋 6. AGENTS

### What are Agents?

Agents are specialized LLMs that can perform tasks like scraping websites, summarizing documents, and even creating charts.

### Agent Capabilities

| Capability | Description |
|------------|-------------|
| Web search/scraping | Agents can call tools for tasks like web search/scraping, deep research, and cross-app actions |
| Custom skills | You can develop custom skills for your agents, whether you need a simple API call or something more complex |

### Using Agents

You can enable them via environment configuration, then invoke an agent with an @agent mention in chat.

### #FedArch Agent Convention

| Field | Convention |
|-------|------------|
| Naming | AI:@<CCC> (e.g., AI:@GTM) |
| Persona | Character assignment (e.g., Vanellope 🍬) |
| Workspace | 1 workspace per agent |

---

## 📋 7. RAG (Retrieval-Augmented Generation)

### What is RAG?

AnythingLLM comes with its own local embedding model and vector database for retrieval-augmented generation workflows, which augments the standard LLM with your own data.

### Uploading Documents

| Step | Action |
|------|--------|
| 1 | Open workspace |
| 2 | Click upload icon |
| 3 | Drag/drop or select files |
| 4 | Wait for embedding |
| 5 | Start chatting with your documents |

### Supported File Types

| Type | Examples |
|------|----------|
| Documents | PDF, DOCX, TXT, MD |
| Code | Python, JavaScript, etc. |
| Data | CSV, JSON |

### #FedArch RAG Best Practices

| ID | Best Practice |
|----|---------------|
| BP-011 | Use drag/drop or paste — avoid hotdir |
| — | Upload SharedKernel.md to all instances |
| — | Upload PROTOCOLS.md for protocol reference |

---

## 📋 8. MULTI-USER MODE

### User Roles

| ID | Role | Description |
|----|------|-------------|
| D-016 | [ADMIN](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-004_ONBOARD_ADMIN.md) | Full access + logs + system settings |
| D-017 | MANAGER | Workspace mgmt, no system settings |
| D-018 | [DEFAULT](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-005_ONBOARD_USER.md) | Limited, scoped to assigned workspaces |

### #FedArch Rules

| ID | Rule |
|----|------|
| R-101 | Usernames = LOWERCASE |
| R-102 | Multi-user mode = NOT reversible |
| R-103 | Default users can only access assigned workspaces |

### Username Convention

| Prefix | Role | Example |
|--------|------|---------|
| u- | Default user | u-thy |
| m- | MAIT | m-rmn |
| a- | Admin | a-gtm |

---

## 📋 9. BEST PRACTICES

### General Best Practices

| # | Practice |
|---|----------|
| 1 | Start with Desktop for learning |
| 2 | Use Docker for multi-user/production |
| 3 | Keep workspaces focused (1 topic per workspace) |
| 4 | Upload relevant documents before chatting |
| 5 | Use @agent to invoke agent capabilities |

### #FedArch Best Practices

| ID | Best Practice |
|----|---------------|
| BP-008 | Users BEFORE workspaces |
| BP-009 | Workspace "CCC" = shared default |
| BP-010 | 1 workspace per agent |
| BP-011 | Use drag/drop or paste — avoid hotdir |
| BP-012 | Workspace-specific LLM overrides system LLM |

### Core Principles

| # | Principle |
|---|-----------|
| 1 | #OnlyHumanApproves — AI cannot approve |
| 2 | #LessIsMore — concise, tables > paragraphs |
| 3 | #NeverForget — learnings permanent |
| 4 | Data Sovereignty — Users own data |

---

## 📋 10. TROUBLESHOOTING

### Common Issues

| Issue | Solution |
|-------|----------|
| Agent not using tools | Use `/reset` to clear chat history |
| Agent not responding | Swap to higher quantization model |
| Slow performance | Turn off unused tools |
| Connection errors | Check network/firewall settings |

### #FedArch Escalation

| Scenario | Escalate To |
|----------|-------------|
| Account issues | Instance ADMIN |
| Technical issues | MAIT (@RMN) |
| Governance questions | #MetaAgent (AI:team-lfg) |
| Security concerns | @GTM + MAIT |

---

## 📋 11. NEXT STEPS

### Documentation

| Doc | Description | Link |
|-----|-------------|------|
| SharedKernel.md | Core #FedArch reference | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/SharedKernel.md) |
| PROTOCOLS.md | Protocol specifications | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/PROTOCOLS.md) |
| TMPL-004 | ADMIN onboarding | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-004_ONBOARD_ADMIN.md) |
| TMPL-005 | USER onboarding | [GH](https://github.com/WeOwnNet/templates/blob/main/AnythingLLM/TMPL-005_ONBOARD_USER.md) |

### Official Resources

| Resource | URL |
|----------|-----|
| AnythingLLM Docs | [docs.anythingllm.com](https://docs.anythingllm.com) |
| AnythingLLM Download | [anythingllm.com](https://anythingllm.com) |
| GitHub | [github.com/Mintplex-Labs/anything-llm](https://github.com/Mintplex-Labs/anything-llm) |

### #FedArch Instances

| ID | Name | URL | Lead |
|----|------|-----|------|
| INT-001 | AI.WeOwn.Agency | ai.weown.agency | @GTM |
| INT-002 | #ProjectConnex | Lite.BurnedOut.xyz | @LDC |

---

#FlowsBros #FedArch #AnythingLLM #SharedKernel

♾️ WeOwnNet 🌐
