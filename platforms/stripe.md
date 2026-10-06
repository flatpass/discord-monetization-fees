# Stripe

A payment processor, not a Discord platform. It is in this dataset because several platforms here run on the seller's own Stripe account, and their all-in cost is their fee plus this one.

| Field | Value |
|---|---|
| Website | https://stripe.com |
| Pricing page | https://stripe.com/pricing (US) · https://stripe.com/en-de/pricing (EEA) |
| Monthly fee | $0 |
| % of each sale | none — Stripe is the processing line, not a platform fee |
| Card processing | US 2.9% + $0.30 · standard EEA 1.5% + €0.25 · UK 2.5% + €0.25 · international 3.15% + €0.25 · currency conversion +1% on a US account, +2% on an EEA account |
| Fixed per transaction | $0.30 (US) · €0.25 (EEA, UK, international) |
| Where the money settles | the account that made the charge |
| Payout fees | not recorded here |
| Payout timing / minimum | set per account; not recorded here |
| Other fees | currency conversion, when required: +1% on a US account, +2% on an EEA account |
| Verified | 2026-10-06 · primary |

## Sources
- https://stripe.com/pricing — retrieved 2026-10-06 — "2.9% + 30¢ per successful transaction for domestic cards"; "+ 1% if currency conversion is required". The URL redirects outside the US to a country page; the US page was read with US content forced.
- https://stripe.com/en-de/pricing — retrieved 2026-10-06 — "1.5% + €0.25 for standard European Economic Area cards"; "2.5% + €0.25 for UK cards"; "3.15% + €0.25 for international cards"; "+ 2% if currency conversion is required".

Until 2026-10-06 this file gave +2% conversion for every account. That is the EEA figure; a US account pays +1%.

## Notes
- **A seller on their own Stripe account pays their own country's Stripe pricing, not the platform's.** A platform being based in the EU does not give its sellers EEA rates, and a platform being based in the US does not impose US rates on a European seller. The rate follows the account that takes the charge.
- Within whichever country's pricing applies, the tier then follows the member's card: EEA, UK or international, plus conversion where it applies.
- **Platforms that process their own cards work the opposite way.** Whop and Discord Server Subscriptions carry their own rate wherever the seller is.
- Headline arithmetic in this repo uses the US rate throughout so one basis runs through every comparison. An EEA seller's processing is roughly half of it, which moves every all-in figure in this dataset.
