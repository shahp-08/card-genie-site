# card-genie-site

The public face of [Card Genie](https://github.com/shahp-08/card-genie): its
privacy policy, its terms, and the kill-switch feed the app fetches at launch.

Everything here is **generated**. Do not edit these files by hand — the source
is `src/app/legal.ts` and `data/overrides.yaml` in the application repository,
and `npm run build:legal` writes the pages. A hand edit here is silently
reverted the next time either is published, and makes the hosted copy disagree
with the copy rendered inside the app.

| File | What it is | Generated from |
|---|---|---|
| `privacy.html` | The privacy policy App Store Connect points at | `src/app/legal.ts` |
| `terms.html` | The terms of use, including Apple's required EULA clauses | `src/app/legal.ts` |
| `overrides.json` | Cards switched off since the last release, with reasons | `data/overrides.yaml` |

`overrides.json` is public on purpose. It is a list of cards we are unsure
about, which is not a secret, and hosting it publicly is what lets the app
fetch it carrying no credential of any kind. It can only ever stop the app
using a card — there is no field in it that could raise a rate, enable a card,
or change a number.
