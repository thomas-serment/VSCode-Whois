# Changelog

All notable changes to this project are documented in this file.
The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and this project adheres to [Semantic Versioning](https://semver.org/).

## [1.1.3] - 2026-10-06

### Changed

- Updated the development toolchain to its latest versions (TypeScript 7, and the VS Code typings)
- Requires VS Code 1.140 or later, and the Node typings and the release build now target Node 24, the version VS Code 1.140 runs
- Updated the GitHub Actions of the release workflow

### Removed

- ESLint and the lint step of the release workflow, TypeScript strict mode and the tests are the checks

## [1.1.2] - 2026-10-03

### Changed

- Account renamed to thomas-serment: publisher, author and repository links updated

## [1.1.1] - 2026-10-02

### Changed

- Repository renamed to VSCode-Whois and display name prefixed with VSCode

## [1.1.0] - 2026-10-02

### Added

- Registration summary from RDAP: registrar, dates, days left before expiry, status, name servers and DNSSEC
- DNS records grouped by type (A, AAAA, CNAME, MX, NS, TXT, SOA, CAA) with copy buttons
- Search field in the panel, recent lookups and support for internationalized domain names
- Right-click a selected domain or URL in any editor to look it up
- Subdomains such as `www.example.co.uk` resolve to their registered domain
- Automated tests

### Fixed

- DNS record values were injected as HTML in the panel: a crafted TXT record could run script. The panel now renders text only and has a strict content security policy
- Failed lookups were only logged to the console: errors now appear in the panel
- The extension activated on the wrong command
- Domain input is validated, and URLs or e-mail addresses are reduced to their host name

### Changed

- WHOIS queries use the IANA referral and follow the registrar server, without the `whois` dependency
- DNS records are queried type by type instead of the unreliable ANY query
- Command renamed to `codewhois.lookup`, interface and messages are now in English
- Rewritten in TypeScript
- Requires VS Code 1.120 or later

## [1.0.123] - 2024-08-04

### Changed

- Packaging update
