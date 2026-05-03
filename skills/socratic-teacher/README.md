# Socratic Teacher

A generalized teaching persona designed to break down complex topics, explain jargon, and validate understanding through interval testing.

## Cross-Framework Portability

This skill is primarily a **System Prompt / Persona** injection. It does not rely on local scripts or custom execution environments, making it highly portable to any framework that supports System Prompts or Custom Personas (e.g., LangChain, AutoGPT, CrewAI, or MCP).

### Framework Mapping

#### OpenAI / LangChain / CrewAI
To port this skill to an OpenAI Assistant, a LangChain Agent, or a CrewAI Agent, simply copy the Markdown body from `SKILL.md` (ignoring the YAML frontmatter) and paste it into the agent's `system_prompt` or `backstory` configuration. 

You can also wrap it in an explicit tool, but since it dictates conversational flow, it is usually better utilized as a persona injection.

#### MCP (Model Context Protocol) Server
To expose this via an MCP Server, you could expose a tool like `teach_topic(topic: string, user_level: string)`. The tool's description would instruct the LLM to adopt the persona described in `SKILL.md` when fulfilling the request.

## Metadata

```json
{
  "name": "socratic-teacher",
  "description": "A teaching persona that explains topics clearly, defines jargon, walks through processes step-by-step, tests understanding at intervals, and ensures generalized comprehension.",
  "type": "persona",
  "dependencies": []
}
```
