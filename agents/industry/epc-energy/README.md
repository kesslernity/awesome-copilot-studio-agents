# Industry Pack: EPC & Energy

> **13 declarative agents for Engineering, Procurement, and Construction projects in the energy sector.**
> Built for the full EPC lifecycle — FEED through Commissioning.
> Default language: formal professional English (British spelling) with full French support (EN/FR).

---

## About This Pack

This is a complete, production-ready agent suite for EPC project teams. It covers the communication, documentation, and project management tasks most frequently required on large-scale energy projects — LNG, downstream petrochemicals, offshore, and energy transition.

Every agent in this pack:
- Defaults to formal British English with full French output support
- Preserves EPC acronyms in both languages (FEED, HAZOP, P&ID, ITB, FAT, IFC, MOC, SIMOPS, PSSR, etc.)
- Includes a built-in quality self-check before every response
- Includes HSE safety guardrails where applicable

---

## Agent Directory

| # | Agent | Domain | Audience | Knowledge |
|---|-------|--------|----------|-----------|
| 01 | [EPC Writer](./agents/epc-writer.md) | Writing & Communication | All Project Staff | None |
| 02 | [EPC Humanizer](./agents/epc-humanizer.md) | Writing & Communication | All Project Staff | None |
| 03 | [EPC Meeting Scribe](./agents/epc-meeting-scribe.md) | Writing & Communication | All Staff / PMs | None |
| 04 | [EPC Translator EN↔FR](./agents/epc-translator.md) | Writing & Communication | All Staff | None |
| 05 | [EPC Status Reporter](./agents/epc-status-reporter.md) | Project & Engineering Docs | PMs / Leadership | Optional: project SharePoint |
| 06 | [EPC Risk Register](./agents/epc-risk-register.md) | Project & Engineering Docs | Project Managers | None |
| 07 | [EPC Document Reviewer](./agents/epc-document-reviewer.md) | Project & Engineering Docs | Engineers / PMs | None |
| 08 | [EPC Lessons Learned](./agents/epc-lessons-learned.md) | Project & Engineering Docs | PMs / Leadership | Optional: LL SharePoint |
| 09 | [EPC Presentation Builder](./agents/epc-presentation-builder.md) | Project & Engineering Docs | Leadership / PMs | None |
| 10 | [EPC Onboarding Guide](./agents/epc-onboarding-guide.md) | HR & Onboarding | New Joiners / HR | Required: HR SharePoint |
| 11 | [EPC Job Description Writer](./agents/epc-job-description-writer.md) | HR & Onboarding | HR / Hiring Managers | None |
| 12 | [EPC Performance Coach](./agents/epc-performance-coach.md) | HR & Onboarding | All Staff / Managers | Optional: competency framework |
| 13 | [EPC Prompt Coach](./agents/epc-prompt-coach.md) | Productivity | All Staff | None |

---

## EPC-Specific Features

### Terminology
All agents preserve standard EPC acronyms in both English and French — no translation, no modification:
`FEED` `EPC` `EPCM` `HSE` `HSSE` `ITB` `RFQ` `RFI` `P&ID` `PFD` `HAZOP` `SIMOPS` `FAT` `SAT` `PSSR` `MOC` `MTO` `IFC` `IFR` `IFA` `AFC` `HAZID` `SIL` `SIS` `PHA` `RAM` `ALARP` `CAPEX` `OPEX` `FID` `NTP` `PMC` `EPCIC`

### HSE Safety Guardrails
Agents touching HSE content include explicit guardrails consistent with the principle: **AI prepares, humans decide.**

The following outputs are never produced by any agent in this pack:
- Permit-to-work, LOTO, confined space entry, hot work permit, working at height authorisation
- Risk assessment sign-off, JSA approval, incident classification or severity determination
- Inspection sign-off, quality hold release, material release, fit-for-purpose determination
- Design approval, IFC approval, NCR disposition

### Project Context
Agents in this pack are calibrated for:
- Project phases: Concept / Pre-FEED / FEED / Detailed Engineering / Procurement / Construction / Pre-Commissioning / Commissioning / Start-Up / Close-Out
- Document types: basis of design, engineering specifications, P&IDs, MDRs, transmittals, ITBs, RFQs, vendor documents, commissioning dossiers, punch lists
- Roles: Project Manager, Project Controls Engineer, Document Controller, Discipline Lead, HSE Manager, Procurement Manager, Construction Manager, Commissioning Engineer

---

## How to Adapt This Pack for Your Organisation

1. **Replace the company description** in EPC Onboarding Guide (Agent 10) with your organisation's actual company information and connect your onboarding SharePoint.
2. **Add your project-specific terminology** to the translator's standard pairs tables in EPC Translator (Agent 04).
3. **Extend the HSE guardrails** in EPC Status Reporter (Agent 05) and EPC Risk Register (Agent 06) if your organisation has additional blocked categories.
4. **Connect knowledge sources** for Agents 05, 08, and 10 where SharePoint libraries are available.

---

## Source Material

This pack was developed for large-scale EPC projects in the energy sector. The instruction sets draw on:
- Standard EPC project management frameworks (PMI, APM)
- OSHA and international HSE standards
- Industry document control conventions (ISO 9001, company-specific numbering schemes)
- Bilingual EN/FR working practices common in international EPC projects

---

## Contributing to This Pack

To contribute new agents to the EPC & Energy pack, follow the standard [contribution guidelines](../../../CONTRIBUTING.md) and place agent files in this directory. EPC-specific contributions should include:
- The relevant EPC acronym preservation rules
- HSE safety guardrail language where applicable
- French language support

---

*EPC & Energy Industry Pack — Part of the Awesome Copilot Studio Agents library*
