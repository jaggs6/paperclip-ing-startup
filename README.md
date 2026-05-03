# startup — a lean AGENTS.md template for [Paperclip](https://paperclip.ing)

Spin up an AI-run company on Paperclip without staring at a blank screen.

This repo gives you a single source of truth — [`AGENTS.md`](AGENTS.md) — that describes a stage-based org chart (CEO, Builder, Operator → Engineer, Designer, Growth, Support, Sales, …) with budgets, heartbeats, and approval gates already filled in. Edit the placeholders, hand it to Paperclip, and you have a running company.

## Quick start (with an LLM — recommended)

Open ChatGPT, Claude, or any LLM that can fetch URLs. Paste this prompt:

```
You are helping me bootstrap an AI-run company on Paperclip (https://paperclip.ing).

Read these two files first:
- https://raw.githubusercontent.com/jaggs6/paperclip-ing-startup/main/AGENTS.md
- https://raw.githubusercontent.com/jaggs6/paperclip-ing-startup/main/prompts/onboarding.md

Then follow the interview script in onboarding.md exactly:
- Ask me ONE question at a time, in order.
- Default aggressively when I don't know.
- When you have enough answers, output a complete filled-in AGENTS.md
  for my company (strip stages above my current one, compute $ alongside %,
  bias each agent's first-week goals toward my biggest constraint).

Start with question 1.
```

The LLM will interview you and hand back a ready-to-paste `AGENTS.md`. Drop it into [paperclip.ing](https://paperclip.ing) and you're running.

## Quick start (manual)

1. **Fork or download** this repo.
2. Open [`AGENTS.md`](AGENTS.md) and fill in the four placeholders at the top:
   - Mission
   - Total monthly budget cap
   - Runtime choices for each agent
   - Anything else in `_[brackets]_`
3. **Configure Paperclip** one of two ways:
   - **Manual:** open [paperclip.ing](https://paperclip.ing), create each agent using the matching block as the job description.
   - **Automated:** paste `AGENTS.md` into a Paperclip onboarding agent and say *"set up this company."*
4. As you hit a stage trigger ($10k MRR, 50 users, etc.), open `AGENTS.md`, follow the **Promotion trigger** lines, and split roles.

## Why this template

Most "AI-native company" guides skip the boring parts: who reports to whom, what each agent is *not* allowed to do, when to hire the next role. This template encodes:

- **Stage gates** — you don't hire a Sales agent at $0 MRR.
- **Approval gates** — irreversible actions always escalate to the human Board.
- **Budgets** — every agent gets a **%-of-cap allocation** (not a hardcoded dollar amount), so the same template works whether your monthly cap is $400 or $40,000. Per-stage allocations sum to ≤100%.
- **Promotion triggers** — explicit metrics that say "split this role now."
- **Demotion rules** — when to pause or merge agents back.

## What's in here

| File | Purpose |
|------|---------|
| [`AGENTS.md`](AGENTS.md) | The template. Edit this. |
| [`llms.txt`](llms.txt) | Sitemap for LLMs reading this repo (per [llmstxt.org](https://llmstxt.org)). |
| [`prompts/onboarding.md`](prompts/onboarding.md) | Interview script — paste into ChatGPT/Claude with your codebase and it'll walk you through filling out `AGENTS.md`. |
| [`examples/b2b-saas.md`](examples/b2b-saas.md) | Filled-in example for a B2B SaaS at Stage 1. |
| [`examples/indie-app.md`](examples/indie-app.md) | Filled-in example for a solo indie consumer app. |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to propose changes. |
| [`LICENSE`](LICENSE) | MIT. |

## Contributing

PRs welcome — especially:

- New filled-in examples (marketplaces, dev tools, agencies, content businesses).
- Better promotion/demotion heuristics from real Paperclip operators.
- Tool/runtime suggestions per agent role.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[MIT](LICENSE). Use it, fork it, sell what you build with it.
