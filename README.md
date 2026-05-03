# Gemini Skills & Agentic Tools

A repository for [Gemini CLI](https://github.com/google/gemini-cli) skills, designed with cross-framework compatibility in mind.

## Design Philosophy

To ensure skills developed here can be easily ported to other agentic frameworks (e.g., LangChain, AutoGPT, CrewAI, or MCP servers), we adhere to the following standards:

1.  **Semantic Clarity:** Use clear, unambiguous names for skills and their intended actions.
2.  **Structured Metadata:** Every skill should include a metadata block (YAML or JSON) defining its purpose, inputs, and outputs.
3.  **Decoupled Logic:** Separate the *instruction* (the prompt) from the *implementation* (tools or shell commands).
4.  **Idempotency:** Where possible, skills should be designed to be safe to run multiple times.

## Directory Structure

```text
.
├── skills/               # Gemini-specific skill files (.md)
│   ├── example-skill/
│   │   ├── SKILL.md      # The Gemini Skill definition
│   │   ├── README.md     # Documentation and cross-framework mapping
│   │   └── tools/        # Supporting scripts/tools
└── specs/                # General specifications (OpenAPI, MCP, etc.)
```

## Contributing

When adding a new skill:
1. Create a new folder in `skills/`.
2. Include a `SKILL.md` following the Gemini CLI format.
3. Include a `README.md` that explains how to adapt the skill for other frameworks.
