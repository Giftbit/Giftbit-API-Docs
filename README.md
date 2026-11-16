# Giftbit API docs

The public documentation at [docs.giftbit.com](https://docs.giftbit.com) is built with Mintlify from the `mintlify/` directory. The API reference comes from `mintlify/api-reference/openapi.yaml`; guides and navigation are in `mintlify/guides/` and `mintlify/docs.json`.

Keep the legacy Apiary Blueprint, `apiary.apib`, in sync until it is retired.

## Local preview and checks

From `mintlify/`, run:

```sh
npx mint dev
npx mint broken-links
npx @redocly/cli lint api-reference/openapi.yaml
```

Submit changes through a pull request. Coordinate publication of API changes with the corresponding backend rollout.
