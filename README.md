# startup — a lean AGENTS.md template for [Paperclip](https://paperclip.ing)

Spin up an AI-run company on Paperclip without staring at a blank screen.

This repo gives you a single source of truth — [`AGENTS.md`](AGENTS.md) — that describes a stage-based org chart (CEO, Builder, Operator → Engineer, Designer, Growth, Support, Sales, …) with budgets, heartbeats, and approval gates already filled in. Edit the placeholders, hand it to Paperclip, and you have a running company.

## Quick start

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
- **Budgets** — every agent has a monthly cap; agents stop when they hit it.
- **Promotion triggers** — explicit metrics that say "split this role now."
- **Demotion rules** — when to pause or merge agents back.

## What's in here

| File | Purpose |
|------|---------|
| [`AGENTS.md`](AGENTS.md) | The template. Edit this. |
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
