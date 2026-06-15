# Implementation Boundary

This repository is a public case-study repository. It is not the runnable implementation.

## Public repository includes

- README and documentation;
- sanitized sample output previews;
- screenshot checklist and placeholder guidance;
- Upwork portfolio summary material;
- article outline material.

## Private implementation includes

- runnable extraction, transformation, validation, and export code;
- local development fixtures;
- complete field mapping logic;
- store-specific configuration;
- client-specific reporting rules;
- any credential handling or API configuration.

## Not included publicly

The public repo must not include:

- `src/`, `tests/`, `scripts/`, `queries/`, dependency files, Docker files, or runnable Python code;
- real Shopify credentials, app tokens, access scopes, or store domains;
- real client data or production exports;
- complete mock datasets;
- complete field mapping templates;
- production connector code;
- private repository paths.

## Why this boundary exists

The case study should show the business problem, workflow shape, deliverables, and implementation judgment without exposing reusable private code or client-sensitive details.

The public material is designed to support portfolio review and client conversations. It should not be treated as a package, starter template, or implementation guide.
