# Sublaunch

A paid-access layer for Telegram, Discord and WhatsApp communities plus hosted courses, on a free percentage tier or a monthly plan with a lower percentage. Not to be confused with Sublyna, a different product whose blog markets it as a "Sublaunch alternative".

| Field | Value |
|---|---|
| Website | https://sublaunch.com |
| Pricing page | https://sublaunch.com/#pricing_id (a section of the homepage) |
| Monthly fee | Free $0 ("Free forever") · Business $99/month · Premium $169/month |
| % of each sale | Free 15% · Business 4% · Premium 3% |
| Card processing | Stripe's rate on the seller's own account — additional. The FAQ: "Stripe's processing fees apply in addition to Sublaunch's commissions" |
| Fixed per transaction | Stripe's fixed fee, on the seller's own account |
| Where the money settles | the seller's own Stripe account — the terms: "Sublaunch does not hold or manage funds for creators" |
| Payout fees | none of Sublaunch's own; Stripe's payout terms apply |
| Payout timing / minimum | not stated (payouts run in the seller's own Stripe account) |
| Other fees | none stated |
| Verified | 2026-08-26 · primary |

## Sources

- https://sublaunch.com/#pricing_id — retrieved 2026-08-26 — plan cards and fee row: "Free — To start for free in 5 minutes. Free forever."; "Business — $99 per month"; "Premium — $169 per month"; "Transaction fee — 15% — 4% — 3%".
- https://sublaunch.com — retrieved 2026-08-26 — FAQ "Are there any fees to use Sublaunch?": "Sublaunch offers a free plan with a 15% commission fee. Paid plans are available, reducing the commission to as low as 3%, based on your volume. Please note that Stripe's processing fees apply in addition to Sublaunch's commissions."
- https://sublaunch.com — retrieved 2026-08-26 — FAQ "Does upgrading affect current subscription commission fees?": "No, the commission fee for any existing subscriptions will remain the same even if you upgrade your plan. The new commission percentage fee will only apply to future subscriptions created after your plan upgrade."
- https://sublaunch.com/terms — retrieved 2026-08-26 — "Sublaunch may collect transaction fees based on the plan chosen by the creator. These fees are deducted automatically via Stripe from each transaction."
- https://sublaunch.com/terms — retrieved 2026-08-26 — "Sublaunch does not hold or manage funds for creators; all funds are processed and delivered directly to creators' Stripe accounts."

## Notes

- The 15% free-tier commission is the highest free-tier rate in this dataset — DoorFee's free plan is 10%, Upgrade.chat's 5.9%, Sublyna's 5%. The paid plans buy it down: Business $99 at 4%, Premium $169 at 3%.
- A plan upgrade does not reprice existing subscribers: the commission on a subscription is fixed at creation, and the new rate applies only to subscriptions created after the upgrade (FAQ, quoted above). A seller who grows on the free plan carries 15% subscribers until they churn.
- Payments run on the seller's own Stripe account, which the seller creates and connects; the terms put disputes, refunds, chargebacks and tax compliance on the creator, handled directly with Stripe. How the account is connected — Stripe Connect or API keys — is not stated on the page or in the terms.
- Gates Telegram channels, Discord servers (role-based access) and WhatsApp groups, and hosts online courses natively; Discord access is one product type among several rather than the platform's centre.
- Stripe is the only stated payment path — the FAQ lists Visa, Mastercard, American Express, Apple Pay and Google Pay through it, and describes PayPal and crypto as "being monitored for future support", not offered.
- The pricing section and FAQ answers are server-rendered — a plain fetch does get the plan table, unlike Sublyna's and Upgrade.chat's pages. The figures here were read in a browser anyway.
- The terms are operated by MetaStudio LLC, "operating as Sublaunch"; the footer says "Sublaunch, Inc.".
