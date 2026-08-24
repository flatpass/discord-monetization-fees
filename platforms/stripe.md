# Stripe

A payment processor, not a Discord platform. It is in this dataset because several platforms here run on the seller's own Stripe account, and their all-in cost is their fee plus this one.

| Field | Value |
|---|---|
| Website | https://stripe.com |
| Pricing page | https://stripe.com/pricing (US) · https://stripe.com/en-de/pricing (EEA) |
| Monthly fee | $0 |
| % of each sale | none — Stripe is the processing line, not a platform fee |
| Card processing | US 2.9% + $0.30 · standard EEA 1.5% + €0.25 · UK 2.5% + €0.25 · international 3.15% + €0.25 · currency conversion +2% |
| Fixed per transaction | $0.30 (US) · €0.25 (EEA, UK, international) |
| Where the money settles | the account that made the charge |
| Payout fees | not recorded here |
| Payout timing / minimum | set per account; not recorded here |
| Other fees | +2% when currency conversion is required |
| Verified | 2026-08-03 · primary |

## Sources
- https://stripe.com/pricing — retrieved 2026-08-03 — US standard card rate. No verbatim quote was recorded at retrieval.
- https://stripe.com/en-de/pricing — retrieved 2026-08-03 — EEA, UK, international and conversion rates. No verbatim quote was recorded at retrieval.

## Notes
- **A seller on their own Stripe account pays their own country's Stripe pricing, not the platform's.** A platform being based in the EU does not give its sellers EEA rates, and a platform being based in the US does not impose US rates on a European seller. The rate follows the account that takes the charge.
- Within whichever country's pricing applies, the tier then follows the member's card: EEA, UK or international, plus conversion where it applies.
- **Platforms that process their own cards work the opposite way.** Whop and Discord Server Subscriptions carry their own rate wherever the seller is.
- Headline arithmetic in this repo uses the US rate throughout so one basis runs through every comparison. An EEA seller's processing is roughly half of it, which moves every all-in figure in this dataset.
