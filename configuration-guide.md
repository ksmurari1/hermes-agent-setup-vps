# Hermes Agent Configuration Guide

## Overview

Hermes Agent supports structured configuration through Markdown instruction files. Each file serves a distinct purpose, helping separate assistant behavior, user preferences, persistent knowledge, and project-specific guidelines.

This project uses four primary files:

- `SOUL.md`
- `USER.md`
- `MEMORY.md`
- `AGENTS.md`

---

## 1. SOUL.md — Personality and Behavior

**Location:** `~/.hermes/SOUL.md`

Defines the assistant's core personality, communication style, behavioral principles, and dynamic expert role instructions.

### Configured capabilities
- Direct, clear, practical, and professional communication
- Concise responses with structured explanations
- Step-by-step technical guidance
- Practical enterprise examples
- Accuracy and acknowledgment of uncertainty
- Safety and approval before destructive operations

### Dynamic Role Switching

The assistant can activate different expert roles based on user instructions.

Example:

```text
Switch to Power BI SME mode.
```

Or:

```text
Switch to GenAI Architect mode.
```

The role remains active until another role is requested or the assistant is returned to General Assistant mode.

---

## 2. USER.md — User Profile and Preferences

**Location:** `~/.hermes/USER.md`

Contains the user's professional identity, technical expertise, and preferred response style.

### Configured information
- Professional background and experience
- BI and analytics expertise
- Enterprise technology stack
- Generative AI and agent development interests
- Technical communication preferences

### Purpose

Provides personalized context so the assistant can adapt its explanations, recommendations, and technical guidance to the user.

---

## 3. MEMORY.md — Persistent Technical Knowledge

**Location:** `~/.hermes/MEMORY.md`

Maintains longer-term technical context and project-related knowledge.

### Configured information
- Professional technology stack
- Technical working conventions
- AI and GenAI project themes
- RAG and multi-agent development
- Automation and assistant projects

### Purpose

Provides a persistent reference for ongoing technical activities and helps maintain continuity across sessions.

### Retrieval validation

Direct file retrieval was tested successfully. However, detailed professional and project information was not consistently recalled automatically in fresh sessions.

---

## 4. AGENTS.md — Workspace Instructions

**Location:** `~/workspace/hermes-personal-assistant/AGENTS.md`

Defines instructions that apply specifically to the project workspace.

### Configured guidelines
- Clean, modular, and maintainable code
- Reliable and production-conscious implementations
- Secure handling of API keys and credentials
- Validation and error handling
- Human approval for sensitive actions
- Systematic troubleshooting
- Clear technical documentation
- Avoidance of unrelated or destructive modifications

### Validation

Automatic workspace discovery was tested successfully by asking Hermes to summarize the project-specific instructions.

---

## Configuration Summary

| Configuration | Scope | Responsibility |
|---|---|---|
| `SOUL.md` | Global | Personality and behavior |
| `USER.md` | Global | User profile and preferences |
| `MEMORY.md` | Global | Persistent knowledge |
| `AGENTS.md` | Workspace | Project-specific instructions |

## Best Practices

1. Keep personality and behavior separate from technical knowledge.
2. Store stable user preferences in `USER.md`.
3. Maintain reusable technical context in `MEMORY.md`.
4. Keep development instructions in the relevant project's `AGENTS.md`.
5. Avoid storing secrets or credentials in instruction files.
6. Validate changes in a fresh session.
7. Use explicit prompts to verify file retrieval when necessary.

---

## Conclusion

A structured configuration approach makes Hermes Agent more personalized, maintainable, and adaptable across technical domains and project environments.
