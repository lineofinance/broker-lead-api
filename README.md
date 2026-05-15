# Lineo Broker Lead API

Public OpenAPI contract for the Lineo Finance broker lead onboarding integration.

## What this repo is

This repo is the canonical, public source for the OpenAPI specification that
broker partners integrate against. The spec is generated and pushed here
automatically from Lineo's internal application repo whenever a new version is
released — **do not edit files in this repo directly**, changes will be
overwritten on the next publish.

## Contents

- [`spec/openapi.yaml`](spec/openapi.yaml) — the OpenAPI 3 specification (YAML)
- [`spec/openapi.json`](spec/openapi.json) — same specification as JSON
- [`CHANGELOG.md`](CHANGELOG.md) — human-readable history of contract changes

## Versioning

The spec follows semantic versioning. Each release is tagged in this repo
(e.g. `v1.0.1`) and is also visible under
[Releases](https://github.com/lineofinance/broker-lead-api/releases). Integrators
can pin to a specific tag by using the raw URL of that tag, e.g.:

```
https://raw.githubusercontent.com/lineofinance/broker-lead-api/v1.0.1/spec/openapi.yaml
```

The current version is the one in
[`spec/openapi.yaml`](spec/openapi.yaml) under `info.version`.

## Quick start

To preview the spec rendered as HTML:

- Drop the YAML or its raw URL into <https://redocly.github.io/redoc/>, or
- Import it into Postman, Insomnia, Stoplight, Swagger Editor, or any
  OpenAPI-aware tool.

## Contact

Integration questions: <integrations@lineo.finance>
