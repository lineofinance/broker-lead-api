# Changelog

All notable changes to the Lineo Broker Lead API are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.2] – 2026-05-15

### Fixed
- Section headers in the `info.description` no longer use backticks. Redoc was
  double-processing them and rendering literal `<code>` tags in the navigation
  and section titles. Cosmetic only — no contract change.

## [1.0.1] – 2026-05-15

- Initial public release of the broker lead onboarding contract.
