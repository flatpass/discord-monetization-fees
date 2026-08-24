# Subscord

A paid-access layer for Discord, metered on active subscribers, with card and crypto payments.

| Field | Value |
|---|---|
| Website | https://subscord.com |
| Pricing page | https://subscord.com (pricing section at /#pricing) |
| Monthly fee | Free $0 up to 10 active subscribers · Pro $39 up to 50 · Max $65 up to 500 · Unlimited $199 uncapped |
| % of each sale | 0% platform fee on card sales · 0.5% on crypto payments, plus gas |
| Card processing | 2.9% + $0.30 · Stripe, on the seller's own account |
| Fixed per transaction | $0.30 on card sales |
| Where the money settles | the seller's own Stripe account; crypto to the seller's wallet |
| Payout fees | none charged by Subscord; Stripe's payout terms apply |
| Payout timing / minimum | not stated |
| Other fees | gas fees on crypto payments |
| Verified | 2026-08-23 · primary |

## Sources
- https://subscord.com — retrieved 2026-08-23 — "0% platform fees"
- https://subscord.com — retrieved 2026-08-23 — plan rows: "Free $0/month, Up to 10 active subscribers"; "Pro $39/month, Up to 50"; "Max $65/month, Up to 500"; "Unlimited $199/month".
- https://subscord.com — retrieved 2026-08-23 — card payments "2.9% + $0.30"; crypto "0.5% fee" plus gas.

## Notes
- The ladder read on 2026-08-23 is identical to the one read on 2026-08-05. Nothing moved.
- **Subscord connects to Stripe by asking the seller to paste their Stripe API keys**, per its setup documentation as read on 2026-08-05: "find your Stripe API keys in your Stripe Dashboard and paste the public and secret keys into the respective fields." Several other platforms in this table — flatpass, DoorFee, PayBot — connect over Stripe Connect instead. This is a fact about the connection method, recorded because it is a published difference in how the accounts are linked.
- Subscord's own site carries a comparison table quoting rates for other platforms. Those figures are not used anywhere in this dataset — see METHODOLOGY on why competitor content is never a source.
