# Ko-fi

A tipping and membership platform for creators, with a Discord connection.

| Field | Value |
|---|---|
| Website | https://ko-fi.com |
| Pricing page | https://ko-fi.com/pricing |
| Monthly fee | $0 on Standard and Ko-fi free · Gold $12/month |
| % of each sale | 5% on memberships, shop sales, commissions and monthly tips · one-time tips 5% on Standard (the default for new creators), 0% with Standard switched off (Ko-fi free) · 0% on Gold with Standard off, which Discord rewards rule out: a Discord role seller pays 5% on everything |
| Card processing | the seller's own PayPal or Stripe |
| Fixed per transaction | the processor's fixed fee |
| Where the money settles | the seller's own PayPal or Stripe account |
| Payout fees | none charged by Ko-fi; the processor's terms apply |
| Payout timing / minimum | not stated |
| Other fees | none stated |
| Verified | 2026-10-06 · primary |

## Sources
- https://ko-fi.com/pricing — retrieved 2026-10-06 — Standard, "(default for new creators)": "5% service fee on all payment types (tips, memberships, commissions and shop sales)".
- https://ko-fi.com/pricing — retrieved 2026-10-06 — Ko-fi free: "0% service fee on tips, keep every tip you receive. 5% service fee on Memberships, Shop sales, and Commissions".
- https://ko-fi.com/pricing — retrieved 2026-10-06 — Gold: "$12 /month", "0% service fee".
- https://help.ko-fi.com/hc/en-us/articles/360002506494-Does-Ko-fi-take-a-fee — retrieved 2026-10-06 — "You can toggle Standard mode on or off any time from Settings > Payment."; the fee table (one-off tips and goals 0% on Free, 5% on Standard; monthly tips, memberships, commissions and shop 5% on both); on Gold, "If you already have this switched on when you subscribe to Gold, you'll need to opt out separately to remove the service fee."
- https://help.ko-fi.com/hc/en-us/articles/8664701197073-How-do-supporters-join-my-Discord-server — retrieved 2026-10-08 — "To offer Discord rewards to your supporters, you'll need to be on the Standard plan."; "If you're not already on Standard, you'll be prompted to opt in when you add your Discord server or adjust your roles."

`ko-fi.com/pricing` returns 403 to an automated fetcher. It was read in a browser on 2026-08-03 and again on 2026-10-06.

## Notes
- **Two $0 modes, and the default charges on tips.** Standard, the default for new creators, takes 5% of every payment type, one-time tips included. It is a toggle — Settings > Payment — and switching it off leaves Ko-fi free: 0% on one-time tips and crowdfunding goals, 5% on monthly tips, memberships, shop and commissions. A membership pays 5% either way. Until 2026-10-06 this file said "0% on tips" without the mode or the one-time scope.
- **Gold is $12/month and waives the fee only with Standard off.** A creator who subscribes to Gold with Standard on has to switch it off separately. The $6 that some 2026 guides quote is not on Ko-fi's page.
- **Discord rewards need Standard.** Ko-fi's help centre says Discord rewards require the Standard plan and prompts the opt-in when a server is added. So a seller selling Discord roles pays 5% on every payment type, one-time tips included, and Gold's waiver does not reach them. Added 2026-10-08; until then this file gave the Gold waiver without that limit.
- Ko-fi does not sit in the payment path. Payments go to the seller's own PayPal or Stripe.
