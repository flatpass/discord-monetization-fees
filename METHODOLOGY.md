# Methodology

How every number in this repo got here, and the rules that decide whether a number is allowed in at all.

## 1. Conventions

**All-in is the basis wherever a cost is computed.** A platform fee is one line of the bill; card processing is another. Quoting only the platform fee would put Whop's 3% beside flatpass's 0% and advertise a three-point gap that no seller ever receives, because the flatpass seller still pays Stripe. So every computed figure in this repo models the platform's fee **plus** card processing at that platform's own rate.

The reason this is a rule and not a preference is Discord. Its own processing is 6%, roughly double the 2.7–2.9% everyone else charges, so processing stopped being a constant that divides out of the comparison. Any platform whose processing is not comparable to the rest breaks a platform-fee-only table; Discord already did.

**Platform-fee-only survives only in labeled prose that names its components.** "3% on Discord-gated sales" beside "16% of every sale — the 90/10 split plus 6% processing" is fine, because the reader can see what is in each number. A bare computed figure never uses that basis.

**Whose processing rate.** Two shapes, and they behave differently:

- **Platforms that process their own cards** — Whop, Discord Server Subscriptions, and by their own published wording Skool, Gumroad, Patreon and Tribute — carry their rate wherever the seller is.
- **Platforms that run on the seller's own account** — LaunchPass, flatpass, Subscord, PayBot, DoorFee, Sublyna, XOE, Upgrade.chat, Memberful, Ko-fi — carry the seller's country's Stripe or PayPal pricing, and within that, the tier follows the member's card (EEA, UK, international, plus conversion).

A consequence worth stating out loud: a platform being based in the EU does not give its sellers EEA rates, and a platform being based in the US does not impose US rates on a European seller. The rate follows the account that takes the charge.

**Headline arithmetic in this repo uses Stripe's US rate** (2.9% + $0.30) wherever the seller pays processing themselves, so one basis runs through every worked example. This is stated at each example. An EEA seller's processing is roughly half of it, which moves every all-in figure here — including the ones that flatter the maintainer.

## 2. Comparing a flat fee to a percentage

The crossover — the sales volume above which a flat monthly fee costs less than a percentage — is:

```
flat fee ÷ (competitor's all-in % − the seller's own processing %)
```

**Not** `flat fee ÷ competitor's all-in %`. The seller on the flat-fee platform still pays card processing; only the *spread* between the two has to be made up. The per-transaction fixed fee washes out entirely when both sides pay one on the same number of transactions.

Worked, against Whop:

```
$29 ÷ (5.7% − 2.9%)  =  $29 ÷ 2.8%  ≈  $1,036/month in sales   ← correct
$29 ÷ 5.7%                            ≈  $509/month in sales   ← wrong
```

The wrong form halves every break-even, and it halves it in the flat-fee platform's favour. **The maintainer made this exact error once**, in a comparison that claimed $29 beat Whop above roughly $510/month; the real figure is roughly $1,036. It is logged in [CHANGELOG.md](CHANGELOG.md).

## 3. The modelled average membership price

Translating a sales volume into a member count — or the reverse — needs an assumed membership price. This repo uses **$35/month**, and states it wherever it is used.

Where it comes from: comparable Discord sellers cluster at $25–50/month, which is the single most common band; cook and sneaker groups run $20–60; trading and alerts communities run higher, $50–200. $35 sits inside the common band.

It is an assumption, so this repo keeps it out of the load-bearing figures. **Crossovers are quoted in sales volume, because volume does not depend on the price assumption** — the $1,036 above is $29 ÷ 2.8% whatever a membership costs. Only the member-count translations move with it, and those are labelled as translations.

## 4. Sources, ranked

1. **The platform's own terms or fee schedule.** Highest, because it is the document the platform is bound by.
2. **The platform's own pricing page.**
3. **The platform's own help centre or docs.**
4. **A reputable independent breakdown** — labelled `secondary`, never presented as the platform's own statement.
5. Nothing. Which is written as **"not stated"**, never as a guess.

**A competitor's comparison content is never a source.** Not their `/vs/` pages, not their "alternatives" blog posts, not a listicle. The reason is concrete: DoorFee's comparison content, checked on 2026-08-13, stated LaunchPass at 5% when LaunchPass's own help centre says 3.5%, and Whop at 7.9% when the all-in figure is 5.7%. Both errors ran in DoorFee's favour. A dataset that picks numbers up from that content inherits the errors, and being caught overstating a rival's fee costs more than the comparison wins.

**A fee guide's headline is not a reading of the schedule.** Three live examples of what that gets you:

- Discord's "90/10 split" is the Platform Fee alone. The 6% payment processing is in the same schedule, one row over. Discord's take on a desktop or browser sale is 16%.
- Whop's 30% marketplace commission was removed in May 2025. Guides still quote it.
- Patreon's 8% / 12% plan tiers are retired. There is one plan, at 10%.

The pattern is consistent: secondary guides copy each other, and they all copy the headline rather than the schedule.

## 5. Verification tiers

| Tier | What it means |
|---|---|
| `primary` | Read on the platform's own page, terms or docs. Carries a URL and a retrieval date. |
| `direct-confirmation` | Not published by the platform, but confirmed directly with the platform or from a maintainer's own account, and corroborated by independent breakdowns. **Used for exactly one figure in this repo: Whop's 3% automation fee.** |
| `secondary` | An independent breakdown only, with no primary reading behind it. Labelled as such at the point of use. |
| `unverified` | No source meeting the bar above. The platform gets a file saying what was attempted and what is known with what confidence, and it appears in `fees.json` with `"verification": "unverified"` and no fee figures — never in the README's table. |

Whop's 3% is the tier's only occupant because it is genuinely unpublished. A reader who opens Whop's pricing page will not find it, and this repo says so on the row rather than quietly presenting the figure as if it were on the page.

## 6. Pages that block automated fetching

`support.discord.com`, `creator-support.discord.com` and `ko-fi.com/pricing` return 403 to a fetcher. They render fine in a browser, and that is how the figures here were read. `support.patreon.com` does the same and was also blocked for the maintainer's browser, so Patreon's creator fees article was read through a render proxy.

**A 403 is not a finding.** This is worth stating as a rule because accepting one as a dead end has already produced a wrong correction in this dataset's history: a US-only claim about Discord Server Subscriptions was "corrected" away by reasoning from a document that did not answer the question, while the document that answered it directly sat behind a 403 whose workaround was already known. The correction was reverted the same day. See [CHANGELOG.md](CHANGELOG.md).

The same rule applies to a page that returns 200 but renders its prices in JavaScript a fetcher does not run. That is not "the platform does not publish a price" — it is "this could not be fetched automatically", and the platform goes to `unverified` until someone reads it in a browser. `www.sublyna.com/pricing` and the pricing section of `upgrade.chat` are both of that kind — their plan tables render only in a browser, and Upgrade.chat's section defaults to its Lifetime toggle, so the monthly prices appear only once it is switched.

## 7. Scope and fairness rules

- **Published fees and payout terms only.** Monthly prices, percentages and their scope, card processing and whose rate it is, fixed per-transaction fees, payout methods and fees, payout timing and minimums where the platform publishes them, holds or reserves **only** where the platform's own terms state them, and where the money settles when the platform's own docs say so.
- **No reviews, no complaints, no ratings, no opinions about platforms.** Whatever is true about any platform's conduct, it is not a published fee and it is not in this dataset.
- **Every claim carries its scope.** Whop's 3% is on automation-gated sales. Gumroad's 30% is on Discover-originated sales. Ko-fi's 5% is on memberships and shop sales and not on tips. A rate without its scope is a wrong rate.
- **Competitor interfaces are described, never reproduced.** Their screenshots are their copyrighted interface. Quotes are limited to the short fee wording needed to source a number.
- **When unsure, say less.** "Not stated" is always available and is never wrong.

## 8. Re-verification order

Highest yield first. Each of these has produced a wrong number before.

1. **Discord's Schedule 1** — the one most likely to move and the one every secondary source gets wrong.
2. **Whop's unpublished 3%** — unpublished means it can change silently. It rests on a direct confirmation from 2026-08-03 plus independent breakdowns agreeing.
3. **Stripe's card tiers** — the tier structure changes more often than the headline rate.
4. **The published pricing pages** — LaunchPass, Patreon, Ko-fi, and the platforms verified on 2026-08-23. Lower risk, but they are the rows a reader is most likely to check.

A rate that changes should move the platform's file, its entry in `data/fees.json`, and the README table in the same commit, with a row in `CHANGELOG.md`.
