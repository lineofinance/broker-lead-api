# Changelog

All notable changes to the Lineo Broker Lead API are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] – 2026-05-15

### Changed
- **`hrb_court` is now a strict enum of XJustiz GDS.Gerichte codes**
  (the official XÖV codelist, 150 German courts, e.g. `D2601` =
  Amtsgericht München) instead of a free-form string, on both
  `RegisterLeadRequest` and `CreateConnectionRequest`. Defined once as
  the shared `XJustizGerichtsId` schema. Only string codes from the
  list are accepted — missing, unknown, or numeric values are rejected
  with `422`.

  ⚠️ **Breaking for any caller that sent free-form court names**
  (e.g. the previous `"Amtsgericht München"` example value is no longer
  valid — send `D2601`). Released as a minor bump rather than `2.0.0`
  because the only onboarded partner (Vivid) already sends XJustiz
  codes, so no live integration is affected; flagged here explicitly so
  future partners are not surprised.

## [1.0.3] – 2026-05-15

### Fixed
- `revocation_reason` enum now includes `null` so the documented
  `null`-for-active-connections value validates under OpenAPI 3.0
  (`nullable: true` + `enum` requires `null` in the enum list). Spec
  correctness only — no behavioural change.

## [1.0.2] – 2026-05-15

### Fixed
- Section headers in the `info.description` no longer use backticks. Redoc was
  double-processing them and rendering literal `<code>` tags in the navigation
  and section titles. Cosmetic only — no contract change.

## [1.0.1] – 2026-05-15

- Initial public release of the broker lead onboarding contract.
