# Awesome Copilot Studio Agents

> **103 production-ready declarative agents for Microsoft 365 Copilot.**
> Paste each instruction block into Copilot Studio → New agent → Instructions field.
> No coding required. Deploy in minutes.

[![GitHub stars](https://img.shields.io/github/stars/kesslernity/awesome-copilot-studio-agents?style=flat-square)](https://github.com/kesslernity/awesome-copilot-studio-agents/stargazers)
[![License: CC BY-SA 4.0](https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-sa/4.0/)

> **103 production-ready agents across 17 domains and two industry packs: EPC & Energy and Investment Banking & M&A.** See [AGENTS.md](AGENTS.md) for the complete library.

---

## AI at Work Newsletter

Tested prompts for Microsoft 365 Copilot. One role at a time. Plus verified GenAI news and one insight you won't find in a changelog. Biweekly, 4-minute read.

**[Subscribe free →](https://newsletter.kesslernity.com/?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=hero)**: no spam, no fluff, unsubscribe anytime.

## Free AI Course

Want to go beyond agents? **AI Quick Start Essentials** is a free 35-minute course covering responsible AI use and practical human+AI collaboration workflows.

**[Start the free course →](https://trainings.kesslernity.com/?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=hero)**: no signup wall, no credit card.

**New:** [M365 Copilot Field Guide](https://github.com/kesslernity/m365-copilot-field-guide): 12 interactive reference guides (decision map, failure triage, one guide per feature)

---

## What This Is

A curated library of instruction sets for [Microsoft 365 Copilot declarative agents](https://learn.microsoft.com/en-us/microsoft-365-copilot/extensibility/overview-declarative-agent). Each agent is a paste-ready instruction block, ready to deploy without configuration files, coding, or Azure resources.

Every agent in this library:
- Requires a Microsoft 365 Copilot licence (the paid add-on, not included in standard M365 plans)
- Defaults to formal professional English (British spelling)
- Supports French output: write in French or ask for French output explicitly
- Includes a banned vocabulary list to prevent AI-sounding language
- Includes a built-in quality self-check the agent runs before every response
- Stays within the 8,000-character Copilot Studio instruction limit

---

## How to Deploy Any Agent

1. Go to [m365.cloud.microsoft/chat/agent/new](https://m365.cloud.microsoft/chat/agent/new): no separate tool needed, it's built into Microsoft 365 Copilot.
2. Enter the **Name** and **Description** from the agent file's frontmatter.
3. In the **Instructions** field, paste the full block from the `## Instructions` section of the relevant file.
4. Add knowledge sources (SharePoint sites) where noted.
5. Click **Create**: the agent is immediately available to `@mention` in Copilot Chat.

> You can also create agents via [Copilot Studio](https://copilotstudio.microsoft.com) for advanced configuration (additional knowledge sources, actions, authentication). For instruction-only agents in this library, the built-in Agent Builder is sufficient.

---

## Deploying Copilot across an org?

These agents are the build layer. A rollout also needs the IT prerequisites checked, a governance decision taken before anything is published, a sequence that survives week one, and something to put in front of the person holding the budget.

The **[M365 Copilot Deployment Kit](https://www.kesslernity.com/kit?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=readme)** covers that full picture: 28 field guides, a 90-day rollout roadmap, a governance checklist, 10 agent templates with practitioner notes on when to build each and what breaks in week one, and an ROI conversation template.

**[See what is in the kit →](https://www.kesslernity.com/kit?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=readme)**

Rolling it out across a team? There is no self-serve seat pack. Email mathieu@kesslernity.com with the headcount and it comes back as one quote and one invoice, with a bank transfer option if procurement prefers that to a card.

### The craft behind these agents

Every agent here lives inside the same 8,000-character limit and the same failure modes. When your own instruction block drifts, runs long, or will not hold its output format, the fix is a pattern rather than more instructions.

**[Agent Instruction Block Design Guide](https://www.kesslernity.com/products/agent-instruction-block-design-guide?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=readme)** ($19): 12 design patterns with before and after rewrites, the 8 named ways instruction blocks break, the 8,000-character constraint solved, a reusable scaffold, 5 worked rewrites, and a 10-question deployment test.

> Deciding *whether* an agent is even the right tool? **[When Not to Use AI](https://www.kesslernity.com/products/when-not-to-use-ai?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=readme)** ($29): the pre-flight check before you build. Or **[get both for $39](https://www.kesslernity.com/products/from-decision-to-deployment?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=readme)**.

**Start here, free:** [Copilot on One Page](https://store.kesslernity.com/l/copilot-on-one-page?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=hero) is the four-step loop these agents automate. Worth reading before you hand any of it to an agent that runs unattended.

---

## Agent Directory

### Writing & Communication

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 01 | [**Enterprise Writer**](agents/writing-communication/enterprise-writer.md) | Draft and polish professional communications | All Staff | None | `@Enterprise Writer ...` |
| 02 | [**AI Text Humanizer**](agents/writing-communication/ai-text-humanizer.md) | Remove AI writing patterns from any text | All Staff | None | `@AI Text Humanizer ...` |
| 03 | [**Meeting Scribe**](agents/writing-communication/meeting-scribe.md) | Turn meeting notes into structured records | All Staff | None | `@Meeting Scribe ...` |
| 04 | [**Professional Translator EN↔FR**](agents/writing-communication/professional-translator-en-fr.md) | Accurate English to French translation | All Staff | None | `@Professional Translator ...` |
| 40 | [**Executive Briefing Builder**](agents/writing-communication/executive-briefing-builder.md) | Compress long reports or email threads into a one-page C-suite brief | Leadership / Chiefs of Staff / EAs | None | `@Executive Briefing ...` |
| 41 | [**Tone Calibrator**](agents/writing-communication/tone-calibrator.md) | Adjust the register of any text to match a specified audience | All Staff | None | `@Tone Calibrator ...` |
| 99 | [**Brand Voice Enforcer**](agents/writing-communication/brand-voice-enforcer.md) | Check content against a defined brand voice guide, every deviation cited to the rule, with a corrected version | Comms / Marketing / Content Teams | None | `@Brand Voice Enforcer ...` |

### Project Management

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 05 | [**Project Status Reporter**](agents/project-management/project-status-reporter.md) | Generate structured project status reports | PMs / Leadership | Optional: project SharePoint | `@Project Status Reporter ...` |
| 06 | [**Risk Register Manager**](agents/project-management/risk-register-manager.md) | Build and manage project risk registers | PMs | None | `@Risk Register Manager ...` |
| 07 | [**Document Reviewer**](agents/project-management/document-reviewer.md) | Review documents for quality and completeness | All Staff | None | `@Document Reviewer ...` |
| 08 | [**Lessons Learned Manager**](agents/project-management/lessons-learned-manager.md) | Convert retrospectives into structured LL entries | PMs / Leadership | Optional: LL SharePoint | `@Lessons Learned Manager ...` |
| 09 | [**Presentation Builder**](agents/project-management/presentation-builder.md) | Build structured slide outlines for any audience | Leadership / PMs | None | `@Presentation Builder ...` |
| 42 | [**Project Charter Writer**](agents/project-management/project-charter-writer.md) | Build a structured project charter from a brief | PMs / PMO | None | `@Project Charter Writer ...` |
| 43 | [**RAID Log Manager**](agents/project-management/raid-log-manager.md) | Generate and update RAID logs from meeting notes or project updates | PMs / PMO | None | `@RAID Log Manager ...` |
| 44 | [**Scope of Work Drafter**](agents/project-management/scope-of-work-drafter.md) | Build a first-draft SOW from a requirement list | PMs / Commercial | None | `@Scope of Work Drafter ...` |
| 45 | [**Meeting Pre-Brief Builder**](agents/project-management/meeting-pre-brief-builder.md) | Turn an agenda and pre-reads into a briefing for attendees | PMs / Chiefs of Staff | None | `@Meeting Pre-Brief ...` |
| 46 | [**Action Register Tracker**](agents/project-management/action-register-tracker.md) | Extract all actions from any input and produce a numbered register | PMs / Team Leads / EAs | None | `@Action Register ...` |
| 47 | [**Project Closure Report Writer**](agents/project-management/project-closure-report-writer.md) | Structure project closeout documentation | PMs / PMO | None | `@Closure Report Writer ...` |

### HR & People

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 10 | [**Employee Onboarding Guide**](agents/hr-people/employee-onboarding-guide.md) | Answer new joiner questions | New Joiners / HR | Required: HR SharePoint | `@Onboarding Guide ...` |
| 11 | [**Job Description Writer**](agents/hr-people/job-description-writer.md) | Write clear, inclusive job descriptions | HR / Hiring Managers | None | `@Job Description Writer ...` |
| 12 | [**Performance Coach**](agents/hr-people/performance-coach.md) | Write SMART goals and structured performance feedback | All Staff / Managers | Optional: competency framework | `@Performance Coach ...` |
| 48 | [**Interview Question Builder**](agents/hr-people/interview-question-builder.md) | Generate structured, competency-based interview questions | HR / Hiring Managers | None | `@Interview Question Builder ...` |
| 49 | [**Probation Review Assistant**](agents/hr-people/probation-review-assistant.md) | Help managers structure 3-month and 6-month probation reviews | Line Managers / HR | None | `@Probation Review ...` |
| 50 | [**Redundancy Communication Writer**](agents/hr-people/redundancy-communication-writer.md) | Draft formal redundancy and restructure communications | HR / Legal / Senior Management | None | `@Redundancy Comms ...` |
| 51 | [**Exit Interview Analyser**](agents/hr-people/exit-interview-analyser.md) | Convert exit interview notes into a structured themes report | HR / People Analytics | None | `@Exit Interview Analyser ...` |
| 52 | [**Org Announcement Writer**](agents/hr-people/org-announcement-writer.md) | Draft internal announcements for org changes | HR / Senior Management / Comms | None | `@Org Announcement Writer ...` |

### Productivity

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 13 | [**Copilot Prompt Coach**](agents/productivity/copilot-prompt-coach.md) | Write and improve Copilot prompts | All Staff | None | `@Prompt Coach ...` |

### Finance

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 14 | [**Financial Report Writer**](agents/finance/financial-report-writer.md) | Draft management accounts commentary and board pack sections | Finance / Leadership | None | `@Financial Report Writer ...` |
| 15 | [**Budget Variance Analyst**](agents/finance/budget-variance-analyst.md) | Explain budget vs actual variances for management reporting | Finance / Controllers | None | `@Budget Variance Analyst ...` |
| 53 | [**Budget Justification Writer**](agents/finance/budget-justification-writer.md) | Convert a cost item list into a formal budget justification | Finance / PMs / Department Heads | None | `@Budget Justification Writer ...` |
| 54 | [**Board Paper Writer**](agents/finance/board-paper-writer.md) | Structure board-level papers with honest risk disclosure | CFO / CEO / Board Secretary | None | `@Board Paper Writer ...` |
| 55 | [**KPI Commentary Writer**](agents/finance/kpi-commentary-writer.md) | Take KPI results and write management commentary | Finance / FP&A / Business Partners | None | `@KPI Commentary Writer ...` |

### IT & Operations

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 18 | [**Incident Report Writer**](agents/it-ops/incident-report-writer.md) | Write IT incident post-mortems and reports | IT / Ops | None | `@Incident Report Writer ...` |
| 19 | [**Change Request Writer**](agents/it-ops/change-request-writer.md) | Write IT change management requests and CAB submissions | IT / Change Managers | None | `@Change Request Writer ...` |
| 56 | [**IT Request Scoper**](agents/it-ops/it-request-scoper.md) | Help non-technical staff write clear IT service requests | All Staff / Business Analysts | None | `@IT Request Scoper ...` |
| 57 | [**Runbook Writer**](agents/it-ops/runbook-writer.md) | Convert bullet-point procedures into structured runbooks | IT Ops / DevOps / Platform Engineers | None | `@Runbook Writer ...` |
| 58 | [**Security Risk Communicator**](agents/it-ops/security-risk-communicator.md) | Translate technical security findings into plain-language risk summaries | CISOs / Security Teams / Risk Committees | None | `@Security Risk Communicator ...` |
| 72 | [**Change-Incident Correlator**](agents/it-ops/change-incident-correlator.md) | Identify incidents likely caused by recent changes using temporal and semantic matching | IT / ITSM / Change Management | None | `@Change-Incident Correlator ...` |
| 73 | [**Problem Pattern Detector**](agents/it-ops/problem-pattern-detector.md) | Find recurring incident patterns for Problem Management, CI-agnostic, with request filtering | IT / ITSM / Problem Management | None | `@Problem Pattern Detector ...` |
| 98 | [**IT Self-Service Agent**](agents/it-ops/it-self-service-agent.md) | First-line IT support: resolution steps, policy answers, and pre-filled helpdesk escalations | All Staff | None | `@IT Self-Service ...` |

### Customer Success

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 20 | [**Escalation Handler**](agents/customer-success/escalation-handler.md) | Manage customer escalations with structured internal and external comms | CS / Account Managers | None | `@Escalation Handler ...` |
| 21 | [**Customer Response Writer**](agents/customer-success/customer-response-writer.md) | Write professional responses to customer queries and complaints | CS / Support | None | `@Customer Response Writer ...` |
| 97 | [**Customer Onboarding Agent**](agents/customer-success/customer-onboarding-agent.md) | Build onboarding plans, welcome comms, milestone check-ins and handover summaries (no live CRM access) | CS / Account Managers / Implementation | None | `@Customer Onboarding ...` |

### Sales & Business Development

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 16 | [**RFP Response Writer**](agents/sales/rfp-response-writer.md) | Write RFP responses and business proposals | Sales / BD | None | `@RFP Response Writer ...` |
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

### Commercial & Legal

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 63 | [**Tender Response Writer**](agents/commercial-legal/tender-response-writer.md) | Structure technical and commercial responses to ITBs and RFPs | BD / Commercial / Proposal Managers | None | `@Tender Response Writer ...` |
| 64 | [**Change Order Assistant**](agents/commercial-legal/change-order-assistant.md) | Structure scope change requests with schedule and cost impact | PMs / Commercial / Contract Managers | None | `@Change Order Assistant ...` |
| 65 | [**Claims Register Manager**](agents/commercial-legal/claims-register-manager.md) | Log and track contractual claims with evidence and deadlines | Commercial / Contract Managers | None | `@Claims Register Manager ...` |
| 66 | [**Back-Charge Drafter**](agents/commercial-legal/back-charge-drafter.md) | Write formal back-charge notices with contractual basis and value | Commercial / Contract Managers | None | `@Back-Charge Drafter ...` |
| 67 | [**NDA & Agreement Summariser**](agents/commercial-legal/nda-agreement-summariser.md) | Summarise key clauses from NDAs and service contracts | Business Managers / Commercial / Procurement | None | `@NDA Summariser ...` |
| 68 | [**Compliance Checklist Builder**](agents/commercial-legal/compliance-checklist-builder.md) | Convert a regulation or policy into a structured compliance checklist | Compliance / Legal / Risk / Audit | None | `@Compliance Checklist ...` |
| 69 | [**Contract Language Simplifier**](agents/commercial-legal/contract-language-simplifier.md) | Rewrite dense contractual clauses into plain language | All Staff / Business Managers | None | `@Contract Simplifier ...` |
| 70 | [**Policy Summariser**](agents/commercial-legal/policy-summariser.md) | Convert long policy documents into what you must do, what is prohibited | HR / Compliance / All Staff | None | `@Policy Summariser ...` |
| 71 | [**Incident Communication Drafter**](agents/commercial-legal/incident-communication-drafter.md) | Draft staff, client, and press communications for incidents and crises | Communications / Legal / Senior Leadership | None | `@Incident Comms Drafter ...` |
| 95 | [**Document Validation Agent**](agents/commercial-legal/document-validation-agent.md) | Check a document against a supplied policy or standard, findings by severity with corrective actions | Compliance / Quality / Legal | None | `@Document Validation ...` |
| 96 | [**Procurement / Vendor Assessment Agent**](agents/commercial-legal/procurement-vendor-assessment-agent.md) | Score vendor proposals against supplied criteria into a comparison matrix and risk summary (decides nothing) | Procurement / Commercial / Evaluation Panels | None | `@Vendor Assessment ...` |

### Data & Analytics

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 74 | [**Data Storyteller**](agents/data-analytics/data-storyteller.md) | Turn validated results into a stakeholder data narrative (no recompute, no overclaim) | Data / BI / Analytics | None | `@Data Storyteller ...` |
| 75 | [**KPI Definition Writer**](agents/data-analytics/kpi-definition-writer.md) | Turn a metric into a precise definition for governance (no value computed) | Analytics / BI / FP&A | None | `@KPI Definition Writer ...` |
| 76 | [**Report Requirements Builder**](agents/data-analytics/report-requirements-builder.md) | Turn a stakeholder ask into a BI requirements spec with gaps flagged | BI / Business Analysts | None | `@Report Requirements ...` |
| 77 | [**Data Dictionary Builder**](agents/data-analytics/data-dictionary-builder.md) | Turn a column list/schema into a data dictionary draft, [TBC] where unknown | Data / Analytics Engineers | None | `@Data Dictionary Builder ...` |

### Data Privacy

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 78 | [**DPIA Scaffold Builder**](agents/data-privacy/dpia-scaffold-builder.md) | Turn a processing description into a DPIA scaffold (ratings left to the DPO) | DPO / Privacy Counsel | None | `@DPIA Scaffold Builder ...` |
| 79 | [**ROPA Entry Drafter**](agents/data-privacy/ropa-entry-drafter.md) | Draft a Record of Processing Activities entry (lawful basis left to confirm) | Privacy Managers / DPO | None | `@ROPA Entry Drafter ...` |
| 80 | [**DSAR Intake Assistant**](agents/data-privacy/dsar-intake-assistant.md) | Structure a data subject request into intake, scope, and statutory clock | Privacy / DPO | None | `@DSAR Intake Assistant ...` |
| 81 | [**Breach Triage Organizer**](agents/data-privacy/breach-triage-organizer.md) | Organize suspected-breach facts for the DPO's assessment (no notifiability call) | DPO / Privacy / Incident Leads | None | `@Breach Triage Organizer ...` |

### Trade Compliance

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 82 | [**Export Classification Prep**](agents/trade-compliance/export-classification-prep.md) | Build a classification worksheet from a product/tech description (no ECCN/USML assigned) | Export Control / Trade Compliance | None | `@Export Classification Prep ...` |
| 83 | [**Restricted Party Screening Prep**](agents/trade-compliance/restricted-party-screening-prep.md) | Extract all parties to screen + a checklist (screening runs in the tool) | Trade Compliance / Trade Ops | None | `@Restricted Party Screening ...` |
| 84 | [**Export Red Flag Checker**](agents/trade-compliance/export-red-flag-checker.md) | Apply standard export red-flag indicators to a transaction (flags, not a finding) | Trade Compliance / Export Liaisons | None | `@Export Red Flag Checker ...` |
| 85 | [**End-Use Statement Drafter**](agents/trade-compliance/end-use-statement-drafter.md) | Draft an end-use/end-user statement scaffold + due-diligence questions | Trade Compliance / Sales | None | `@End-Use Statement ...` |

### Procurement & Vendor

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 86 | [**RFP Requirements Builder**](agents/procurement/rfp-requirements-builder.md) | Turn a need into structured RFP/RFQ requirements (criteria only, no scores) | Procurement / Category / Sourcing | None | `@RFP Requirements Builder ...` |
| 87 | [**Supplier Response Comparator**](agents/procurement/supplier-response-comparator.md) | Lay bid responses side by side vs requirements with gaps and questions | Procurement / Sourcing / Panels | None | `@Supplier Response Comparator ...` |
| 88 | [**Vendor Scorecard Builder**](agents/procurement/vendor-scorecard-builder.md) | Structure performance evidence into a scorecard (reviewer sets the ratings) | Procurement / Vendor Managers | None | `@Vendor Scorecard Builder ...` |
| 89 | [**Negotiation Prep Brief**](agents/procurement/negotiation-prep-brief.md) | Turn history and context into a negotiation prep brief (no price targets) | Procurement / Category / Buyers | None | `@Negotiation Prep Brief ...` |

### Advanced / MCP-Enabled

> These agents require platform connections via Microsoft Graph API. Deploy after all instruction-only agents are stable.

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 59 | [**SharePoint Knowledge Agent**](agents/advanced/sharepoint-knowledge-agent.md) | Answer questions grounded in a connected SharePoint site with source citations | All Staff | Required: SharePoint via Graph API | `@SharePoint Knowledge ...` |
| 60 | [**Email Triage Assistant**](agents/advanced/email-triage-assistant.md) | Classify, summarise, and draft responses to unread emails, never sends without confirmation | Senior Leaders / EAs / Chiefs of Staff | Required: Outlook via Graph API | `@Email Triage ...` |
| 61 | [**Meeting Intelligence Agent**](agents/advanced/meeting-intelligence-agent.md) | Produce structured records from Teams meeting transcripts | PMs / Team Leads / All Staff | Required: Teams transcripts via Graph API | `@Meeting Intelligence ...` |
| 62 | [**Cross-Agent Orchestrator**](agents/advanced/cross-agent-orchestrator.md) | Route user requests to the correct specialist agent, single entry point for the library | All Staff | All agents deployed | `@Copilot Assistant ...` |

---

## Industry Packs

### EPC & Energy

**4 agents, available now.** A project-team suite for Engineering, Procurement, and Construction projects in the energy sector: prompt coaching that fixes the missing-source failure, status reports written by phase, risk registers with the categories generic tools omit, and document review that lists every open HOLD. EPC acronyms preserved in EN and FR, and the HSE fence throughout: no permit, no sign-off, no classification, and a risk register that never passes for a HAZOP or a JSA.

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 100 | [**EPC Prompt Coach**](agents/industry/epc-energy/epc-prompt-coach.md) | Write and repair Copilot prompts for EPC work, and diagnose the missing-source failure behind most complaints | All Project Staff | None | `@EPC Prompt Coach ...` |
| 101 | [**EPC Status Reporter**](agents/industry/epc-energy/epc-status-reporter.md) | Status reports by phase: deliverables through IFR/IFA/IFC, PO and vendor documents, installed quantities vs MTO, systems handed over | PMs / Project Controls / Leadership | Optional: project SharePoint | `@EPC Status Reporter ...` |
| 102 | [**EPC Risk Register**](agents/industry/epc-energy/epc-risk-register.md) | Build, score and review registers on a 5x5 matrix with interface, vendor, permitting, logistics and marine categories (never a safety study) | PMs / Project Controls / Package Engineers | None | `@EPC Risk Register ...` |
| 103 | [**EPC Document Reviewer**](agents/industry/epc-energy/epc-document-reviewer.md) | Comment sheet against eight criteria: every open HOLD listed, tag and unit consistency, revision status vs content maturity | Engineers / Document Control / PMs | None | `@EPC Document Reviewer ...` |

[**View the EPC & Energy Agent Pack →**](agents/industry/epc-energy/README.md)

### Investment Banking & M&A

**5 agents, available now.** A deal-team suite for transaction structuring and diligence: requirements checklists cited to internal policy, CIM extraction with confidence grades, term sheet deviation reports, data-room provision sweeps with honest coverage reports, and a precedent library interface. Banking guardrails throughout: every agent retrieves and cites, none approves, prices, or advises. AI prepares, committees decide.

| # | Agent | Description | Audience | Knowledge | Invoke |
|---|-------|-------------|----------|-----------|--------|
| 90 | [**Deal Requirements Navigator**](agents/industry/investment-banking/structuring-requirements-navigator.md) | Retrieve structuring requirements as a checklist cited to internal policy (gaps flagged, never invented) | IB Deal Teams / Structuring | Required: policy SharePoint | `@Deal Requirements Navigator ...` |
| 91 | [**CIM & Teaser Digester**](agents/industry/investment-banking/cim-teaser-digester.md) | Extract a CIM or teaser into a referenced dataset with confidence grades (no valuation) | IB Analysts / Deal Teams | None | `@CIM & Teaser Digester ...` |
| 92 | [**Term Sheet Consistency Check**](agents/industry/investment-banking/term-sheet-consistency-checker.md) | Flag every deviation between a draft and the approved position, both clauses quoted verbatim | IB Deal Teams | Optional: deal Notebook | `@Term Sheet Consistency Check ...` |
| 93 | [**Data Room Extraction Sweep**](agents/industry/investment-banking/data-room-extraction-sweep.md) | Sweep a data-room folder into a provision tracker with a full coverage report (Cowork for full sweeps) | Deal Teams / Legal / Diligence | Required: data-room folder | `@Data Room Extraction Sweep ...` |
| 94 | [**Deal Precedent Finder**](agents/industry/investment-banking/deal-precedent-finder.md) | Retrieve comparable past deals with terms and sources; capture closed deals into the library | Deal Teams / Coverage | Required: precedent library | `@Deal Precedent Finder ...` |

[**View the Investment Banking & M&A Pack →**](agents/industry/investment-banking/README.md)


---

### Before you ship an agent to other people

Copying an agent that works is easy. Writing the instruction block so it keeps working when
somebody asks it something you did not anticipate is the part that takes the time.

[The Agent Instruction Block Design Guide](https://store.kesslernity.com/l/eyeauo?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=instruction_block_a) is twelve patterns for that. $19, one-time.

---

## Notes

- All agents default to formal professional English with British spelling.
- All agents support French output: write in French or include "in French" in your request.
- Agents marked **Required knowledge source** will not answer outside that source. Connect the SharePoint site before publishing.
- The AI-assistance disclaimer present in several agents (meeting records, status reports) must be reviewed by the document owner before official distribution.
- Agent instructions are sized to stay within the 8,000-character Copilot Studio instruction limit.

---

## Full Library

The library contains 103 agents across 17 domains and two industry packs, EPC & Energy and Investment Banking & M&A. See [AGENTS.md](AGENTS.md) for the complete index with links to every agent.

---

## Related Resources

**On Copilot Chat, not the premium licence?**

[**Awesome Copilot Chat Agents →**](https://github.com/kesslernity/awesome-copilot-chat-agents): 82 ready-to-deploy agents built for **Copilot Chat, no premium M365 Copilot licence required**. Works on any commercial M365 plan, no SharePoint grounding needed. The companion to this repo for the majority of your org that isn't on the paid Copilot seat.

**Using Microsoft 365 Copilot prompts rather than agents?**

[**Awesome Microsoft Copilot Prompts →**](https://github.com/kesslernity/awesome-microsoft-copilot-prompts): 573 production-tested M365 Copilot prompts across 20 role-specific collections. No Copilot Studio required: paste directly into Copilot Chat, Outlook, Teams, or Word.

**Running automated recurring briefings without building an agent?**

[**Scheduled Prompts →**](https://github.com/kesslernity/awesome-microsoft-copilot-prompts/tree/main/prompts/scheduled-prompts): 15 prompts designed to run automatically on a recurring schedule. Daily email briefings, weekly pipeline reviews, and Friday team summaries that run without you. Set up in 2 minutes via the clock icon in Copilot Chat. Requires M365 Copilot paid licence. GA since January 2026.

**Deploying Copilot across a team?**

[**Kesslernity →**](https://www.kesslernity.com/store?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=related): deployment tools for M365 Copilot teams. Frameworks, agent templates and decision guides you own outright, with no platform to log into and no consultant in the loop.

**More free Copilot reference?**

[**M365 Copilot Field Guide →**](https://www.kesslernity.com/guides?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=related): 27 reference guides, a decision map and a failure triage table. Browser-readable, print-ready, no account required.

---

## Stay Updated

- **Star this repo** to get notified when new agents are added
- **Watch releases** for new domain packs and major additions
- **Follow on X:** [@kesslernity](https://x.com/kesslernity): Copilot tips and enterprise AI insights
- **Follow on LinkedIn:** [Mathieu Kessler](https://linkedin.com/in/mathieukessler): enterprise AI deployment and agent design

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) and [AUTHORING-CHECKLIST.md](AUTHORING-CHECKLIST.md). All contributions welcome: new agents, improvements to existing instructions, and translations.

---

## License

[CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/): free to use, adapt, and distribute with attribution.

---

## Quick Links

- **[Agent Library](AGENTS.md)**: complete index of all 103 agents with links
- **[Authoring Checklist](AUTHORING-CHECKLIST.md)**: standards for contributing agents
- **[Contributing Guide](CONTRIBUTING.md)**: submission process
- **[AI at Work Newsletter](https://newsletter.kesslernity.com/?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=quicklinks)**: biweekly GenAI briefing
- **[Free AI Course](https://trainings.kesslernity.com/?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=quicklinks)**: AI Quick Start Essentials (35 min, free)
- **[365 Copilot Prompts](https://github.com/kesslernity/awesome-microsoft-copilot-prompts)**: the companion prompts repository
- **[Free Copilot Guides](https://www.kesslernity.com/guides?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=quicklinks)**: 27 reference guides, no account required
- **[Kesslernity Store](https://www.kesslernity.com/store?utm_source=github&utm_medium=readme&utm_campaign=studio_repo&utm_content=quicklinks)**: deployment tools for M365 Copilot teams
- **[License](https://creativecommons.org/licenses/by-sa/4.0/)**: CC BY-SA 4.0

---

*awesome-copilot-studio-agents · v2.0 · 2026*