# Hi, I'm Johel

**Operations professional turned AI workflow builder.**

For 6+ years I worked inside the workflows that AI is now changing: leave and Workers' Compensation
cases, compensation tickets, payroll cutoffs and QA scores for US companies. Today I design and ship AI
workflows for those same kinds of teams, by directing AI coding agents with specs, tests and human
approval gates.

San Jose, Costa Rica · English (C1) / Spanish (native) · [LinkedIn](https://www.linkedin.com/in/johelgomez)

## Highlights

- Built a custom GPT that turned raw QA reports into outliers, pain points and 1:1 action plans for my
  team. Four other supervisors adopted it.
- Built and sold a WhatsApp follow-up automation for a nutrition clinic that replaced a manual daily
  task and runs unattended in production.
- Built a leave policy assistant with RAG, an AI agent and three privacy layers that passes 15/15 on its
  evaluation set.
- In operations: 120+ leave and Workers' Compensation cases per week, 15–25 compensation cases per day
  with a 99% QA score, and team QA raised from 75% to 92% as a Team Lead.

## Featured projects

### [fmla-rag](https://github.com/xJDevs/fmla-rag): Leave Policy Assistant

A document-grounded assistant that answers employee questions about FMLA and a (fictional) company
leave policy.

- **How it works:** an n8n AI Agent searches the documents through Supabase pgvector with Gemini
  embeddings, and every answer cites the document, section and page.
- **Guardrails:** personal data is masked with regex and Microsoft Presidio before the model sees it,
  replies are re-checked, the chat fails closed if masking is down, no conversations are stored, and
  legal or individual cases go to HR.
- **Proof:** 15/15 on a 15-question evaluation set (policy questions, out-of-scope escalation and
  personal data), plus 33 unit tests.

### [cv-factory](https://github.com/xJDevs/cv-factory): AI job-search pipeline

An AI-agent workflow that turns a verified career history into tailored, ATS-safe CVs.

- **How it works:** a Notion career inventory where every achievement is confirmed; for each job,
  eligibility and ghost-job checks, a requirement-by-requirement fit score and gap questions asked one
  at a time. An optional finder searches job sources twice a day.
- **Guardrails:** it refuses to build a CV if any sentence lacks a verified source, and it never
  applies, creates accounts or contacts anyone.
- **Proof:** no CV ships unless it passes 9 automated tests, including four PDF readers, an
  open-source resume parser and two zero-context AI agents.

### [fabrik](https://github.com/xJDevs/fabrik): Project factory for AI coding agents

Decide what to build, then assemble a repo whose rules are enforced, not just written down.

- **How it works:** the agent and I discuss the idea, it researches my Notion knowledge base of tools
  and the web, and then it assembles a ready-to-build repo sized to one of three levels.
- **Guardrails:** every rule names the gate that checks it, dangerous agent commands are blocked, and
  pushes and pull requests wait for my approval.
- **Proof:** a script plants 42 rule violations and confirms each one is caught.

### [n8n-followup-bot](https://github.com/xJDevs/n8n-followup-bot): WhatsApp follow-up bot

A follow-up bot for a nutrition clinic, built so a patient never gets a duplicate message. Sanitized
export of a real client project.

- **How it works:** a daily n8n workflow finds the patients due for a follow-up and sends approved
  WhatsApp templates.
- **Guardrails:** health checks before any send, an atomic deduplication key in Postgres, no automatic
  retries, delivery confirmed only by a signed webhook, alerts to a human when anything is unclear, and
  daily backups to Backblaze B2.
- **Proof:** 10 workflows, 17 behavior rules checked by a validator, and 11 mutation tests.

## How I work

| Step | Who |
|---|---|
| 1. Business problem | with the process owner |
| 2. Spec and tickets | Claude Opus |
| 3. Implementation | Gemini Flash |
| 4. Review | Claude Sonnet agent |
| 5. Adversarial review | OpenAI Codex |
| 6. Tests and evals | |
| 7. My approval | commit and push |

- **Start from the business problem.** I've lived these workflows, so I start with the people who own
  the process, then automate.
- **Spec first.** Spec-driven development with TDD and BDD. Each model does the job it's best and
  cheapest at.
- **Guardrails by default.** Human approval before commits and pushes, personal-data masking,
  fail-closed behavior and evaluation sets before anything ships.
- **Honest about the tools.** I don't write code from scratch. I direct AI coding agents, then read,
  review and test what they produce.

## Toolbox

- **AI and automation:** n8n (AI Agent node) · Claude Code (skills, hooks, subagents) · Gemini API ·
  Custom GPTs · Microsoft Presidio
- **Data and infrastructure:** Supabase (Postgres, pgvector) · Docker · Oracle Cloud with Terraform ·
  VPS hosting · Backblaze B2
- **Practices:** Spec-driven development · TDD and BDD · Git · Vitest · Playwright
- **Languages (with AI):** TypeScript · JavaScript · Python · SQL
- **Business systems I've worked in:** Workday · ServiceNow · Salesforce · ADP · Kronos · Epic

## Background

| Years | Role |
|---|---|
| 2026 – today | Freelance automation developer |
| 2025 – today | Workers' Compensation Case Manager, Amazon |
| 2025 | HR Services Specialist, Compensation & Rewards, Auxis |
| 2023 – 2025 | Customer Service Rep → Team Coach → Team Lead, Health Prime International |
| 2020 – 2023 | Workers' Compensation & Leave of Absence Case Manager, Amazon |
| 2019 – 2020 | Customer service, SmileDirectClub and Concentrix (Humana Pharmacy) |

**Studying:** Software Application Development Technician, Instituto Tecnológico de Costa Rica.

## Currently

- Open to AI workflow, AI automation and AI enablement roles, remote from Costa Rica.
- Preparing for the AWS Certified AI Practitioner exam.
