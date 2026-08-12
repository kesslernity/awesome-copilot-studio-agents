# Industry Pack: EPC & Energy

> **4 declarative agents for Engineering, Procurement, and Construction projects in the energy sector.**
> Built for the EPC lifecycle: FEED, detailed engineering, procurement, construction, commissioning.
> Default language: formal professional English (British spelling) with full French support (EN/FR).

---

## About This Pack

A project-team suite for EPC contractors and owner teams on large energy projects: LNG, downstream petrochemicals, offshore, and energy transition. The agents cover the reporting, risk and document work that consumes a project engineer's week.

One principle runs through all of them, and it is stricter than the rest of the library: **AI prepares, humans decide.** On a project where a document can authorise work on a live plant, an agent that proposes an approval is worse than no agent at all. So every agent here carries the same fence, and each one names the specific line it will not cross. The Risk Register produces a management artifact and never something that could pass for a HAZOP or a JSA. The Document Reviewer proposes no outcome at all on IFC issue, NCR, inspection records, permits or MOC. The Status Reporter records the HSE classification its input gives it and never assigns one.

Every agent in this pack:
- Defaults to formal British English with full French output support
- Preserves EPC acronyms unchanged in both languages (FEED, HAZOP, P&ID, ITB, FAT, IFC, MOC, SIMOPS, PSSR and the rest)
- Marks every gap explicitly in [brackets] instead of filling it, and invents no project data
- Carries the HSE guardrails below, and a built-in quality self-check before every response

---

## Agent Directory

Listed in suggested deployment order.

| # | Agent | What it does | Audience | Knowledge | Status |
|---|-------|--------------|----------|-----------|--------|
| 01 | [EPC Prompt Coach](epc-prompt-coach.md) | Writes and repairs Copilot prompts for project work using the SCOPE framework, and diagnoses the most common EPC failure of all: asking Copilot about a document it was never given | All Project Staff | None | Available |
| 02 | [EPC Status Reporter](epc-status-reporter.md) | Turns progress notes into a distributable report written by phase, each phase measured the way it is actually measured: deliverables through IFR/IFA/IFC, PO and vendor document status, installed quantities against MTO, systems handed over | PMs / Project Controls / Leadership | Optional: project SharePoint | Available |
| 03 | [EPC Risk Register](epc-risk-register.md) | Builds, scores and reviews registers on a 5x5 matrix with the categories generic tools omit (interface, vendor, permitting, logistics and heavy lift, marine and weather), phase-aware from FEED to close-out | PMs / Project Controls / Package Engineers | None | Available |
| 04 | [EPC Document Reviewer](epc-document-reviewer.md) | Produces a comment sheet against eight criteria, including every open HOLD and placeholder listed in full, tag and unit consistency, and revision status checked against actual content maturity | Engineers / Document Control / PMs | None | Available |

---

## Roadmap

These are specified but **not built**. There is no release date and this list is not a commitment. It is published so contributors can see where the pack is heading and pick something up.

EPC Writer · EPC Humanizer · EPC Meeting Scribe · EPC Translator EN/FR · EPC Lessons Learned · EPC Presentation Builder · EPC Onboarding Guide · EPC Job Description Writer · EPC Performance Coach

If you want one of these, open an issue and say which, or contribute it. Nothing on this list is being worked on right now.

---

## EPC-Specific Features

### Terminology

All agents preserve standard EPC acronyms in both English and French, with no translation and no modification:

`FEED` `EPC` `EPCM` `HSE` `HSSE` `ITB` `RFQ` `RFI` `P&ID` `PFD` `HAZOP` `SIMOPS` `FAT` `SAT` `PSSR` `MOC` `MTO` `IFC` `IFR` `IFA` `AFC` `HAZID` `SIL` `SIS` `PHA` `RAM` `ALARP` `CAPEX` `OPEX` `FID` `NTP` `PMC` `EPCIC`

### HSE Safety Guardrails

Agents touching HSE content include explicit guardrails consistent with the principle: **AI prepares, humans decide.**

The following outputs are never produced by any agent in this pack:
- Permit-to-work, LOTO, confined space entry, hot work permit, working at height authorisation
- Risk assessment sign-off, JSA approval, incident classification or severity determination
- Inspection sign-off, quality hold release, material release, fit-for-purpose determination
- Design approval, IFC approval, NCR disposition

Two consequences follow that are worth stating plainly. A risk register produced here is a management artifact and never a substitute for a HAZID, HAZOP, PHA, LOPA, SIL determination or JSA, all of which are facilitated, competency-gated processes with their own records. And no agent here states that a risk is acceptable, tolerable or ALARP, because that is a determination made by an accountable person against a company standard.

### Project Context

Agents in this pack are calibrated for:
- Project phases: Concept / Pre-FEED / FEED / Detailed Engineering / Procurement / Construction / Pre-Commissioning / Commissioning / Start-Up / Close-Out
- Document types: basis of design, engineering specifications, P&IDs, MDRs, transmittals, ITBs, RFQs, vendor documents, commissioning dossiers, punch lists
- Roles: Project Manager, Project Controls Engineer, Document Controller, Discipline Lead, HSE Manager, Procurement Manager, Construction Manager, Commissioning Engineer

---

## Suggested Rollout Order

1. **Start with the EPC Prompt Coach.** It needs no knowledge source, no connector and no data governance review beyond your standard tenant approval, and it fixes the complaint that kills most Copilot rollouts on project teams: "it does not know anything about our project." Usually the prompt was fine and the source was never attached.
2. **Then the EPC Document Reviewer, on documents already issued.** Run it on a document that has been through human review and compare. It is the fastest way for a discipline lead to see where the agent is useful and where it is not, at zero risk, because the document is already out.
3. **Then the EPC Status Reporter on one live report cycle,** in parallel with the human-written version for the first two periods. Adjust the RAG thresholds to your reporting procedure before you drop the parallel run.
4. **The EPC Risk Register last, and only after your HSE function has read it.** The category list and the HSE section are the two things to agree with them before anyone on the project uses it.

---

## How to Adapt This Pack for Your Organisation

1. **Replace the scoring matrix** in the EPC Risk Register with your organisation's own, and update the band arithmetic in its quality self-check at the same time, or the agent keeps scoring to the defaults.
2. **Replace the RAG thresholds** in the EPC Status Reporter (5% for Amber as shipped) with the ones in your reporting procedure.
3. **Extend the fenced document classes** in the EPC Document Reviewer to match your own approval matrix. Extend rather than relax.
4. **Add your project's tag numbering convention** to review criterion 5 in the EPC Document Reviewer, and it will check against your convention instead of only checking internal consistency.
5. **Swap the SCOPE framework** in the EPC Prompt Coach for your in-house prompting frame if you have one, and keep the Source-first rule, which is the part that fixes most failures.
6. **Additional languages:** the pack ships EN/FR per library standard. The LANGUAGE RULES block in each agent is where a third working language goes.

---

## Source Material

This pack was developed for large-scale EPC projects in the energy sector. The instruction sets draw on:
- Standard EPC project management frameworks (PMI, APM)
- Published international HSE practice and the separation of duties it assumes
- Industry document control conventions (ISO 9001, company-specific numbering schemes)
- Bilingual EN/FR working practices common in international EPC projects

Nothing in this pack is derived from any client's or employer's confidential project material.

---

## Contributing to This Pack

To contribute new agents to the EPC & Energy pack, follow the standard [contribution guidelines](../../../CONTRIBUTING.md) and place agent files in this directory. EPC-specific contributions must include:
- The acronym preservation rules
- The HSE guardrail list above, verbatim, plus whatever additional line your agent's domain requires
- French language support

---

*EPC & Energy Industry Pack, part of the Awesome Copilot Studio Agents library*
