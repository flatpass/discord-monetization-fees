# Discord monetization fees

A sourced, dated record of what each platform charges to sell paid access to a Discord server — and the nearest membership platforms alongside them — maintained in the open so the numbers can be checked and corrected.

This dataset is maintained by **flatpass** ([flatpass.io](https://flatpass.io)), which sells one of the products in the table below. That is a conflict of interest, so here is how it is handled: every number carries a source URL, a retrieval date and a verification tier; the table includes the rows where flatpass is the more expensive option, and [`platforms/flatpass.md`](platforms/flatpass.md) has a section that names them; corrections are logged in [CHANGELOG.md](CHANGELOG.md) with credit to whoever found them; and anyone can open an issue disputing any figure here. If a number is wrong, the fix is a pull request, not an argument.

Last updated **2026-08-23**.

## The table

Every row below is either `primary` (read on the platform's own page or terms) or `direct-confirmation` (see METHODOLOGY). Platforms whose own pages could not be read are in [Wanted: help verifying](#wanted-help-verifying) instead, with no numbers attached.

| Platform | Monthly fee | % of each sale | Card processing | Where the money settles | Payout fees | Verified | Tier |
|---|---|---|---|---|---|---|---|
| [Whop](platforms/whop.md) | $0 | 3% [^1] | own, 2.7% + $0.30 | Whop balance | ACH $2.50 · instant 4% + $1 · wire ~$23 | 2026-08-03 | direct-confirmation |
| [LaunchPass](platforms/launchpass.md) | $29 Premium, per community [^2] | 3.5% | seller's own Stripe | seller's Stripe | none | 2026-08-02 | primary |
| [flatpass](platforms/flatpass.md) | $0 / $29 / $79 / $149 / $399 [^3] | 0% | seller's own Stripe | seller's Stripe | none | 2026-08-23 | primary |
| [Subscord](platforms/subscord.md) | $0 / $39 / $65 / $199 [^4] | 0% (crypto 0.5% + gas) | seller's own Stripe, 2.9% + $0.30 | seller's Stripe | none | 2026-08-23 | primary |
| [PayBot](platforms/paybot.md) | $0 | 3% | seller's own Stripe | seller's Stripe | none | 2026-08-23 | primary |
| [DoorFee](platforms/doorfee.md) | $0 Free · $28 Pro | 10% Free · 2.5% Pro | seller's own Stripe | seller's Stripe | none | 2026-08-23 | primary |
| [XOE](platforms/xoe.md) | $0 | 0% cards · 5% crypto | seller's own Stripe | seller's Stripe; crypto to wallet | none stated | 2026-08-23 | primary |
| [Discord Server Subscriptions](platforms/discord-server-subscriptions.md) | $0 | 10% platform fee | own, 6% desktop/browser | Discord | not stated | 2026-08-03 | primary |
| [Patreon](platforms/patreon.md) | $0 | 10% | own, rate not stated here | Patreon | payout and conversion fees apply | 2026-08-03 | primary |
| [Ko-fi](platforms/ko-fi.md) | $0, or paid Gold [^5] | 0% tips · 5% memberships and shop | seller's own PayPal or Stripe | seller's account | none | 2026-08-03 | primary |
| [Skool](platforms/skool.md) | $9 Hobby · $99 Pro | 10% Hobby · 2.9% Pro | no separate line published | not stated | not stated | 2026-08-23 | primary |
| [Gumroad](platforms/gumroad.md) | $0 | 10% + $0.50 · 30% via Discover | no separate line published | Gumroad | not stated | 2026-08-23 | primary |
| [Memberful](platforms/memberful.md) | $49 Standard | 4.9% | seller's own Stripe | seller's Stripe | none stated | 2026-08-23 | primary |
| [Circle](platforms/circle.md) | $89 Pro · $199 Business | 2% · 1% · 0.5% Circle Plus | not stated | not stated | not stated | 2026-08-23 | primary |
| [Tribute](platforms/tribute.md) | $0 | 10% | no separate line published | Tribute | not stated [^6] | 2026-08-23 | primary |
| [Stripe](platforms/stripe.md) — *processor, for reference* | $0 | — | US 2.9% + $0.30 [^7] | the account that took the charge | — | 2026-08-03 | primary |

[^1]: Whop's 3% applies to sales that run through an automation — Discord, Telegram or TradingView gating. For a Discord seller that is every sale, so the all-in base is 5.7% + $0.30. **It is not on Whop's public pricing page.**
[^2]: LaunchPass's Free plan cannot charge members. Premium is $29/month per community, so two servers cost twice.
[^3]: flatpass is metered on active paid members: free to 15, then $29 to 80, $79 to 200, $149 to 750, $399 uncapped.
[^4]: Subscord is metered on active subscribers: free to 10, then $39 to 50, $65 to 500, $199 uncapped.
[^5]: Gold waives the 5%. Its monthly price is quoted as both $6 and $12 across 2026 guides, so this dataset does not state it.
[^6]: Tribute pays out on the 25th and the 10th, with a €100 minimum for bank card payouts.
[^7]: Standard EEA 1.5% + €0.25 · UK 2.5% + €0.25 · international 3.15% + €0.25 · +2% on currency conversion.

Skool, Gumroad and Circle host or sell the community themselves rather than gating a Discord server. Tribute gates Telegram. They are here because a seller weighing options weighs them too.

## How to read this

**All-in versus platform-fee-only.** A platform fee is not the whole bill — card processing sits beside it, and the two are not comparable across platforms because Discord's own processing is 6%, roughly double what everyone else charges. So every cost computed in this repo is **all-in**: the platform's fee plus card processing at that platform's own rate. Where a figure is platform-fee-only it says so and names what it leaves out. [METHODOLOGY.md](METHODOLOGY.md) § Conventions has the full rule.

**Whose processing rate.** Whop and Discord process their own cards, so their rate follows *them* wherever the seller is. LaunchPass, flatpass, Subscord, PayBot, DoorFee, XOE, Memberful and Ko-fi run on the seller's own Stripe or PayPal account, so the rate follows the *seller's* country and the member's card. A platform being based in the EU does not give its sellers EEA rates.

**Flat fee versus percentage.** The crossover is `flat fee ÷ (competitor's all-in % − the seller's own processing %)`. Dividing by the competitor's full percentage instead is a common error that halves every break-even — see [METHODOLOGY.md](METHODOLOGY.md) § Comparing a flat fee to a percentage.

## A worked example

Both examples model **57 and 14 memberships at $35/month**, the modelled average membership price this repo uses (see [METHODOLOGY.md](METHODOLOGY.md) § The modelled average membership price). Transactions are the monthly volume divided by $35 and rounded. Processing is Stripe's US rate, 2.9% + $0.30, wherever the seller pays it themselves.

### $2,000/month in sales — 57 transactions

| Platform | Arithmetic | All-in monthly cost |
|---|---|---|
| flatpass | $29 (Starter, 57 paid members) + $2,000 × 2.9% ($58.00) + 57 × $0.30 ($17.10) | **$104.10** |
| Whop | $2,000 × 5.7% ($114.00) + 57 × $0.30 ($17.10) | **$131.10** |
| LaunchPass | $29 + $2,000 × 6.4% ($128.00) + 57 × $0.30 ($17.10) | **$174.10** |
| Discord Server Subscriptions | $2,000 × 16% | **$320.00** |

Whop's 5.7% is 3% + 2.7%. LaunchPass's 6.4% is 3.5% + Stripe's 2.9%. flatpass's 2.9% is Stripe's alone. Discord's 16% is 10% + 6%, and Discord publishes no per-transaction fixed fee, so none is invented here.

### $500/month in sales — 14 transactions

| Platform | Arithmetic | All-in monthly cost |
|---|---|---|
| flatpass | $0 (Free, 14 paid members) + $500 × 2.9% ($14.50) + 14 × $0.30 ($4.20) | **$18.70** |
| Whop | $500 × 5.7% ($28.50) + 14 × $0.30 ($4.20) | **$32.70** |
| LaunchPass | $29 + $500 × 6.4% ($32.00) + 14 × $0.30 ($4.20) | **$65.20** |
| Discord Server Subscriptions | $500 × 16% | **$80.00** |

### $800/month in sales — 23 transactions, and this is where flatpass loses

| Platform | Arithmetic | All-in monthly cost |
|---|---|---|
| Whop | $800 × 5.7% ($45.60) + 23 × $0.30 ($6.90) | **$52.50** |
| flatpass | $29 (Starter, 23 paid members) + $800 × 2.9% ($23.20) + 23 × $0.30 ($6.90) | **$59.10** |
| LaunchPass | $29 + $800 × 6.4% ($51.20) + 23 × $0.30 ($6.90) | **$87.10** |
| Discord Server Subscriptions | $800 × 16% | **$128.00** |

Whop is $6.60/month cheaper there. That band runs from the sixteenth paid member — where flatpass's Free tier ends — to about $1,036/month in sales, which is $29 ÷ 2.8%. At the $35 modelled price the flat fee wins above that and does not give it back; below the sixteenth member flatpass is $0 and wins again. At lower membership prices the picture is less tidy — flatpass's caps are break-evens at $35, so at $25 or $20 each cap re-opens a small losing band. [`platforms/flatpass.md`](platforms/flatpass.md) lists them. At $1,000/month the two are within a dollar of each other: Whop $65.70, flatpass $66.70.

Redo any of these with the numbers in [`data/fees.json`](data/fees.json).

## Wanted: help verifying

These platforms are in [`data/fees.json`](data/fees.json) with `"verification": "unverified"` and no fee figures. They are deliberately not in the table above. If you can read their own pricing page, open an issue.

| Platform | What is missing |
|---|---|
| [Sublyna](platforms/sublyna.md) | The plan table at `www.sublyna.com/pricing` could not be fetched automatically on 2026-08-23 — the page returned only its heading. Needed: each plan's name, monthly price, percentage per sale, and whether Stripe processing is additional. |
| [Upgrade.chat](platforms/upgrade-chat.md) | `upgrade.chat/pricing` rendered a Monthly / Lifetime toggle but no plan names or prices on 2026-08-23. The site states "Starting at 2.9%", which is a floor rather than a rate. Needed: each plan's name, monthly price and percentage. |

Also wanted, on rows that are otherwise verified: Patreon's own card processing rate; Ko-fi Gold's current monthly price; Skool's and Circle's payout terms; whether Circle publishes a processing rate anywhere.

## Contributing

Finding wrong numbers is the point of this repo — report one and it gets fixed and credited. See [CONTRIBUTING.md](CONTRIBUTING.md) for what counts as a source and how to add a platform.

## License

[CC BY 4.0](LICENSE). Use the data, attribute the source.

## Maintained by

flatpass — [flatpass.io](https://flatpass.io) · support@flatpass.io · [@flatpass_io](https://x.com/flatpass_io)
