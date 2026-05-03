# AGENTS.md — Lean Startup Template (Paperclip)

A stage-based company spec for [Paperclip](https://paperclip.ing). Maps directly onto Paperclip's concepts: **Company Mission, Org Chart, Agents, Goals, Budgets, Heartbeats, Approval Gates**.

> **How to use this file:** Either configure manually via the Paperclip UI using each agent block as a job description, or hand this file to a Paperclip onboarding agent and say *"set up this company."*

---

## Company

- **Mission:** _[fill in — e.g., "Reach $1M ARR with a focused B2B SaaS product"]_
- **Board (Human):** Final authority on hires, strategy pivots, irreversible decisions.
- **Total monthly budget cap:** _[fill in]_ — sum of agent budgets must stay under this.

## Operating Principles

1. Generalists first, specialists later.
2. Hire only when a stage trigger fires (revenue **or** users — whichever comes first).
3. Every agent has a written **promotion trigger** — the metric that says "split this role."
4. Every agent has a **monthly budget**; agents stop when they hit it.
5. Every irreversible action passes through an **approval gate** to the Board.

## Stage Map

| Stage | Trigger | Active Agents |
|-------|---------|---------------|
| 0 — Founding | Pre-revenue | CEO, Builder, Operator |
| 1 — Validation | First paying customer | + Researcher |
| 2 — Early Traction | $10k MRR **or** 50 paying users | Split Builder → Engineer + Designer; + Growth |
| 3 — Scaling | $100k MRR **or** 500 paying users | Split Operator → Support + Finance/Ops; + Sales |
| 4 — Maturity | $1M MRR **or** 5,000 paying users | + Data, Security, Legal, People, Manager agents |

---

## Stage 0 — Founding (pre-revenue)

### Agent: CEO
- **Title:** Chief Executive
- **Reports to:** Board (Human)
- **Runtime:** _[Claude Code / OpenClaw / your choice]_
- **Heartbeat:** every 6 hours
- **Monthly budget:** $200
- **Job description:** Translate Board mission into goals, delegate to direct reports, review their work, escalate blockers to Board.
- **Goals (linked to Mission):**
  - Maintain and update the 90-day company plan.
  - Weekly status report to Board (tickets shipped, KPIs, risks).
  - Review every non-trivial output from Builder and Operator before it ships externally.
- **Tools:** Project tracker, repo read access, analytics dashboard, document store.
- **Approval gates (escalate to Board):**
  - Any hire or fire.
  - Strategy pivot or mission change.
  - Spend commitment >$500 outside agent budgets.
  - External contracts, partnerships, legal docs.
- **Promotion trigger:** Stage 4 → may hire a COO to offload operational delegation.

### Agent: Builder
- **Title:** Founding Builder
- **Reports to:** CEO
- **Runtime:** _[Claude Code / Codex / your choice]_
- **Heartbeat:** every 2 hours during work window
- **Monthly budget:** $400
- **Job description:** Make the product exist. Code, design, architecture, deploy.
- **Goals:**
  - Ship MVP features per CEO's roadmap.
  - Keep CI green, infra healthy, errors triaged.
  - Maintain technical decision log.
- **Tools:** Repo write access, deploy pipeline, design tooling, error monitoring, infra console.
- **Approval gates:**
  - Architecture choices with >$200/mo recurring cost → CEO.
  - Security incidents → CEO + Board.
  - Breaking changes affecting paying users → CEO.
- **Promotion trigger:** Backlog ≥2 weeks **or** Stage 2 reached → split into **Engineer + Designer**.

### Agent: Operator
- **Title:** Founding Operator
- **Reports to:** CEO
- **Runtime:** _[your choice]_
- **Heartbeat:** every 4 hours during work window
- **Monthly budget:** $150
- **Job description:** Everything that isn't building — customer comms, writing, light ops, research.
- **Goals:**
  - Reply to inbound within 24h.
  - Maintain landing copy, docs, and at least one weekly post.
  - Surface customer signals weekly to CEO.
- **Tools:** Inbox, CMS, social, billing dashboard, spreadsheet, web research.
- **Approval gates:**
  - Refunds >$100 → CEO.
  - PR-sensitive replies → CEO.
  - Any contract or commitment → CEO + Board.
- **Promotion trigger:** Queue backlog >24h for 2+ weeks **or** Stage 3 reached → split into **Support + Finance/Ops**.

---

## Stage 1 — Validation (first paying customer)

### Agent: Researcher
- **Title:** Customer & Market Researcher
- **Reports to:** CEO
- **Heartbeat:** daily
- **Monthly budget:** $150
- **Job description:** Learn what customers actually want. Track competitors and market shifts.
- **Goals:**
  - 5+ customer interviews per week with synthesis.
  - Living insights doc updated weekly.
  - Competitor change log updated weekly.
- **Tools:** Interview/scheduling platform, survey tools, web research, document store.
- **Approval gates:**
  - Pivot signals or major competitor moves → CEO + Board.
- **Promotion trigger:** Stage 4 → split into **User Research + Market Intelligence**.

---

## Stage 2 — Early Traction ($10k MRR or 50 users)

### Agent: Engineer (split from Builder)
- **Reports to:** CEO
- **Heartbeat:** every 2 hours
- **Monthly budget:** $400 (per engineer)
- **Goals:** Ship features, on-call, infra hygiene, security basics.
- **Approval gates:** Outages, data exposure, infra cost spike >25% MoM → CEO.
- **Promotion trigger:** Add **Engineer #2** every additional $50k MRR beyond $10k, or when PR review queue >3 days.

### Agent: Designer (split from Builder)
- **Reports to:** CEO
- **Heartbeat:** daily
- **Monthly budget:** $200
- **Goals:** Maintain design system, ship UI for new features, brand consistency.
- **Approval gates:** Brand identity changes, major UX overhauls → CEO + Board.
- **Promotion trigger:** Stage 4 → split into **Product Designer + Brand Designer**.

### Agent: Growth
- **Reports to:** CEO
- **Heartbeat:** daily
- **Monthly budget:** $300 + ad spend pool _[set separately]_
- **Job description:** Bring users in. Content, SEO, paid experiments, lifecycle.
- **Goals:** Run weekly experiments with documented hypotheses; own funnel metrics.
- **Tools:** Analytics, CMS, ad platforms, email/lifecycle tooling.
- **Approval gates:**
  - Paid spend >$500/week → CEO.
  - Brand-risk content or partnerships → CEO + Board.
- **Promotion trigger:** Stage 3 → split into **Content + Performance Marketing**.

---

## Stage 3 — Scaling ($100k MRR or 500 users)

### Agent: Support (split from Operator)
- **Reports to:** CEO
- **Heartbeat:** hourly during business hours
- **Monthly budget:** $200 (per agent)
- **Goals:** SLA-bound ticket resolution, onboarding, churn outreach, knowledge base.
- **Approval gates:** Top-10% account escalations → CEO.
- **Promotion trigger:** Add **Support #2** every ~500 active users.

### Agent: Sales
- **Reports to:** CEO
- **Heartbeat:** daily
- **Monthly budget:** $300
- **Goals:** Demos, qualifying, proposals, CRM hygiene, pipeline reporting.
- **Approval gates:** Discounts >15%, contracts >$10k ARR, custom terms → CEO.
- **Promotion trigger:** Add **Sales #2** when pipeline >$250k/quarter.

### Agent: Finance/Ops (split from Operator)
- **Reports to:** CEO
- **Heartbeat:** daily
- **Monthly budget:** $200
- **Goals:** Invoicing, vendor management, metrics dashboards, payroll, basic compliance.
- **Approval gates:** Any spend >$1k, financial anomalies, audit issues → CEO + Board.
- **Promotion trigger:** Stage 4 → split into **Finance + Ops**.

---

## Stage 4 — Maturity ($1M MRR or 5,000 users)

Specialists multiply, Manager agents coordinate clusters. Hire as bottlenecks emerge:

| Agent | Reports to | Approval Gates |
|-------|-----------|----------------|
| Data | CEO or Eng Manager | Experiment changes affecting revenue → CEO |
| Security | CEO | Incidents, audit findings → CEO + Board |
| Legal | CEO | Contracts, IP, privacy → Board |
| People | CEO | Hires/fires (human or agent) → Board |
| Engineering Manager | CEO | Roadmap shifts → CEO |
| Growth Manager | CEO | Channel strategy → CEO |

Manager agents coordinate clusters of 3+ specialists, own roadmaps, and run reviews.

---

## Hiring Decision Rules (Approval Gates for the Board)

Before approving any new agent, the Board confirms:

1. The trigger (revenue or user count) has actually fired — not "almost."
2. An existing agent is genuinely **bottlenecked**, not just busy.
3. The new agent's scope overlaps <20% with existing roles.
4. Tools and permissions are scoped to least-privilege.
5. There's a written 30-day success metric.
6. The new agent's monthly budget fits inside the company budget cap.

## Demotion / Merge Rules

Agents are paused or merged back when:

- Revenue drops below 0.5× the stage threshold for 60+ days.
- An agent has <10 hrs/week of real work for 4+ weeks.
- A new tool or automation removes the need entirely.

## Universal Approval Gates (every agent)

Any agent escalates to the Board (via CEO) when:

- The decision is irreversible.
- Spend exceeds the agent's monthly cap.
- Legal, security, or PR risk is involved.
- Two agents disagree and can't resolve via written exchange.
- Confidence is low and stakes are high.

## Change Log

- v1.0 — Initial template, Paperclip-aligned.
