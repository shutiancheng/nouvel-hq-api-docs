# Nouvel API docs

Public documentation for the Nouvel `/v1` API, published with Mintlify.

## This repo is public

Everything here is world readable. The app repo's `docs/` directory is **not**
part of this repo and must never be copied into it: it holds
`unit-economics-audit.md` and `api-margin-analysis.md`, which contain COGS,
margins and provider pricing.

Keeping the docs in their own repo is the reason that cannot happen by accident.

## Local preview

```sh
npm i -g mint
mint dev
```

Opens on http://localhost:3000.

## Deploying

Mintlify is connected to this repo on the `main` branch, with `docs.json` at the
root. Push to `main` and it redeploys. Leave **"docs.json is in a subdirectory"**
off in Git settings.

## Keeping it accurate

Prices, rate limits, error codes and languages are duplicated here from the app
repo. Nothing enforces that they stay in sync, so when any of these change,
update the matching page.

| Source of truth (in `nouvelhq`) | Page here |
|---|---|
| `src/lib/api/pricing.ts` | `billing.mdx`, `index.mdx` |
| `KEY_LIMITS` in `src/lib/api/request.ts` | `rate-limits.mdx` |
| `ApiErrorCode` in `src/lib/api/request.ts` | `errors.mdx` |
| `OutputLanguage` in `src/lib/analysis/language.ts` | `markets.mdx` |
| `CREDIT_PACKS` in `src/lib/billing/credit-packs.ts` | `billing.mdx` |
