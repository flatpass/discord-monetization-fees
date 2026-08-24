# Contributing

This repo exists to be checked. A wrong number here is a bug report, not a disagreement.

## Reporting a wrong number

Open an issue using the **[wrong number]** template, or a pull request if you would rather fix it directly. Either way, include:

- **The platform.**
- **The number as this repo states it** — the row or field you are disputing.
- **The number the platform states.**
- **The URL of the platform's own page** where you read it. Its pricing page, help centre, docs or terms.
- **The date you saw it.** Pages move; a dated reading is what makes a correction checkable later.
- **A screenshot**, optionally. Useful when the price renders in JavaScript and a fetcher cannot reach it.

If the number is missing rather than wrong — a field that says "not stated" and shouldn't — the same form works.

## What counts as a source

Ranked, highest first. Same ranking as [METHODOLOGY.md](METHODOLOGY.md) § Sources, ranked.

1. The platform's own terms or fee schedule.
2. The platform's own pricing page.
3. The platform's own help centre or docs.
4. A reputable independent breakdown — accepted, but labelled `secondary`, never presented as the platform's own statement.

**A competitor's comparison page is not a source**, for any platform, ever. Neither is a listicle, a "best alternatives" post, or a fee guide's headline figure. The reason is in METHODOLOGY § Sources, ranked, with two measured examples.

If you cannot source a figure, say "not stated". That is a valid, correct answer and it will be merged.

## Adding a platform

Three changes, in one pull request:

1. **A file in `platforms/<id>.md`**, following the skeleton every other file uses: the field table, a `## Sources` section with one line per source (URL, retrieval date, verbatim quote of 25 words or fewer), and a `## Notes` section limited to what the platform's own pages say.
2. **An entry in `data/fees.json`.** Use `null` for anything the platform does not state — never a guessed number. Every figure in the platform's markdown table must match its JSON entry exactly.
3. **A row in the README table only if the platform is primary-verified.** If its own pages could not be read, it goes in "Wanted: help verifying" instead, with `"verification": "unverified"` in the JSON and no fee figures anywhere.

Validate the JSON before opening the pull request:

```sh
python3 -c 'import json; json.load(open("data/fees.json"))'
```

## Style

- Plain and concrete. State the mechanism; skip the adjectives.
- Cite and date everything. A number without a URL and a retrieval date does not go in.
- Scope every rate. "3%" is wrong if the real thing is "3% on automation-gated sales".
- No reviews, complaints, ratings or opinions about any platform. Published fees and payout terms only.
- Describe a competitor's interface if you must; never reproduce it.
- **"flatpass" is lowercase**, including at the start of a sentence.
- No emoji, no exclamation marks.

## Credit

Every correction is logged in [CHANGELOG.md](CHANGELOG.md) with the source that settled it and who found it. Say in your issue how you would like to be credited — name, handle, or not at all.

## Licence

This repo is [CC BY 4.0](LICENSE). By contributing you agree that your contribution is published under the same licence.
