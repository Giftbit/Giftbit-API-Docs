# Giftbit API documentation instructions

## About this project

- This is the Giftbit API documentation site, built on [Mintlify](https://mintlify.com).
- Guide pages are MDX files with YAML frontmatter, under `guides/` (plus the `index.mdx` introduction).
- The API reference is generated from a single OpenAPI 3.1 spec at `api-reference/openapi.yaml`.
- Configuration and navigation live in `docs.json`.
- The canonical source for ported content is the legacy `../apiary.apib` (Apiary Blueprint). Keep it in sync when the API changes until it is retired.
- Run `mint dev` to preview locally.
- Run `mint broken-links` to check links.
- Lint the OpenAPI spec with `npx @redocly/cli lint api-reference/openapi.yaml`.

## Terminology

- Use **reward** in prose, not "gift". The API field names still use `gift_*` / `/gifts` — keep those verbatim in code formatting.
- Use **order** for a `/campaign` (the API/JSON calls this object `campaign`; keep `campaign` verbatim in code and JSON).
- Two environments: **Testbed** (`https://api-testbed.giftbit.com/papi/v1`) and **Production** (`https://api.giftbit.com/papi/v1`).
- Field, code, and endpoint names are always in code formatting with their exact casing: `brand_code`, `price_in_cents`, `gift_template`, `delivery_type`, `/direct_links`, `/embedded`.

## Style preferences

- Use active voice and second person ("you").
- Keep sentences concise — one idea per sentence.
- Use sentence case for headings.
- Bold for UI elements: Click **Account → API keys**.
- Code formatting for file names, commands, paths, field names, and code references.
- Prefer Mintlify components where they add value: `<Info>`/`<Warning>` for important callouts (timeouts, idempotency), `<Steps>` for sequential flows, `<CardGroup>`/`<Card>` for option sets, `<AccordionGroup>`/`<Accordion>` for reference tables.
- Link to reference endpoints with their generated slug: `/api-reference/<operationId>` (e.g. `/api-reference/list-brands`).

## Content boundaries

- Document the public Testbed and Production API surface only.
- Do not document internal-only endpoints, deprecated fields (e.g. `marketplacegift_id`, `TO_CHARITY`) beyond noting they are deprecated, or account-specific internal tooling.
