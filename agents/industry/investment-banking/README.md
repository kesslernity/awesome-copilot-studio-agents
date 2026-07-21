# Industry Pack: Investment Banking & M&A

> **5 declarative agents for investment banking deal teams — transaction structuring, diligence, and institutional memory.**
> Built for the deal lifecycle: mandate → structuring → diligence → close → precedent.
> Default language: formal professional English (British spelling) with full French support (EN/FR).



https://github.com/user-attachments/assets/e909f6e5-af00-4497-b40c-37d2c0bb956d

*The full build in 100 seconds — also on [YouTube](https://youtu.be/-4QWOGDjj5s) with captions and chapters.*


---

## About This Pack

A deal-team suite for banks and advisory teams running premium Microsoft 365 Copilot, with one Cowork seat recommended for data-room work. One design principle runs through every agent: **the agent's job is retrieval with citations from your own approved sources, not knowing banking regulation.** An agent that "understands the requirements for structuring a transaction" is an agent grounded on the bank's structuring playbooks, credit policy, and precedent deals — it retrieves the applicable requirements and cites the paragraph it got them from. The knowledge stays the bank's, every answer is checkable, and every decision stays human.

Every agent in this pack:
- Puts a **source citation and a confidence grade** on every factual line, and flags gaps explicitly (NOT FOUND / Not stated) instead of filling them
- Quotes documents **verbatim** — no paraphrased clauses, no silent conversions of numbers, currencies, or units
- Labels every output a **draft** with a named human review step
- Includes the banking guardrails below, and a built-in quality self-check before every response
- Defaults to formal British English with full French output support

---

## Agent Directory

| # | Agent | What it does | Knowledge | Runs on | Status |
|---|-------|--------------|-----------|---------|--------|
| 01 | [Deal Requirements Navigator](structuring-requirements-navigator.md) | "What do we need for this transaction" — approvals, documentation set, CPs, compliance checkpoints, as a checklist cited to internal policy | Required: policy/playbook SharePoint | Agent Builder | Available |
| 02 | [CIM & Teaser Digester](cim-teaser-digester.md) | Extract a CIM, teaser, or IM into a referenced dataset with HIGH/MEDIUM/LOW confidence per item; never values the deal | None (attach/paste) | Agent Builder | Available |
| 03 | [Term Sheet Consistency Check](term-sheet-consistency-checker.md) | Flag every deviation between a draft and the approved position, both clauses quoted side by side; judges nothing | Optional: per-deal Notebook | Agent Builder | Available |
| 04 | [Data Room Extraction Sweep](data-room-extraction-sweep.md) | Sweep a data-room folder into a provision tracker with a full coverage report — unread documents listed, never skipped | Required: data-room folder | Agent Builder / **Cowork** for full sweeps | Available |
| 05 | [Deal Precedent Finder](deal-precedent-finder.md) | Retrieve comparable past deals with terms and sources; capture closed deals into the precedent library so the memory compounds | Required: precedent library SharePoint | Agent Builder | Available |

---

## Banking Guardrails

Agents in this pack follow the principle: **AI prepares, humans and committees decide.**

The following outputs are never produced by any agent in this pack:
- Recommendations to approve, decline, price, or pursue a transaction
- Credit decisions, risk ratings, or capital treatment conclusions
- Valuations, fairness or suitability determinations, or investment recommendations
- Regulatory or legal determinations — agents cite what internal policy says, they never interpret regulation directly
- KYC/AML clearance decisions
- Any suggestion to move deal information across a permission or information wall, or to work around blocked access

Two structural safeguards back these up. First, **need-to-know is enforced by permissions, not by the agent**: deal content lives in permission-trimmed SharePoint sites and Notebooks aligned with the insider list, and Copilot cannot show a user what their account cannot open. Second, **gaps are findings**: every agent reports what it could not read, could not access, or could not find — because on deal work, a silent skip is worse than a wrong answer.

---

## Terminology

All agents preserve standard deal and finance acronyms in both English and French — no translation, no modification:
`CIM` `IM` `NDA` `LOI` `SPA` `APA` `SHA` `EBITDA` `EV` `DCF` `CP` `MAC` `MAE` `KYC` `CDD` `AML` `RCF` `LBO` `IPO` `ECM` `DCM` `M&A` `FDD` `VDD` `SPV` `IC`

---

## Suggested Rollout Order

1. **Week 1 — no tenant grounding needed:** deploy the CIM & Teaser Digester and the Term Sheet Consistency Check on one live or recently closed deal. Lowest risk, immediate hours back, and their verbatim-quote outputs are trivially checkable, which is how the team learns to trust the pack.
2. **Weeks 2–4 — build the two libraries:** consolidate structuring playbooks and policies into one SharePoint site and deploy the Deal Requirements Navigator on it; start the precedent library with the last five closed deals (the Precedent Finder's CAPTURE mode drafts those pages from final documents).
3. **In the quarter — the Cowork step:** run the Data Room Extraction Sweep on one diligence workstream with admin spend limits set, and measure one number: analyst hours per diligence workstream, before and after. That number is the business case.

---

## Data Handling and Compliance Notes

- CIMs, data rooms, and term sheets are NDA material and potentially MNPI. Within a work tenant, Microsoft handles prompts and responses under enterprise data protection and does not use them to train foundation models — but the approval to process deal documents through Copilot belongs to the organisation's compliance and information security functions, not to the deploying team. Get it in writing before rollout.
- Publish agents through the organisation's Agent Store ("Built by your org") after admin review; do not sideload for team-wide use.
- No agent in this pack uses web grounding. Internal knowledge sources and attached documents only.
- Cowork jobs are usage-billed: set tenant/group spend limits before the first data-room sweep.

---

## How to Adapt This Pack for Your Organisation

1. **Connect the knowledge sources** — the pack's value scales with the policy library (Agent 01) and the precedent library (Agent 05). The libraries are the asset; the agents are their interface.
2. **Replace the standard provision list** in the Data Room Extraction Sweep with your house diligence checklist.
3. **Decide the precedent library's anonymisation policy** (client names vs codenames) with compliance before the first page is filed.
4. **Add your approval matrix names** (committee names, thresholds) to the Deal Requirements Navigator's collected inputs if your bank routes approvals by named committee.
5. **Additional languages:** the pack ships EN/FR per library standard; the LANGUAGE RULES block in each agent is the place to add a third working language if your desk needs one.

---

## Contributing to This Pack

To contribute new agents to the Investment Banking & M&A pack, follow the standard [contribution guidelines](../../../CONTRIBUTING.md) and place agent files in this directory. Contributions should include:
- The banking guardrails language (the "never produced" list above)
- Citation-plus-confidence output discipline and an explicit gaps section
- French language support with the acronym preservation rules

---

*Investment Banking & M&A Industry Pack — Part of the Awesome Copilot Studio Agents library*
