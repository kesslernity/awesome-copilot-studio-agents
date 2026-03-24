# Awesome Copilot Studio Agents

> **39 production-ready declarative agents for Microsoft 365 Copilot.**
> Paste each instruction block into Copilot Studio → New agent → Instructions field.
> No coding required. Deploy in minutes.

[![GitHub stars](https://img.shields.io/github/stars/mathieukessler/awesome-copilot-studio-agents?style=flat-square)](https://github.com/mathieukessler/awesome-copilot-studio-agents/stargazers)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

> **39 agents built. 44 on the roadmap.** See [AGENTS.md](AGENTS.md) for the full library plan.

---

## AI at Work — Newsletter

Tested prompts for Microsoft 365 Copilot. One role at a time. Plus verified GenAI news and one insight you won't find in a changelog. Biweekly, 4-minute read.

**[Subscribe free →](https://newsletter.kesslernity.com)** — no spam, no fluff, unsubscribe anytime.

## Free AI Course

Want to go beyond agents? **AI Quick Start Essentials** is a free 35-minute course covering responsible AI use and practical human+AI collaboration workflows.

**[Start the free course →](https://trainings.kesslernity.com)** — no signup wall, no credit card.

---

## What This Is

A curated library of instruction sets for [Microsoft 365 Copilot declarative agents](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/overview-declarative-agent). Each agent is a paste-ready instruction block, battle-tested and ready to deploy without configuration files, coding, or Azure resources.

Every agent in this library:
- Works with a standard M365 Copilot licence (no premium required for declarative agents)
- Defaults to formal professional English (British spelling)
- Supports French output — write in French or ask for French output explicitly
- Includes a banned vocabulary list to prevent AI-sounding language
- Includes a built-in quality self-check the agent runs before every response
- Stays within the 8,000-character Copilot Studio instruction limit

---

## How to Deploy Any Agent

1. Go to [copilotstudio.microsoft.com](https://copilotstudio.microsoft.com) and sign in with your M365 account.
2. Click **Create → New agent**.
3. Enter the agent name and description from the table below.
4. In the **Instructions** field, paste the full block from the relevant file.
5. Add knowledge sources (SharePoint sites) where noted.
6. Click **Publish → Microsoft 365 Copilot**.
7. Users can then `@mention` the agent in Copilot Chat.

---

## Agent Directory

### Writing & Communication

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 01 | [**Enterprise Writer**](agents/writing-communication/enterprise-writer.md) | Draft and polish professional communications | All Staff | None | `@Enterprise Writer ...` |
| 02 | [**AI Text Humanizer**](agents/writing-communication/ai-text-humanizer.md) | Remove AI writing patterns from any text | All Staff | None | `@AI Text Humanizer ...` |
| 03 | [**Meeting Scribe**](agents/writing-communication/meeting-scribe.md) | Turn meeting notes into structured records | All Staff | None | `@Meeting Scribe ...` |
| 04 | [**Professional Translator EN↔FR**](agents/writing-communication/professional-translator-en-fr.md) | Accurate English–French translation | All Staff | None | `@Professional Translator ...` |

### Project Management

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 05 | [**Project Status Reporter**](agents/project-management/project-status-reporter.md) | Generate structured project status reports | PMs / Leadership | Optional: project SharePoint | `@Project Status Reporter ...` |
| 06 | [**Risk Register Manager**](agents/project-management/risk-register-manager.md) | Build and manage project risk registers | PMs | None | `@Risk Register Manager ...` |
| 07 | [**Document Reviewer**](agents/project-management/document-reviewer.md) | Review documents for quality and completeness | All Staff | None | `@Document Reviewer ...` |
| 08 | [**Lessons Learned Manager**](agents/project-management/lessons-learned-manager.md) | Convert retrospectives into structured LL entries | PMs / Leadership | Optional: LL SharePoint | `@Lessons Learned Manager ...` |
| 09 | [**Presentation Builder**](agents/project-management/presentation-builder.md) | Build structured slide outlines for any audience | Leadership / PMs | None | `@Presentation Builder ...` |

### HR & People

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 10 | [**Employee Onboarding Guide**](agents/hr-people/employee-onboarding-guide.md) | Answer new joiner questions | New Joiners / HR | Required: HR SharePoint | `@Onboarding Guide ...` |
| 11 | [**Job Description Writer**](agents/hr-people/job-description-writer.md) | Write clear, inclusive job descriptions | HR / Hiring Managers | None | `@Job Description Writer ...` |
| 12 | [**Performance Coach**](agents/hr-people/performance-coach.md) | Write SMART goals and structured performance feedback | All Staff / Managers | Optional: competency framework | `@Performance Coach ...` |

### Productivity

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 13 | [**Copilot Prompt Coach**](agents/productivity/copilot-prompt-coach.md) | Write and improve Copilot prompts | All Staff | None | `@Prompt Coach ...` |

### Finance

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 14 | [**Financial Report Writer**](agents/finance/financial-report-writer.md) | Draft management accounts commentary and board pack sections | Finance / Leadership | None | `@Financial Report Writer ...` |
| 15 | [**Budget Variance Analyst**](agents/finance/budget-variance-analyst.md) | Explain budget vs actual variances for management reporting | Finance / Controllers | None | `@Budget Variance Analyst ...` |

### Sales & Business Development

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 16 | [**Proposal Writer**](agents/sales/proposal-writer.md) | Write RFP responses and business proposals | Sales / BD | None | `@Proposal Writer ...` |
| 17 | [**Sales Email Writer**](agents/sales/sales-email-writer.md) | Write outbound prospecting and follow-up emails | Sales / AEs | None | `@Sales Email Writer ...` |
| 22 | [**Account Plan Writer**](agents/sales/account-plan-writer.md) | Build structured account plans with stakeholder maps and relationship gaps | Account Managers / BD | None | `@Account Plan Writer ...` |
| 23 | [**Win/Loss Analyser**](agents/sales/win-loss-analyser.md) | Analyse deal outcomes to surface patterns and strategic insights | Sales Leaders / Revenue Ops | None | `@Win Loss Analyser ...` |
| 24 | [**Competitive Intelligence Brief**](agents/sales/competitive-intelligence-brief.md) | Produce competitor briefs and battle cards with confidence labelling | Sales / Marketing / Strategy | None | `@Competitive Intel ...` |
| 25 | [**Pipeline Review Preparer**](agents/sales/pipeline-review-preparer.md) | Convert CRM data into structured pipeline reviews with health RAG and coverage ratios | Sales Leaders / Revenue Ops | None | `@Pipeline Review ...` |
| 26 | [**Partnership Proposal Writer**](agents/sales/partnership-proposal-writer.md) | Draft partnership and commercial alliance proposals | BD / Strategy / Leadership | None | `@Partnership Proposal ...` |
| 27 | [**Customer Case Study Writer**](agents/sales/customer-case-study-writer.md) | Write customer success stories in full, one-pager, and social formats | Marketing / Sales / CS | None | `@Case Study Writer ...` |

### Strategy & Executive

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 28 | [**Strategic Plan Structurer**](agents/strategy-executive/strategic-plan-structurer.md) | Structure multi-year strategic plans from executive input | C-Suite / Strategy Teams | None | `@Strategic Plan ...` |
| 29 | [**OKR Writer**](agents/strategy-executive/okr-writer.md) | Write, review, and cascade OKRs across teams | Leadership / Managers / Strategy | None | `@OKR Writer ...` |
| 30 | [**Executive Decision Brief**](agents/strategy-executive/executive-decision-brief.md) | Convert complex decisions into a one-page structured brief | C-Suite / Senior Leaders | None | `@Decision Brief ...` |
| 31 | [**Board Report Writer**](agents/strategy-executive/board-report-writer.md) | Draft board reports and papers with honest risk disclosure | CFO / CEO / Board Secretary | None | `@Board Report Writer ...` |

### Learning & Development

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 32 | [**Training Needs Analyser**](agents/learning-development/training-needs-analyser.md) | Convert performance gaps and survey data into structured TNA reports | L&D / HR / OD | None | `@Training Needs Analyser ...` |
| 33 | [**Learning Objective Writer**](agents/learning-development/learning-objective-writer.md) | Write Bloom's-levelled learning objectives for any course | L&D / Instructional Designers | None | `@Learning Objective Writer ...` |
| 34 | [**Course Outline Builder**](agents/learning-development/course-outline-builder.md) | Build structured course outlines with module sequencing and activity design | L&D / Instructional Designers | None | `@Course Outline Builder ...` |
| 35 | [**Assessment Question Writer**](agents/learning-development/assessment-question-writer.md) | Write scenario, MCQ, and short answer questions with marking criteria | L&D / Assessment Designers | None | `@Assessment Question Writer ...` |

### ESG & Sustainability

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 36 | [**ESG Report Section Writer**](agents/esg/esg-report-section-writer.md) | Draft ESG report sections aligned to GRI, TCFD, ESRS, or SASB | Sustainability Teams / CFOs | None | `@ESG Report Writer ...` |
| 37 | [**Carbon Footprint Narrative Writer**](agents/esg/carbon-footprint-narrative-writer.md) | Convert Scope 1, 2, and 3 emissions data into carbon narrative | Sustainability Teams / IR | None | `@Carbon Narrative ...` |
| 38 | [**Materiality Assessment Writer**](agents/esg/materiality-assessment-writer.md) | Structure double materiality assessments for ESRS, GRI, and TCFD | Sustainability Teams / Legal | None | `@Materiality Assessment ...` |
| 39 | [**ESG Commitment Tracker**](agents/esg/esg-commitment-tracker.md) | Track ESG commitments and produce progress reports with RAG status | Sustainability Teams / Board | None | `@ESG Commitment Tracker ...` |

### IT & Operations

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 18 | [**Incident Report Writer**](agents/it-ops/incident-report-writer.md) | Write IT incident post-mortems and reports | IT / Ops | None | `@Incident Report Writer ...` |
| 19 | [**Change Request Writer**](agents/it-ops/change-request-writer.md) | Write IT change management requests and CAB submissions | IT / Change Managers | None | `@Change Request Writer ...` |

### Customer Success

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 20 | [**Escalation Handler**](agents/customer-success/escalation-handler.md) | Manage customer escalations with structured internal and external comms | CS / Account Managers | None | `@Escalation Handler ...` |
| 21 | [**Customer Response Writer**](agents/customer-success/customer-response-writer.md) | Write professional responses to customer queries and complaints | CS / Support | None | `@Customer Response Writer ...` |

---

## Industry Packs

### EPC & Energy

A complete 13-agent suite built for Engineering, Procurement, and Construction projects in the energy sector. Includes EPC-specific terminology, bilingual EN/FR support, and HSE safety guardrails.

[**View the EPC & Energy Agent Pack →**](agents/industry/epc-energy/README.md)

---

## Notes

- All agents default to formal professional English with British spelling.
- All agents support French output — write in French or include "in French" in your request.
- Agents marked **Required knowledge source** will not answer outside that source. Connect the SharePoint site before publishing.
- The AI-assistance disclaimer present in several agents (meeting records, status reports) must be reviewed by the document owner before official distribution.
- Agent instructions are sized to stay within the 8,000-character Copilot Studio instruction limit.

---

## Full Roadmap

The library is planned to grow to 44 agents across 10 domains including Commercial & Legal, additional HR agents, IT & Digital expansion, vertical packs (Healthcare, Legal, NGO/Public Sector), and 4 MCP-enabled advanced agents.

See [AGENTS.md](AGENTS.md) for the complete planned agent list with descriptions and build priority.

---

## Related Resources

**Using Microsoft 365 Copilot prompts rather than agents?**

[**Awesome Microsoft Copilot Prompts →**](https://github.com/mathieukessler/awesome-microsoft-copilot-prompts) — 365 production-tested M365 Copilot prompts across 17 role-specific collections. No Copilot Studio required — paste directly into Copilot Chat, Outlook, Teams, or Word.

**Need enterprise AI deployment support?**

[**Kesslernity →**](https://kesslernity.com) — Enterprise AI deployment platform covering governed agents, adoption strategy, and team training programmes.

**More free AI prompts and tools?**

[**NerdyChefs.ai →**](https://nerdychefs.ai) — 1,600+ free AI prompts across 73 packs, no signup required.

---

## Stay Updated

- **Star this repo** to get notified when new agents are added
- **Watch releases** for new domain packs and major additions
- **Follow on X:** [@nerdychefsai](https://x.com/nerdychefsai) — Copilot tips and enterprise AI insights
- **Follow on LinkedIn:** [Mathieu Kessler](https://linkedin.com/in/mathieukessler) — enterprise AI deployment and agent design

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) and [AUTHORING-CHECKLIST.md](AUTHORING-CHECKLIST.md). All contributions welcome — new agents, improvements to existing instructions, and translations.

---

## License

[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) — free to use, adapt, and distribute with attribution.

---

## Quick Links

- **[Agent Library Plan](AGENTS.md)** — full roadmap with status and priority
- **[Authoring Checklist](AUTHORING-CHECKLIST.md)** — standards for contributing agents
- **[Contributing Guide](CONTRIBUTING.md)** — submission process
- **[AI at Work Newsletter](https://newsletter.kesslernity.com)** — biweekly GenAI briefing
- **[Free AI Course](https://trainings.kesslernity.com)** — AI Quick Start Essentials (35 min, free)
- **[365 Copilot Prompts](https://github.com/mathieukessler/awesome-microsoft-copilot-prompts)** — the companion prompts repository
- **[NerdyChefs.ai](https://nerdychefs.ai)** — 1,600+ free AI prompts
- **[Kesslernity](https://kesslernity.com)** — enterprise AI deployment platform
- **[License](https://creativecommons.org/licenses/by-sa/4.0/)** — CC BY-SA 4.0

---

*awesome-copilot-studio-agents — v1.1 — 2026*
