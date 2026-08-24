# Changelog

A public corrections log. Every row is a number that was stated wrongly somewhere and then fixed, with the source that settled it.

## 2026-08-23 — first public cut

Corrections carried over from the maintainer's internal fee record, which this repo restates in public, plus the ones found while verifying pages on 2026-08-23.

| Date | Platform | Previously stated | Corrected to | Source | Found by |
|---|---|---|---|---|---|
| 2026-08-03 | Discord Server Subscriptions | 10% — the "90/10 split" | **16%** — 10% Platform Fee plus 6% payment processing on desktop and browser | Schedule 1 of the Monetization Terms, support.discord.com | maintainer, reading the primary source |
| 2026-08-03 | Patreon | 8–12%, varying by plan | **10%**, one plan; the tiered structure is retired | patreon.com/pricing | maintainer, reading the primary source |
| 2026-08-03 | Discord Server Subscriptions | Requires roughly 100 members and a 90-day-old server | **No member-count or server-age requirement exists** in Discord's published documents | Monetization Terms, then the Creator Revenue FAQ | maintainer, reading the primary source |
| 2026-08-03 | Discord Server Subscriptions | Briefly marked as **not** US-only, on the strength of the Monetization Terms' EU/UK section. **Reverted the same day.** | **US-only is correct and explicit:** "Server Subscriptions will not be available outside of the United States." The EU/UK section covers Discord's monetization products generally, not Server Subscriptions specifically | Creator Revenue FAQ, creator-support.discord.com | maintainer |
| pre-2026-08 | Whop | 30% commission on marketplace sales | **Removed in May 2025.** Discover sales pay the same rates as direct sales | multiple independent 2026 breakdowns | maintainer |
| 2026-08-07 | flatpass, vs Whop | A flat fee beats Whop's all-in above `fee ÷ 5.7%` — about $510/month for $29 | **`fee ÷ 2.8%` — about $1,036/month.** Dividing by the full 5.7% assumes the flat-fee seller pays no processing; they pay Stripe's 2.9% on their own account. The error halves every break-even | arithmetic; see METHODOLOGY § Comparing a flat fee to a percentage | maintainer |
| 2026-08-07 | flatpass, vs Subscord | flatpass undercuts Subscord at every matching rung | **True at the bottom, false above roughly 200 active subscriptions.** Subscord's $65 up to 500 beats flatpass's $79 (to 200) and $149 (to 750); Subscord's $199 uncapped beats flatpass's $399 | both published ladders | maintainer, after flatpass repriced |
| 2026-08-23 | Circle | Roughly 7% on some plans, from a secondary breakdown | **Professional $89/mo with 2%, Business $199/mo with 1%, Circle Plus 0.5%** | circle.so/pricing | maintainer, reading the primary source |
| 2026-08-23 | Memberful | A free plan with paid tiers above it | **Standard $49/month + 4.9%, plus a custom Enterprise tier.** What is free is a trial: charging starts when the seller goes live | memberful.com/pricing | maintainer, reading the primary source |
| 2026-08-23 | Skool | Pro at 2.9% + $0.30, rising to 3.9% + $0.30 above $899 | **Hobby $9/month with 10%, Pro $99/month with 2.9%.** No fixed per-transaction fee and no higher band appear on the page today; both are now recorded as not stated | skool.com/pricing | maintainer, reading the primary source |
| 2026-08-23 | Gumroad | 10% + $0.50, from a secondary source | **10% + $0.50 confirmed on Gumroad's own page**, plus 30% on sales originated by the Discover marketplace, which had not been recorded | gumroad.com/pricing | maintainer, reading the primary source |
| 2026-08-23 | XOE | Crypto-only, with a free tier | **$0/month, 0% on card payments (the seller pays Stripe's standard processing), 5% on crypto payments** on Base and Solana | xoe.gg and xoe.gg/premium | maintainer, reading the primary source |
| 2026-08-23 | Tribute | Telegram-native, no rate recorded | **10% commission**, payouts on the 25th and the 10th, €100 minimum for bank card payouts | tribute.tg | maintainer, reading the primary source |
| 2026-08-23 | DoorFee | Free 10%, Pro $28/month + 2.5% | **Confirmed unchanged**, and an annual Pro price of $236/year added | doorfee.io and doorfee.io/terms §4 | maintainer, reading the primary source |
| 2026-08-23 | Subscord | Free ≤10, Pro $39 ≤50, Max $65 ≤500, Unlimited $199 | **Confirmed unchanged** from the 2026-08-05 reading | subscord.com | maintainer, reading the primary source |
| 2026-08-23 | PayBot | 3% per sale, no monthly fee, seller's own Stripe | **Confirmed** on PayBot's own pages | paybotapp.com | maintainer, reading the primary source |
| 2026-08-23 | Upgrade.chat | A ladder from a free tier at a higher percentage down to 2.9% on a paid plan | **Moved to unverified.** The pricing page did not render plan names or prices to a fetcher; the only rate the site states plainly is "Starting at 2.9%", which is a floor, not a rate | upgrade.chat and upgrade.chat/pricing | maintainer |
| 2026-08-23 | Sublyna | A free tier plus two paid tiers with falling percentages | **Moved to unverified.** The pricing page could not be fetched automatically; no figure meets this repo's sourcing bar, so none is stated | www.sublyna.com/pricing | maintainer |

Corrections are credited here by name or handle if the reporter wants — open an issue.
