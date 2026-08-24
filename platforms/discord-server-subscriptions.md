# Discord Server Subscriptions

Discord's own paid-membership product, sold inside the server it gates.

| Field | Value |
|---|---|
| Website | https://discord.com |
| Pricing page | https://support.discord.com/hc/en-us/articles/5330075836311-Monetization-Terms (Schedule 1) |
| Monthly fee | $0 |
| % of each sale | 10% Platform Fee, all transaction types — charged on the payment *less* taxes, processing and transaction fees, so 9.4% of a gross desktop or browser sale |
| Card processing | 6% on desktop and browser, as a percentage of the gross payment · Discord processes its own payments. iOS App Store 30% (15% on retained auto-renewing subscriptions); Google Play 15% auto-renewing / 30% other — both rows are marked *not currently available*. |
| Fixed per transaction | none published |
| Where the money settles | Discord, then a monthly payout |
| Payout fees | not stated |
| Payout timing / minimum | within 45 days of month end per the terms; the FAQ describes practice as on or before the 15th of the following month. $100 minimum first payout, $25 subsequent. |
| Other fees | store fees on the mobile rows are added to the buyer's price rather than deducted from the seller's |
| Verified | 2026-08-03 · primary · fee bases re-read 2026-08-24 |

All-in on a desktop or browser sale: **15.4%** — 6% off the gross payment, then
10% of the 94% that remains. **Not 16%: the two rates are not on the same
base.** Schedule 1 states the rates but not their bases; the Fees section above
it does. Payment Processing Fees are "calculated as a percentage of the total
payments from a user", while the Platform Fee is a percentage of those payments
"less applicable transaction taxes, Payment Processing Fees, and Transaction
Fees". So 0.06 + 0.10 × 0.94 = 0.154, and on a $10 sale Discord takes $0.60,
then $0.94, leaving the seller **$8.46**.

## Sources
- https://support.discord.com/hc/en-us/articles/5330075836311-Monetization-Terms — retrieved 2026-08-03, effective 2024-06-06 — Schedule 1 sets the 6% payment processing and 10% Platform Fee rows, the 45-day payout window and the $100 / $25 minimums.
- https://support.discord.com/hc/en-us/articles/5330075836311-Monetization-Terms — retrieved 2026-08-24 — the Fees section above Schedule 1, which defines the bases the schedule omits: processing is a percentage of the total payments from a user, the Platform Fee a percentage of those payments less applicable transaction taxes, Payment Processing Fees and Transaction Fees.
- https://creator-support.discord.com/hc/en-us/articles/10424143128343-Creator-Revenue-FAQ — retrieved 2026-08-03 — "Server Subscriptions will not be available outside of the United States."
- https://creator-support.discord.com/hc/en-us/articles/10424143128343-Creator-Revenue-FAQ — retrieved 2026-08-03 — "our implementation with Stripe requires you to create a new, separate account for Discord."

Both Discord URLs return 403 to an automated fetcher. They were read in a browser on 2026-08-03, and the Monetization Terms again on 2026-08-24.

## Notes
- **The "90/10 split" is the Platform Fee alone.** The 6% payment processing sits beside it in the same schedule, and secondary fee guides quote the 10 while dropping the 6 entirely — the larger error, and the reason this row exists.
- **The 10 and the 6 must not be added.** They have different bases, stated in the Fees prose rather than in the rate table: processing is a percentage of the gross payment, the Platform Fee a percentage of what is left after taxes, processing and transaction fees. So the 10% is 9.4% of a sale, the all-in is 15.4%, and "90/10" stays accurate — it is 10% of the remainder. This dataset carried 16% from 2026-08-03 to 2026-08-24; see CHANGELOG.
- Transaction fees are added "as applicable" on top of both, and are not modelled here.
- Discord's 6% is roughly double what every other platform in this table charges to process a card. That is why costs here are computed all-in rather than platform-fee-only — see METHODOLOGY.
- **US only.** The requirement is on the account, not the server: 18 or over, account in good standing, verified email and phone, two-factor authentication, US-based banking information and identification provided to Stripe, and nothing on Stripe's Prohibited and Restricted Businesses list.
- **A new, separate Stripe account is required.** An existing one cannot be connected.
- **No member-count or server-age requirement appears in either document.** The "~100 members / 90-day-old server" figure quoted by secondary guides is not Discord's published requirement.
- Discord may withhold payouts for terms violations, compliance, or anticipated refund volume, and determines refund eligibility at its sole discretion. In the EU and UK, Discord is the reseller of the offering; in the US it acts as the seller's limited payment collection agent.
