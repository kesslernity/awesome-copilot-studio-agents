# Agent Library — Full Roadmap

> **39 agents built. 71 on the roadmap.**
> This file is the master planning document for the library.
> Built agents link to their files. Planned agents are marked with their build priority.

---

## Legend

| Symbol | Meaning |
|--------|---------|
| ✅ | Built and in the library |
| 🟢 | Planned — new territory, no public equivalent |
| 🔵 | Planned — extends the base suite |
| 🟡 | Planned — vertical / industry-specific pack |
| 🔴 | Planned — Advanced (requires MCP or Graph API connection) |

---

## Build Priority

| Phase | Agents | Focus |
|-------|--------|-------|
| Phase 1 ✅ | 01–21 | Core horizontal — writing, project management, finance, HR, IT, sales |
| Phase 2 ✅ | 22–39 | Sales expansion, strategy & executive, learning & development, ESG |
| Phase 3 | 40–58 | Writing, PM, HR, Finance, and IT expansions |
| Phase 4 | — | Vertical packs (Healthcare, Legal, NGO/Public Sector) — numbered when built |
| Phase 5 | 59–62 | Advanced / MCP-enabled (build after instruction-only library is stable) |

---

## Writing & Communication

| # | Status | Agent | File |
|---|--------|-------|------|
| 01 | ✅ | Enterprise Writer | [agents/writing-communication/enterprise-writer.md](agents/writing-communication/enterprise-writer.md) |
| 02 | ✅ | AI Text Humanizer | [agents/writing-communication/ai-text-humanizer.md](agents/writing-communication/ai-text-humanizer.md) |
| 03 | ✅ | Meeting Scribe | [agents/writing-communication/meeting-scribe.md](agents/writing-communication/meeting-scribe.md) |
| 04 | ✅ | Professional Translator EN↔FR | [agents/writing-communication/professional-translator-en-fr.md](agents/writing-communication/professional-translator-en-fr.md) |
| 40 | 🟢 | Executive Briefing Builder | Compresses long reports or email threads into a 1-page C-suite brief: situation, decision required, options, recommendation. |
| 41 | 🔵 | Tone Calibrator | Adjusts the register of any text to match a specified audience without changing the substance. |

---

## Project Management

| # | Status | Agent | File |
|---|--------|-------|------|
| 05 | ✅ | Project Status Reporter | [agents/project-management/project-status-reporter.md](agents/project-management/project-status-reporter.md) |
| 06 | ✅ | Risk Register Manager | [agents/project-management/risk-register-manager.md](agents/project-management/risk-register-manager.md) |
| 07 | ✅ | Document Reviewer | [agents/project-management/document-reviewer.md](agents/project-management/document-reviewer.md) |
| 08 | ✅ | Lessons Learned Manager | [agents/project-management/lessons-learned-manager.md](agents/project-management/lessons-learned-manager.md) |
| 09 | ✅ | Presentation Builder | [agents/project-management/presentation-builder.md](agents/project-management/presentation-builder.md) |
| 42 | 🟢 | Project Charter Writer | Builds a structured project charter from a brief: objectives, scope, stakeholders, constraints, milestones, budget envelope, governance. |
| 43 | 🟢 | RAID Log Manager | Generates and updates RAID logs (Risks, Assumptions, Issues, Dependencies) from meeting notes or project updates. |
| 44 | 🟢 | Scope of Work Drafter | Builds a first-draft SOW from a requirement list: scope inclusions, exclusions, interfaces, deliverables, assumptions. |
| 45 | 🟢 | Meeting Pre-Brief Builder | The inverse of a meeting scribe. Takes an agenda and pre-reads; produces a briefing for attendees: decisions needed, known positions, open questions, each attendee's expected contribution. |
| 46 | 🔵 | Action Register Tracker | Extracts all actions from any input and produces a numbered register with owner, due date, priority, and status. Flags stale or ownerless items. |
| 47 | 🟢 | Project Closure Report Writer | Structures project closeout documentation: final scope vs baseline, budget outturn, schedule variance, key achievements, lessons learned summary, outstanding items. |

---

## HR & People

| # | Status | Agent | File |
|---|--------|-------|------|
| 10 | ✅ | Employee Onboarding Guide | [agents/hr-people/employee-onboarding-guide.md](agents/hr-people/employee-onboarding-guide.md) |
| 11 | ✅ | Job Description Writer | [agents/hr-people/job-description-writer.md](agents/hr-people/job-description-writer.md) |
| 12 | ✅ | Performance Coach | [agents/hr-people/performance-coach.md](agents/hr-people/performance-coach.md) |
| 48 | 🟢 | Interview Question Builder | Generates structured, competency-based interview questions for a given role, mapped to a competency framework. |
| 49 | 🟢 | Probation Review Assistant | Helps managers structure 3-month and 6-month probation review conversations. |
| 50 | 🟢 | Redundancy Communication Writer | Drafts formal redundancy and restructure communications. Legally measured tone, separate templates for at-risk notification, confirmation, and appeals. |
| 51 | 🟢 | Exit Interview Analyser | Converts exit interview notes into a structured themes report: top reasons for leaving, patterns, recommended actions. |
| 52 | 🔵 | Org Announcement Writer | Drafts internal announcements for org changes: new hires, promotions, departures, restructures, leadership changes. |

---

## Productivity

| # | Status | Agent | File |
|---|--------|-------|------|
| 13 | ✅ | Copilot Prompt Coach | [agents/productivity/copilot-prompt-coach.md](agents/productivity/copilot-prompt-coach.md) |

---

## Finance & Reporting

| # | Status | Agent | File |
|---|--------|-------|------|
| 14 | ✅ | Financial Report Writer | [agents/finance/financial-report-writer.md](agents/finance/financial-report-writer.md) |
| 15 | ✅ | Budget Variance Analyst | [agents/finance/budget-variance-analyst.md](agents/finance/budget-variance-analyst.md) |
| 53 | 🟢 | Budget Justification Writer | Converts a cost item list into a formal budget justification: rationale per item, alternatives considered, risk of non-approval. |
| 54 | 🟢 | Board Paper Writer | Structures board-level papers: purpose, background, analysis, recommendation, financial implications, risks, resolution required. |
| 55 | 🟢 | KPI Commentary Writer | Takes KPI results (figures, RAG statuses) and writes management commentary: performance vs target, root cause, forward outlook. |

---

## Sales & Business Development

| # | Status | Agent | File |
|---|--------|-------|------|
| 16 | ✅ | RFP Response Writer | [agents/sales/rfp-response-writer.md](agents/sales/rfp-response-writer.md) |
| 17 | ✅ | Sales Email Writer | [agents/sales/sales-email-writer.md](agents/sales/sales-email-writer.md) |
| 22 | ✅ | Account Plan Writer | [agents/sales/account-plan-writer.md](agents/sales/account-plan-writer.md) |
| 23 | ✅ | Win/Loss Analyser | [agents/sales/win-loss-analyser.md](agents/sales/win-loss-analyser.md) |
| 24 | ✅ | Competitive Intelligence Brief | [agents/sales/competitive-intelligence-brief.md](agents/sales/competitive-intelligence-brief.md) |
| 25 | ✅ | Pipeline Review Preparer | [agents/sales/pipeline-review-preparer.md](agents/sales/pipeline-review-preparer.md) |
| 26 | ✅ | Partnership Proposal Writer | [agents/sales/partnership-proposal-writer.md](agents/sales/partnership-proposal-writer.md) |
| 27 | ✅ | Customer Case Study Writer | [agents/sales/customer-case-study-writer.md](agents/sales/customer-case-study-writer.md) |

---

## Strategy & Executive

| # | Status | Agent | File |
|---|--------|-------|------|
| 28 | ✅ | Strategic Plan Structurer | [agents/strategy-executive/strategic-plan-structurer.md](agents/strategy-executive/strategic-plan-structurer.md) |
| 29 | ✅ | OKR Writer | [agents/strategy-executive/okr-writer.md](agents/strategy-executive/okr-writer.md) |
| 30 | ✅ | Executive Decision Brief | [agents/strategy-executive/executive-decision-brief.md](agents/strategy-executive/executive-decision-brief.md) |
| 31 | ✅ | Board Report Writer | [agents/strategy-executive/board-report-writer.md](agents/strategy-executive/board-report-writer.md) |

---

## Learning & Development

| # | Status | Agent | File |
|---|--------|-------|------|
| 32 | ✅ | Training Needs Analyser | [agents/learning-development/training-needs-analyser.md](agents/learning-development/training-needs-analyser.md) |
| 33 | ✅ | Learning Objective Writer | [agents/learning-development/learning-objective-writer.md](agents/learning-development/learning-objective-writer.md) |
| 34 | ✅ | Course Outline Builder | [agents/learning-development/course-outline-builder.md](agents/learning-development/course-outline-builder.md) |
| 35 | ✅ | Assessment Question Writer | [agents/learning-development/assessment-question-writer.md](agents/learning-development/assessment-question-writer.md) |

---

## ESG & Sustainability

| # | Status | Agent | File |
|---|--------|-------|------|
| 36 | ✅ | ESG Report Section Writer | [agents/esg/esg-report-section-writer.md](agents/esg/esg-report-section-writer.md) |
| 37 | ✅ | Carbon Footprint Narrative Writer | [agents/esg/carbon-footprint-narrative-writer.md](agents/esg/carbon-footprint-narrative-writer.md) |
| 38 | ✅ | Materiality Assessment Writer | [agents/esg/materiality-assessment-writer.md](agents/esg/materiality-assessment-writer.md) |
| 39 | ✅ | ESG Commitment Tracker | [agents/esg/esg-commitment-tracker.md](agents/esg/esg-commitment-tracker.md) |

---

## IT & Digital

| # | Status | Agent | File |
|---|--------|-------|------|
| 18 | ✅ | Incident Report Writer | [agents/it-ops/incident-report-writer.md](agents/it-ops/incident-report-writer.md) |
| 19 | ✅ | Change Request Writer | [agents/it-ops/change-request-writer.md](agents/it-ops/change-request-writer.md) |
| 56 | 🟢 | IT Request Scoper | Helps non-technical staff write clear IT service requests and business cases. |
| 57 | 🟢 | Runbook Writer | Converts bullet-point operational procedures into structured runbooks: trigger, prerequisites, steps, verification, rollback, escalation contacts. |
| 58 | 🟢 | Security Risk Communicator | Translates technical security findings (vulnerability scans, pen test results, audit findings) into plain-language risk summaries for non-security leadership. |

---

## Customer Success

| # | Status | Agent | File |
|---|--------|-------|------|
| 20 | ✅ | Escalation Handler | [agents/customer-success/escalation-handler.md](agents/customer-success/escalation-handler.md) |
| 21 | ✅ | Customer Response Writer | [agents/customer-success/customer-response-writer.md](agents/customer-success/customer-response-writer.md) |

---

## Commercial & Legal

| # | Status | Agent | File |
|---|--------|-------|------|
| — | 🟢 | Tender Response Writer | Structures technical and commercial responses to ITBs and RFPs: executive summary, compliance matrix, technical approach, team credentials, clarification log. |
| — | 🟢 | Change Order Assistant | Structures scope change requests: change description, contractual basis, schedule impact, cost impact, required approvals. |
| — | 🟢 | Claims Register Manager | Logs and tracks contractual claims: description, contractual basis, value, evidence required, status, response deadline. |
| — | 🟢 | Back-Charge Drafter | Writes formal back-charge notices: event description, contractual reference, value, supporting evidence required, response deadline. |
| — | 🟢 | NDA & Agreement Summariser | Summarises key clauses from NDAs and service contracts: obligations, restrictions, term, liability cap, termination rights. |
| — | 🟢 | Compliance Checklist Builder | Converts a regulation or policy into a structured compliance checklist: requirement, evidence needed, owner, status. |
| — | 🟢 | Contract Language Simplifier | Rewrites dense contractual clauses into plain language for non-legal readers. Preserves meaning, flags ambiguity, never gives legal advice. |
| — | 🟢 | Policy Summariser | Converts long policy documents into: what it covers, what you must do, what is prohibited, who to contact. |
| — | 🟢 | Incident Communication Drafter | Drafts internal and external communications for incidents, outages, or crises. Separate templates for staff, clients, and press. |

---

## Industry Packs

| # | Status | Pack | File |
|---|--------|------|------|
| — | ✅ | EPC & Energy (13 agents) | [agents/industry/epc-energy/README.md](agents/industry/epc-energy/README.md) |
| — | 🟡 | Healthcare | Planned — patient communications, clinical briefings, care pathway summaries |
| — | 🟡 | Legal | Planned — legal matter summaries, case briefings |
| — | 🟡 | NGO / Public Sector | Planned — grant applications, public consultations, policy responses |

---

## Advanced / MCP-Enabled

> These agents require platform connections beyond plain instructions. Build after the instruction-only library is stable.

| # | Status | Agent | Requires | Description |
|---|--------|-------|----------|-------------|
| 59 | 🔴 | SharePoint Knowledge Agent | SharePoint via Graph | Answers questions grounded in a connected SharePoint site. Cites source document and section for every answer. |
| 60 | 🔴 | Email Triage Assistant | Outlook via Graph API | Classifies, summarises, and drafts responses to unread emails by urgency and type. Never sends without explicit confirmation. |
| 61 | 🔴 | Meeting Intelligence Agent | Teams transcripts via Graph | Automatically produces structured records (decisions, actions, risks) from Teams meeting transcripts. |
| 62 | 🔴 | Cross-Agent Orchestrator | All agents in library | Routes user requests to the correct specialist agent based on intent. Single entry point that delegates to any agent in the library. |

---

## Totals

| Status | Count |
|--------|-------|
| Built ✅ | 39 |
| Planned 🟢🔵🟡 | 28 |
| Advanced / MCP 🔴 | 4 |
| **Total roadmap** | **71** |

---

*Last updated: 2026-03-24*
