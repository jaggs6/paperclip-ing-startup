# Example: B2B SaaS at Stage 1

A worked example of [`AGENTS.md`](../AGENTS.md) for a small B2B SaaS — a Linear-style issue tracker for legal teams — that just landed its first paying customer.

---

## Company

- **Mission:** Reach $50k MRR in 12 months by building a focused issue tracker for in-house legal teams.
- **Board:** Two human co-founders.
- **Total monthly budget cap:** $1,500.

## Active Stage

**Stage 1 — Validation.** First paying customer signed last week ($400/mo). Researcher agent activated.

## Active Agents

### CEO
- **Runtime:** Claude Code, scheduled run every 6h.
- **Monthly budget:** 22% of cap → $330.
- **This week's focus:**
  - Cut the 90-day plan from 14 goals to 5.
  - Review every outbound email Operator sends to the new paying customer.
  - Decide whether the next hire is a second customer interview push or a Growth experiment.

### Builder
- **Runtime:** Claude Code with repo write access.
- **Monthly budget:** 48% of cap → $720.
- **This week's focus:**
  - Ship SAML SSO (blocking enterprise pilot #2).
  - Set up error monitoring (Sentry) — currently flying blind.
  - Decision log entry: chose Postgres over DynamoDB; revisit at Stage 2.

### Operator
- **Runtime:** Claude with inbox + CMS tools.
- **Monthly budget:** 15% of cap → $225.
- **This week's focus:**
  - Reply to 3 inbound demo requests within 24h.
  - Publish one post: "Why we built this for legal, not engineering."
  - Hand-off summary of customer signals to CEO every Friday.

### Researcher *(newly activated)*
- **Runtime:** Claude with web research + scheduling tools.
- **Monthly budget:** 10% of cap → $150. Stage 1 reserve (5% → $75) is held back for one-off tools.
- **30-day success metric:** 20 interviews completed, insights doc updated weekly, 3 pivot signals flagged or explicitly ruled out.
- **First focus:** Interview the 12 trial accounts that didn't convert. Find the single biggest objection.

## Live Approval Gates

- Builder needs CEO sign-off before turning on a paid Sentry plan ($210/mo recurring — over the 2%-of-cap = $30 threshold for recurring infra).
- Operator needs CEO sign-off on the refund request from trial account #7 ($120 — over the 1%-of-cap = $15 refund threshold).
- CEO needs Board sign-off on the verbal partnership offer from a legal-ops consultancy.

## Next Promotion Trigger

Splitting Builder → Engineer + Designer triggers at **$10k MRR or 50 paying users**. Currently at $400 MRR / 1 paying user. Not close.
