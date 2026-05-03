# Example: Solo Indie Consumer App at Stage 0

A worked example of [`AGENTS.md`](../AGENTS.md) for a one-person founder building a consumer app — a habit tracker with a focus on streaks for couples — pre-revenue.

---

## Company

- **Mission:** Validate whether couples will pay $5/mo for a shared habit-tracking app. Decide go/no-go in 90 days.
- **Board:** One human (the founder).
- **Total monthly budget cap:** $400.

## Active Stage

**Stage 0 — Founding.** No revenue yet. TestFlight beta with 22 users.

## Active Agents

### CEO
- **Runtime:** Claude Code, every 6h.
- **Monthly budget:** $100 (lower than template — solo founder, less delegation overhead).
- **This week's focus:**
  - Pick the single metric that decides go/no-go at day 90 (current candidate: % of beta couples still active in week 4).
  - Weekly Friday self-review: what did Builder ship, what did Operator hear from users.

### Builder
- **Runtime:** Claude Code + Xcode.
- **Monthly budget:** $200.
- **This week's focus:**
  - Ship streak-recovery flow (top complaint from beta).
  - Wire up RevenueCat so the paywall is ready the day Stage 1 trigger fires.
  - Cut 2 features from the roadmap that don't serve the 90-day decision.

### Operator
- **Runtime:** Claude with inbox + Notion.
- **Monthly budget:** $80.
- **This week's focus:**
  - Reply to TestFlight feedback within 24h (currently 13 unread).
  - Draft 1 short post for IndieHackers about the couples-niche thesis.
  - Log every churn reason from beta drop-offs into a single spreadsheet.

## Notable Deviations from the Template

- **No Researcher agent yet.** Stage 1 trigger (first paying customer) hasn't fired. Founder is doing interviews directly during beta — this is allowed under "Generalists first."
- **Lowered budgets.** Solo founder, smaller cap. Template defaults assume a small team behind the agents.
- **Heartbeats stretched.** Operator runs every 8h instead of 4h — inbound volume is low enough.

## Live Approval Gates

- Builder flagged a $25/mo Mixpanel add-on. Under the $200/mo threshold → Builder can proceed without CEO sign-off, but logs it in the decision log.
- Operator wants to offer a 1-month free extension to the 5 most active beta couples. No financial impact (no paywall yet) → no gate triggered.

## Next Promotion Trigger

Activating Researcher agent triggers at **first paying customer**. Founder is targeting end of month for paywall flip.
