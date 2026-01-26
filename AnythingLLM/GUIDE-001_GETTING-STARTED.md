# Getting Started with AnythingLLM

## ♾️ WeOwnNet 🌐 — User Guide

| Field | Value |
|-------|-------|
| Guide | GUIDE-001 |
| Version | 2.4.1 |
| Updated | 2026-01-26 (W05) |
| Audience | New Users |
| Status | 🔒 LOCKED |

---

## 📖 Table of Contents

1. [Welcome](#-welcome)
2. [What is AnythingLLM?](#-what-is-anythingllm)
3. [Core Concepts](#-core-concepts)
4. [Workspace Overview](#-workspace-overview)
5. [Getting Started Steps](#-getting-started-steps)
6. [Working with Documents (RAG)](#-working-with-documents-rag)
7. [Using Agents](#-using-agents)
8. [Quick Reference](#-quick-reference)
9. [FAQ](#-faq)
10. [Version History](#-version-history)

---

## 👋 Welcome

Welcome to **AnythingLLM** on the ♾️ WeOwnNet 🌐 platform!

This guide will help you get started with your AI-powered workspace.

### What You'll Learn

| Topic | Description |
|-------|-------------|
| Workspaces | How to navigate and use workspaces |
| Documents | How to upload and query documents (RAG) |
| Agents | How to interact with AI agents |
| Best Practices | Tips for effective AI collaboration |

---

## 🤖 What is AnythingLLM?

**AnythingLLM** is an open-source AI platform that allows you to:

| Capability | Description |
|------------|-------------|
| **Chat** | Converse with AI models |
| **RAG** | Query your uploaded documents |
| **Agents** | Use AI agents with tools and capabilities |
| **Privacy** | Keep your data secure and private |

### Why AnythingLLM?

| Benefit | Description |
|---------|-------------|
| Data Sovereignty | Your data stays yours |
| FOSS | Free and Open Source Software |
| Flexible | Works with multiple LLM providers |
| Customizable | Tailor to your needs |

---

## 📚 Core Concepts

### Workspaces

A **Workspace** is a containerized environment where you can:

- Chat with AI
- Upload documents
- Use agents
- Maintain separate contexts

> "A Workspace functions a lot like a thread, but with the addition of containerization of your documents. Workspaces can share documents, but they do not talk to each other."

### Documents (RAG)

**RAG** (Retrieval-Augmented Generation) allows the AI to:

- Search your uploaded documents
- Provide answers based on your content
- Cite sources from your files

### Agents

**Agents** are AI assistants that can:

- Use tools (web search, calculators, etc.)
- Follow specific instructions
- Perform multi-step tasks

---

## 🏠 Workspace Overview

### The Three Workspace Types

♾️ WeOwnNet 🌐 uses three workspace types, each with a specific purpose:

| Workspace | Metaphor | Purpose | You Use For |
|-----------|----------|---------|-------------|
| **CCC** | 🤝 THE HANDS | Primary human interface | Daily interaction, tasks, questions |
| **MAIT** | 🧠 THE BRAIN | Strategy & meta-cognition | Planning, analysis, complex thinking |
| **ADMIN** | ⚙️ THE ENGINE | Administration functions | System configuration (advanced users) |

### Which Workspace Should I Use?

| If You Want To... | Use |
|-------------------|-----|
| Ask questions | 🤝 CCC |
| Get help with tasks | 🤝 CCC |
| Discuss strategy | 🧠 MAIT |
| Analyze complex problems | 🧠 MAIT |
| Configure system settings | ⚙️ ADMIN |

### Workspace Metaphors Explained

#### 🤝 CCC — THE HANDS

> *"The hands do the work."*

- Your primary workspace for daily interaction
- Where you collaborate with your AI agent
- User-friendly, task-focused

#### 🧠 MAIT — THE BRAIN

> *"The brain thinks strategically."*

- For deeper analysis and planning
- Meta-cognition and reflection
- Strategy and SME (Subject Matter Expert) discussions

#### ⚙️ ADMIN — THE ENGINE

> *"The engine powers everything."*

- System administration functions
- Document management
- Configuration and settings

---

## 🚀 Getting Started Steps

### Step 1: Access Your Workspace

1. Log in to AnythingLLM
2. Select your **CCC** workspace (🤝 THE HANDS)
3. You're ready to chat!

### Step 2: Say Hello

Try typing:

```
Hello! What can you help me with today?
```

### Step 3: Ask a Question

Try asking:

```
What is the CCC format for entry IDs?
```

### Step 4: Upload a Document (Optional)

1. Click the **Upload** button
2. Select a document (PDF, TXT, MD, etc.)
3. Wait for processing
4. Ask questions about your document!

---

## 📄 Working with Documents (RAG)

### Supported File Types

| Type | Extension | Notes |
|------|-----------|-------|
| PDF | `.pdf` | Most common |
| Text | `.txt` | Plain text |
| Markdown | `.md` | Formatted text |
| Word | `.docx` | Microsoft Word |
| Web | URL | Paste a link |

### How RAG Works

```
You ask a question
        ↓
AI searches your documents
        ↓
AI finds relevant content
        ↓
AI generates answer with citations
```

### Tips for Better RAG Results

| Tip | Description |
|-----|-------------|
| Be specific | Ask focused questions |
| Reference docs | "Based on the uploaded document..." |
| Check citations | Verify AI's sources |
| Upload quality | Better docs = better answers |

---

## 🤖 Using Agents

### What Agents Can Do

| Capability | Example |
|------------|---------|
| Web Search | "Search for the latest news on..." |
| Calculations | "Calculate the sum of..." |
| Document Query | "Find in my documents..." |
| Multi-step Tasks | "Research X, then summarize..." |

### Agent Best Practices

| Do | Don't |
|----|-------|
| Be clear and specific | Be vague |
| Break complex tasks into steps | Expect magic |
| Verify important information | Blindly trust |
| Provide context | Assume agent knows everything |

### Agent Commands

Start your message with `@agent` to invoke agent mode:

```
@agent Search the web for AnythingLLM documentation
```

---

## 📇 Quick Reference

### Workspace Metaphors

| Workspace | Metaphor | Use For |
|-----------|----------|---------|
| CCC | 🤝 THE HANDS | Daily tasks |
| MAIT | 🧠 THE BRAIN | Strategy |
| ADMIN | ⚙️ THE ENGINE | Configuration |

### Common Commands

| Command | Purpose |
|---------|---------|
| `@agent` | Invoke agent mode |
| `/reset` | Clear chat history |

### Getting Help

| Need | Action |
|------|--------|
| General help | Ask in CCC workspace |
| Technical issues | Contact admin |
| Documentation | Check uploaded guides |

---

## ❓ FAQ

### Q: Which workspace should I use?

**A:** Start with **CCC** (🤝 THE HANDS) for most tasks. It's your primary workspace for daily interaction.

### Q: Can I upload any document?

**A:** Most common formats are supported (PDF, TXT, MD, DOCX). Check with your admin for specific limits.

### Q: How do I get better answers?

**A:** Be specific in your questions, provide context, and reference uploaded documents when relevant.

### Q: What if the AI gives wrong information?

**A:** Always verify important information. AI can make mistakes. Report issues to improve the system.

### Q: Can workspaces share documents?

**A:** Workspaces can share documents, but they maintain separate conversation contexts.

---

## 📋 Version History

| Version | Date | Changes |
|---------|------|---------|
| 2.4.0 | 2026-W03 | Initial release |
| 2.4.1 | 2026-W05 | +Workspace metaphors (🤝 🧠 ⚙️), +Metaphor explanations, +Quick reference table |

---

## 🆘 Need More Help?

| Resource | Description |
|----------|-------------|
| This Guide | Getting started basics |
| PROTOCOLS.md | Interaction protocols |
| BEST-PRACTICES.md | Tips and best practices |
| Your Admin | Technical support |

---

#FlowsBros #FedArch #GettingStarted

♾️ WeOwnNet 🌐 | 🏡 Real Estate and 🤝 cooperative ownership for everyone. An 🤗 inclusive community, by 👥 invitation only.
