# flatpass

A paid-access layer for Discord, metered on active paid members. Maintains this dataset.

| Field | Value |
|---|---|
| Website | https://flatpass.io |
| Pricing page | https://flatpass.io/pricing |
| Monthly fee | Free $0 up to 15 paid members · Starter $29 up to 80 · Growth $79 up to 200 · Scale $149 up to 750 · Max $399 uncapped |
| % of each sale | 0% at every rung |
| Card processing | Stripe's rate on the seller's own connected account — additional. US 2.9% + $0.30. |
| Fixed per transaction | Stripe's fixed fee (US $0.30) |
| Where the money settles | the seller's own Stripe account (Stripe Connect direct charges) |
| Payout fees | none charged by flatpass; Stripe's payout terms apply |
| Payout timing / minimum | not stated; set by the seller's own Stripe account |
| Other fees | none |
| Verified | 2026-08-23 · primary |

The meter is **active paid members**, not sales volume and not Discord headcount.

## Sources
- https://flatpass.io/pricing — retrieved 2026-08-23 — "0% of your revenue — the only meter is active paid members."
- https://flatpass.io/pricing — retrieved 2026-08-23 — "And past $1,036 a month in sales, it's also cheaper — permanently."
- https://flatpass.io/pricing — retrieved 2026-08-23 — on annual billing: "No — every tier is billed monthly, and you can cancel anytime."

## Notes
- **Discord only.** No Telegram, no Slack.
- **No annual platform plan.** Every tier is billed monthly.
- Payments are Stripe Connect direct charges on the seller's connected account, so processing is billed to that account at its own country's Stripe pricing — not at a rate flatpass sets.

## Where flatpass is the more expensive option

Two cases, both from the numbers in this repo.

**Whop is cheaper all-in below about $1,036/month in sales.** Whop's all-in is 5.7% + $0.30; flatpass's Starter rung is $29 plus the seller's own Stripe 2.9% + $0.30. The fixed fee cancels, so the crossover is $29 ÷ (5.7% − 2.9%) = $29 ÷ 2.8% ≈ $1,036/month. Between the sixteenth paid member and that volume — roughly 16 to 29 paid members at a modelled $35 average membership price — Whop costs the seller less. Below 16 paid members flatpass's Free tier is $0 and the comparison goes the other way.

**Subscord is cheaper at 81–500 active subscriptions, and above 750.** Subscord meters the same thing flatpass does, so the ladders compare directly: Subscord's $65 for up to 500 active subscribers beats flatpass's $79 (up to 200) and $149 (up to 750), and Subscord's $199 uncapped beats flatpass's $399. flatpass is cheaper below 81 and in the 501–750 band.
