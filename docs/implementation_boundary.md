# Implementation Boundary

This repository is a public case-study repository. It is not the runnable implementation.

## Public repository includes

- README and documentation;
- sanitized sample output previews;
- screenshot guide and public-safe screenshot notes.

## Private implementation includes

- runnable extraction, transformation, validation, and export code;
- local development fixtures;
- REST-style v0.1 and GraphQL-shaped v0.2 mock workflow paths;
- development-store validation notes and sanitized evidence review from v0.3;
- private connector template planning and redaction helpers from v0.4;
- client delivery workflow templates and optional extension planning from v0.5;
- complete field mapping logic;
- store-specific configuration;
- client-specific reporting rules;
- any credential handling or API configuration.

## Kept Private

The public case study keeps these materials private:

- `src/`, `tests/`, `scripts/`, `queries/`, dependency files, Docker files, or runnable Python code;
- real Shopify credentials, app tokens, access scopes, or store domains;
- real client data or production exports;
- complete mock datasets;
- complete field mapping templates;
- GraphQL query templates;
- connector templates or detailed request and response examples;
- app identity values or automation-token details;
- live development-store validation evidence unless it has been manually sanitized for public release;
- Google Sheets, PostgreSQL, scheduler, dashboard, webhook, or cloud integration code;
- production connector code;
- private repository paths.

## Why this boundary exists

The case study should show the business problem, workflow shape, deliverables, and implementation judgment without exposing reusable private code or client-sensitive details.

The public material is designed to support portfolio review and client conversations. It is a case study, not a package, starter template, or implementation guide.
