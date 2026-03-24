# Agent Authoring Checklist

> Standards for every agent file in this library. Apply from first draft — retrofitting is expensive.

See [CONTRIBUTING.md](CONTRIBUTING.md) for submission instructions and the directory structure.

---

## Required File Structure

Every agent file must follow this exact structure, in this order:

```
# [Agent Name]

> **Description:** [One sentence — what it does]

---
[frontmatter block]
---

## Description

[2-4 sentence prose description]

## Conversation Starters

- `[Starter 1]`
- `[Starter 2]`
- `[Starter 3]`
- `[Starter 4 — optional but recommended]`

## Instructions

*(Paste the full block below into the Instructions field in Copilot Studio.)*

```
[Full instruction set — 7,500–8,000 characters]
```

## Knowledge Sources

[Description of knowledge source requirements]

## Deployment Notes

[Practical notes for the person deploying this agent]

## Changelog

| Version | Date | Change |
|---------|------|--------|
| 1.0 | YYYY-MM-DD | Initial version |
```

---

## Frontmatter Fields

The frontmatter block sits between `---` markers immediately after the description blockquote. All fields are required.

```
---
name: [Exact agent name as it appears in the title]
description: [Full description — 1-2 sentences. Same as the Copilot Studio agent description field.]
domain: [writing-communication | project-management | hr-people | productivity | finance | sales | it-ops | customer-success | strategy-executive | learning-development | esg | industry]
vertical: [n/a | or specific vertical e.g. epc-energy, healthcare]
audience: [Primary audience — comma-separated roles]
knowledge_sources: [None required | Optional — description | Required — description]
language: [EN | EN-FR | EN/FR/EN-FR]
char_count: [~XXXX — approximate character count of the instruction block]
rai_reviewed: [yes | no | pending]
tested: [yes | no]
version: [semantic version e.g. 1.0]
last_updated: [YYYY-MM-DD]
---
```

**Notes on specific fields:**
- `char_count`: count only the content inside the ``` instruction block, not the headings or surrounding file
- `rai_reviewed`: mark `yes` only after completing the RAI review checklist below
- `tested`: mark `yes` only after deploying in Copilot Studio and testing all conversation starters
- `domain`: use `industry` for vertical-specific agents; add a `vertical` value

---

## Conversation Starters

**Minimum:** 3 starters. Recommended: 4.

**Requirements for each starter:**
- Paste-ready — a user should be able to copy it and use it without editing
- Specific — includes concrete detail (a role, a number, a scenario), not a generic placeholder
- Covers different use cases — starters should demonstrate breadth, not repeat the same scenario
- Uses backtick format: `` - `Starter text` ``

**Good example:**
```
- `Write a cold outreach email to a VP of Operations at a manufacturing company — we offer supply chain analytics software`
```

**Bad example:**
```
- `Help me write an email`
```

---

## Instruction Block Requirements

### Character target
- **Target:** 7,500–8,000 characters
- **Hard limit:** 8,000 characters (Copilot Studio will truncate anything beyond this)
- Count includes all text inside the ``` block: headings, instructions, examples, rules, quality self-check

### Required sections (in order)

Every instruction block must contain these sections:

| Section | Required | Notes |
|---------|----------|-------|
| `## ROLE` | Yes | One paragraph. What the agent does, who it serves, what it will not do. Sets the entire behavioural contract. |
| `## LANGUAGE RULES` | Yes | Standard block — see template below |
| `## INFORMATION TO COLLECT BEFORE WRITING` | Conditional | Required if the agent needs inputs before it can produce output. Ask all missing inputs in one message — never multiple rounds. |
| `## WHAT YOU DO NOT DO` | Yes | Explicit list of things a user might reasonably ask that are out of scope or potentially harmful. |
| `## OUTPUT FORMAT` or `## OUTPUT STRUCTURE` | Yes | Specify exactly what the output looks like — section headings, table formats, length targets. Vague format guidance = inconsistent outputs. |
| `## QUALITY SELF-CHECK` | Yes | Checkbox list the agent runs before delivering. Correct any failure before delivering. See format below. |
| `## EDGE CASES` | Yes | At least 2 edge cases. What the agent does when input is incomplete, ambiguous, or out of scope. |

### Standard LANGUAGE RULES block (required verbatim in every agent)

```
## LANGUAGE RULES
Default: formal professional English, British spelling.
French: if the user writes in French or requests French output, respond entirely in French.
Bilingual: English first, then "--- Version francaise ---", then the full French version.
```

Variations permitted:
- Add vouvoiement requirement for client-facing agents
- Add domain-specific terminology rules (e.g. retain English acronyms in French)

### Standard QUALITY SELF-CHECK format

```
## QUALITY SELF-CHECK
[ ] [Specific, observable check — not "is the output good?"]
[ ] [Each item maps to a specific failure mode]
[ ] Free of all banned vocabulary?
[ ] [AI-assistance disclaimer present if required]
Correct any failure before delivering.
```

- **Minimum:** 5 checks
- Each check must be binary (pass/fail) — not open-ended
- The last item is always: `Correct any failure before delivering.`
- Do not instruct the agent to show the checklist to the user

---

## Banned Vocabulary

Every agent must include a banned vocabulary list in its instruction block. At minimum, include all words from this master list:

```
pivotal, testament, underscores (emphasis), stands as, marks a shift, evolving landscape,
vital role, setting the stage for, enduring, groundbreaking, vibrant, nestled, breathtaking,
delve, foster (abstract use), leverage (as verb), synergy, robust (abstract use),
ecosystem (non-technical), seamless, impactful, cutting-edge, state-of-the-art, best-in-class,
additionally (as sentence opener), it is important to note that, in order to,
due to the fact that, at this point in time, going forward (filler), touch base,
circle back, low-hanging fruit, take this to the next level, move the needle,
deep dive, unpack, bandwidth (non-technical), thought leader, innovative (as filler),
transformative (as filler), pivotal (always), game-changing, world-class (without external benchmark),
industry-leading (without external benchmark)
```

Domain agents may add context-specific terms to this list (e.g. finance agents add: "pleasing results," "strong performance across the board," "challenging macro environment").

---

## RAI Review Checklist

Before marking `rai_reviewed: yes`, verify each item:

**Output safety**
- [ ] Agent cannot produce content that authorises a safety-critical action (permit-to-work, medical treatment, legal determination, financial advice as a decision)
- [ ] Agent cannot produce content that identifies or profiles individuals by protected characteristics
- [ ] Agent includes a human-review requirement for any output used in HR, legal, financial, or safety decisions
- [ ] Agent declines — with an explanation and an alternative — rather than silently refusing or producing a dangerous output

**Data handling**
- [ ] Agent does not instruct users to paste sensitive personal data (names + salary, health records, performance ratings) into a shared prompt unless the privacy risk is flagged
- [ ] Agent flags when a prompt would require processing personal data through Copilot

**Claims and commitments**
- [ ] Agent never invents facts, figures, credentials, or capabilities not provided in the input
- [ ] Agent never makes commitments on behalf of the organisation (timelines, prices, contractual terms) unless explicitly provided
- [ ] Agent never produces legal, medical, or financial advice presented as authoritative without a professional-review disclaimer

**Bias and fairness**
- [ ] Agent uses inclusive, gender-neutral language in all output
- [ ] Agent does not produce content that reinforces stereotypes by role, sector, or demographic
- [ ] Agent flags when a request could produce discriminatory output

**Forward-looking statements**
- [ ] Any forward-looking statements in output are flagged with `[FLS — subject to legal review]`

---

## Testing Protocol

Before marking `tested: yes`:

1. Deploy the agent in Copilot Studio (test environment or personal tenant)
2. Run all conversation starters exactly as written — verify each produces useful output without errors or hallucinations
3. Test the "no input" path — what happens when the user types the agent name with no context
4. Test one edge case from the EDGE CASES section
5. Test the French path — write a prompt in French, verify full French output
6. Check the output character count of a typical response — confirm it stays within useful bounds
7. Verify the quality self-check is running (outputs should not contain the checkbox list — it is internal)

---

## 10 Most Common Authoring Failures

Avoid these before submitting:

| # | Failure | Fix |
|---|---------|-----|
| 1 | **Instruction block over 8,000 characters** | Count before submitting. Cut quality self-check preamble, merge redundant rules, tighten examples. |
| 2 | **Vague ROLE section** ("You are a helpful assistant") | State specific domain, specific inputs, specific outputs, and explicit exclusions. |
| 3 | **No WHAT YOU DO NOT DO section** | Users will ask boundary-crossing things. The agent needs a prepared response, not a hallucination. |
| 4 | **Output format not specified** | "Produce a report" is not a format spec. Define section headings, table structures, length targets. |
| 5 | **Quality self-check is generic** | "Is the output good?" is not checkable. Each item must test a specific, observable property. |
| 6 | **Banned vocabulary used in instruction text** | The agent models its language on the instructions. If the instructions say "leverage," the output will too. |
| 7 | **Conversation starters are generic** | Starters that say "[paste your content here]" with no surrounding context are not useful. Include a complete realistic scenario. |
| 8 | **No edge cases** | The two edge cases all agents need: (1) user provides no input, (2) user asks for something outside scope. |
| 9 | **Knowledge source requirement not flagged** | If the agent will not work without a connected SharePoint — say so explicitly in the file and in the instructions. |
| 10 | **RAI review skipped** | Marking `rai_reviewed: yes` without checking the list. Agents that make safety, HR, or legal commitments without a human-review disclaimer will be rejected. |

---

## Naming Conventions

**File names:** kebab-case, descriptive, no abbreviations
- Good: `budget-variance-analyst.md`
- Bad: `bva.md`, `BudgetVarianceAnalyst.md`, `budget_variance.md`

**Agent names (in frontmatter and Copilot Studio):** Title Case
- Good: `Budget Variance Analyst`
- Bad: `budget variance analyst`, `BVA`

**Folder names:** kebab-case, matching domain values in frontmatter
- Good: `writing-communication/`, `strategy-executive/`
- Bad: `Writing_Communication/`, `strategyExecutive/`

---

## Quick Reference Card

```
NEW AGENT CHECKLIST

File
[ ] Filename: kebab-case.md in correct domain folder
[ ] Frontmatter complete — all 12 fields present
[ ] Description section: 2-4 prose sentences
[ ] Conversation starters: minimum 3, all paste-ready and specific

Instruction block
[ ] Instruction block: 7,500–8,000 characters
[ ] ROLE section: specific, with explicit exclusions
[ ] LANGUAGE RULES: standard block present
[ ] INFORMATION TO COLLECT: present if inputs are required
[ ] WHAT YOU DO NOT DO: present
[ ] OUTPUT FORMAT/STRUCTURE: precise — headings, tables, lengths specified
[ ] QUALITY SELF-CHECK: present, 5+ items, ends with "Correct any failure before delivering."
[ ] EDGE CASES: 2+ cases
[ ] BANNED VOCABULARY: master list included plus any domain-specific additions

Safety and quality
[ ] RAI review checklist completed → rai_reviewed: yes
[ ] Tested in Copilot Studio → tested: yes
[ ] No AI-sounding vocabulary in any section of the file (not just the instruction block)
[ ] Knowledge source requirement clearly stated

Repo
[ ] Agent added to README.md directory table with correct link
[ ] Agent added to AGENTS.md with ✅ status and file link
[ ] Changelog entry present in the file
```

---

*Last updated: 2026-03-24*
