# Contributing to Awesome Copilot Studio Agents

Contributions are welcome. New agents, improvements to existing instructions, bug fixes, and translations all help.

> **Full authoring standards:** See [AUTHORING-CHECKLIST.md](AUTHORING-CHECKLIST.md) for the complete checklist — file structure, frontmatter fields, instruction block requirements, RAI review, testing protocol, and the 10 most common authoring failures.

---

## What Makes a Good Agent

Every agent in this library must meet the same quality bar:

- **Specific role** — the agent does one thing well, not ten things adequately
- **Clear input/output contract** — the instruction set defines what the agent accepts and exactly what it produces
- **Formal professional language** — British English default, French support, no AI-sounding vocabulary
- **Banned vocabulary list** — explicit list of words that make output sound AI-generated
- **Quality self-check** — a checklist the agent runs internally before every response
- **Edge cases handled** — the instruction set addresses what happens with incomplete input, ambiguous requests, and out-of-scope tasks
- **Within the 8,000-character limit** — Copilot Studio instruction fields have an 8,000-character cap. Instructions must fit.

---

## Agent File Structure

Each agent lives in a single `.md` file. Use this template:

```markdown
# [Agent Name]

> **Description:** [One sentence — what it does]

---
name: [Agent Name]
description: [Full description — 1-2 sentences. Used as the Copilot Studio agent description.]
domain: [writing-communication | project-management | hr-people | productivity | finance | sales | it-ops | customer-success | strategy-executive | learning-development | esg | industry]
vertical: [n/a | specific vertical]
audience: [Primary audience — comma-separated roles]
knowledge_sources: [None required | Optional — description | Required — description]
language: [EN / EN-FR]
char_count: [~XXXX]
rai_reviewed: [yes | no | pending]
tested: [yes | no]
version: 1.0
last_updated: YYYY-MM-DD
---

## Description

[2-4 sentence prose description of what the agent does, what it produces, and its key rules.]

## Conversation Starters

- `[Concrete, paste-ready example 1]`
- `[Concrete, paste-ready example 2]`
- `[Concrete, paste-ready example 3]`

## Instructions

*(Paste the full block below into the Instructions field in Copilot Studio.)*

\```
[Full instruction set — 7,500–8,000 characters]
\```

## Knowledge Sources

[None required. / Required: [what to connect]. / Optional: [what to connect and why it improves the agent.]]

## Deployment Notes

[Practical notes for the person deploying — customisation points, review requirements, known limitations]

## Changelog

| Version | Date | Change |
|---------|------|--------|
| 1.0 | YYYY-MM-DD | Initial version |
```

---

## Directory Structure

Place new agents in the most relevant folder:

```
agents/
├── writing-communication/
├── project-management/
├── hr-people/
├── productivity/
├── finance/
├── sales/
├── it-ops/
├── customer-success/
├── strategy-executive/
├── learning-development/
├── esg/
└── industry/
    └── [sector-name]/
```

For a new industry pack, create a folder under `agents/industry/` with a `README.md` describing the pack and individual agent files.

---

## Instruction Writing Guidelines

### Language defaults
Every agent must include this block near the top of its instructions:

```
## LANGUAGE RULES
Default: formal professional English, British spelling.
French: if the user writes in French or requests French output, respond entirely in French.
Bilingual: produce English first, then "--- Version francaise ---", then the full French version.
```

### Banned vocabulary
Every agent must include a banned vocabulary list. At minimum, include:

```
pivotal, testament, underscores (emphasis), stands as, evolving landscape, vibrant, groundbreaking,
delve, foster (abstract), leverage (as verb), synergy, robust (abstract), seamless, impactful,
cutting-edge, state-of-the-art, best-in-class, additionally (sentence opener), it is important to note that,
in order to, due to the fact that, going forward (filler), touch base, circle back, low-hanging fruit.
```

### Quality self-check
Every agent must end with a `## QUALITY SELF-CHECK` section — a checklist the agent runs internally before delivering output. The check must not be shown to the user.

### Output format
Every agent must specify exactly what its output looks like — structure, section headings, table formats, length targets. Vague format guidance produces inconsistent outputs.

### What you must not do
Every agent must include an explicit list of things it will not do, specifically things a user might reasonably ask that are outside the agent's remit or that could cause harm.

---

## Submitting

1. Fork the repository.
2. Create a branch: `git checkout -b add/[agent-name]`.
3. Add your agent file in the correct folder.
4. Update the agent directory table in `README.md`.
5. Open a pull request with a short description of what the agent does and who it is for.

---

## What We Do Not Accept

- Agents that require premium Copilot licences or external connectors not noted in the agent file
- Agents with instructions longer than 8,000 characters (they will not work in Copilot Studio)
- Agents with company-specific branding baked into the instruction set (keep them generic — use the `industry/` folder for sector-specific packs)
- Instruction sets that produce legally, medically, or financially authoritative output without a human-review disclaimer
