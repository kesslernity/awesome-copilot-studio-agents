# Advanced / MCP-Enabled Agents

> Four agents that need platform connections through the Microsoft Graph API. Deploy these after every instruction-only agent in the library is stable.

[← Full agent index](../../AGENTS.md) | [Repository README](../../README.md)

---

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 59 | [**SharePoint Knowledge Agent**](sharepoint-knowledge-agent.md) | Answer questions grounded in a connected SharePoint site with source citations | All Staff | Required: SharePoint via Graph API | `@SharePoint Knowledge ...` |
| 60 | [**Email Triage Assistant**](email-triage-assistant.md) | Classify, summarise, and draft responses to unread emails, never sends without confirmation | Senior Leaders / EAs / Chiefs of Staff | Required: Outlook via Graph API | `@Email Triage ...` |
| 61 | [**Meeting Intelligence Agent**](meeting-intelligence-agent.md) | Produce structured records from Teams meeting transcripts | PMs / Team Leads / All Staff | Required: Teams transcripts via Graph API | `@Meeting Intelligence ...` |
| 62 | [**Cross-Agent Orchestrator**](cross-agent-orchestrator.md) | Route user requests to the correct specialist agent, single entry point for the library | All Staff | All agents deployed | `@Copilot Assistant ...` |

---

These are the agents that read things they were not pointed at. An email triage agent sees every
thread. A SharePoint knowledge agent inherits whatever permissions its source has, including the
ones somebody set wrong two years ago.

[Govern Your Agents](https://store.kesslernity.com/l/govern-your-agents?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=agents_advanced_a) is about that boundary. $47, one-time.
