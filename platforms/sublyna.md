# Sublyna

A paid-access layer for Discord and Telegram communities, on a free percentage tier or a monthly plan with a lower percentage.

| Field | Value |
|---|---|
| Website | https://www.sublyna.com |
| Pricing page | https://www.sublyna.com/pricing |
| Monthly fee | Starter $0 · Creator $29/month · Business $89/month. Annual billing is displayed as $23/month for Creator and $71/month for Business |
| % of each sale | Starter 5% · Creator 2% · Business 1% |
| Card processing | Stripe's rate on the seller's own account — additional. The page states it as "around 2.9% + 30¢" |
| Fixed per transaction | Stripe's fixed fee, stated on the page as part of "around 2.9% + 30¢" |
| Where the money settles | the seller's own Stripe account |
| Payout fees | none stated by Sublyna; Stripe's payout terms apply |
| Payout timing / minimum | not stated |
| Other fees | none stated |
| Verified | 2026-10-06 · primary |

## Sources
- https://www.sublyna.com/pricing — retrieved 2026-10-06 (the plan table is in the server-rendered HTML, but deep in a 3 MB page that truncating fetchers cut off) — "you only pay standard Stripe processing fees (around 2.9% + 30¢), which go directly to Stripe, not us."
- https://www.sublyna.com/pricing — retrieved 2026-10-06 — plan rows: "Starter — Free (Early Adopter) — 5% transaction fee"; "Creator — $29 — 2% transaction fee"; "Business — $89 — 1% transaction fee".
- https://www.sublyna.com/pricing — retrieved 2026-10-06 — every plan lists its platforms as "Stripe, Discord, Telegram".

## Notes
- The percentage falls as the monthly price rises: 5%, then 2%, then 1%. Stripe's processing is additional at every rung, on the seller's own account.
- The prices are displayed in dollars and euros: Creator $29 (27 €), Business $89 (82 €). The annual figures are per-month equivalents as displayed: Creator $23 (21 €), Business $71 (65 €).
- Every price on the page carries an "Early Adopter" label, including the free Starter plan, so they may be introductory.
- Sublyna's marketing headline of "just 1%" is the Business plan's rate. Business is $89/month, which the headline does not carry.
- Plan limits as displayed: Starter is 2 products and 1 admin seat, with Sublyna branding; Creator is unlimited products and admin seats, with Sublyna branding; Business adds customizable branding and priority support. Customers and transactions are unlimited on every plan.
- The same page carries a banner reading "0% fees for early adopters during 2025 and early 2026", and its FAQ says Sublyna takes no platform fees for early adopters, beside a plan table that charges 5%, 2% and 1%. The table's rates are what this dataset records; the page does not say which applies to a seller signing up now.
- How the seller's Stripe account is connected — Stripe Connect or pasted API keys — is not stated on the page.
- The page was read in a browser. A plain fetcher gets the heading and no plan table, which is what put this platform in "Wanted: help verifying" earlier the same day.
