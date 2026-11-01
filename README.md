# Hermes Agent — Personalized AI Assistant

A personalized AI assistant built using **Hermes Agent**, featuring persistent context, dynamic expert role switching, customized behavior, and workspace-aware instructions.

## Project Overview

This project demonstrates how to transform a general-purpose AI agent into a personalized technical assistant capable of adapting to different professional roles and development environments.

## Objectives

- Configure a personalized AI assistant using structured instruction files.
- Establish user identity, professional expertise, and response preferences.
- Enable dynamic expert role switching through natural-language prompts.
- Maintain persistent technical knowledge and project context.
- Implement workspace-specific instructions using `AGENTS.md`.
- Access the assistant through CLI and Telegram.

## Architecture

```text
                   HERMES AGENT
                        |
          ┌─────────────┼──────────────┐
          │             │              │
       SOUL.md       USER.md      MEMORY.md
          │             │              │
     Personality    User Profile   Knowledge &
     & Behavior     & Preferences  Project Context
          │             │              │
          └─────────────┼──────────────┘
                        |
                Personalized Agent
                        |
          ┌─────────────┼──────────────┐
          │             │              │
       Hermes CLI    Telegram     Role Switching
                                      |
                    ┌─────────────────┼──────────────┐
                    │                 │              │
                 Power BI SME   GenAI Architect   Other
                                                    Roles

           Workspace-specific context
                        |
                   AGENTS.md
                        |
              Project Instructions
```

## Configuration Files

| File | Description |
|---|---|
| `SOUL.md` | Defines assistant personality, behavior, tone, and dynamic role-switching rules |
| `USER.md` | Stores user identity, professional background, expertise, and response preferences |
| `MEMORY.md` | Maintains technical knowledge, active project themes, and working conventions |
| `AGENTS.md` | Provides workspace-specific development instructions, coding standards, and security guidelines |

## Key Features

### Personalized Assistant
- Customized personality and communication style
- User profile and technical expertise
- Context-aware technical assistance

### Dynamic Expert Roles
- Power BI SME
- GenAI Architect
- Microsoft Fabric Architect
- Python and AI Developer
- RAG and Multi-Agent Systems Expert
- Technical Mentor

Roles can be activated through natural-language instructions without manually modifying configuration files.

### Persistent Context
- User profile and preferences
- Technical stack and project themes
- Saved knowledge and working conventions

### Workspace Awareness
- Automatic discovery of `AGENTS.md`
- Project-specific development guidelines
- Security-conscious and maintainable development practices

### Multi-Interface Access
- Hermes CLI
- Telegram bot integration through Hermes Gateway

## Validation

The following capabilities were tested:

- Generic assistant introduction before personalization
- Personalized identity and response preferences
- Power BI SME role activation and technical response
- GenAI Architect role activation and architecture response
- Direct retrieval of saved profile and technical memory
- Automatic discovery of workspace-specific instructions
- Fresh-session memory recall behavior

## Demonstration

A screen-recorded demonstration showcases the configuration, role switching, memory retrieval, and workspace awareness.

## Technology

- Hermes Agent
- Linux / Ubuntu VPS
- Markdown-based configuration
- CLI and Telegram integration
- LLM-powered agent interaction

## Conclusion

This project demonstrates a practical approach to building a personalized AI assistant using structured instructions, persistent context, dynamic expertise, and workspace-aware behavior.

---

*Developed as part of the Social Eagle AI GenAI and Agentic AI learning journey.*
