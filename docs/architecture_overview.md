# Architecture Overview

This public repository describes the architecture at a case-study level only. It does not include implementation code.

## Conceptual components

```text
Shopify-style API layer
    -> extraction and pagination boundary
    -> normalization and field mapping layer
    -> validation layer
    -> reporting table layer
    -> export and handoff layer
```

## Extraction and pagination boundary

The extraction boundary is responsible for collecting order, customer, product, and line-item records from a Shopify-style source.

The private case-study implementation has two documented demo paths:

- v0.1 REST-style mock path for simple paginated API-shaped fixtures;
- v0.2 GraphQL-shaped mock path that simulates connection pagination with `edges`, `node`, `cursor`, and `pageInfo` shapes.

Both paths use fake local fixtures only. Neither path calls the real Shopify API, stores credentials, or exposes production connector code in this public repository.

In a real Shopify project, this layer would need to use the Shopify GraphQL Admin API, approved access scopes, cursor pagination, retry handling, and secure credential storage.

See [graphql_workflow_summary.md](graphql_workflow_summary.md) and [rest_to_graphql_mock_migration_summary.md](rest_to_graphql_mock_migration_summary.md) for public-safe v0.2 notes.

## Evidence and connector boundary

Later private milestones are documented publicly only as summaries:

- v0.3 covers development-store validation planning and sanitized evidence boundaries;
- v0.4 covers a private connector template at a high level, including security and redaction boundaries;
- v0.5 covers client delivery workflow planning and optional extension decisions.

These summaries keep the focus on architecture, evidence quality, and delivery boundaries. Runnable code, live Shopify access material, connector templates, detailed request and response payloads, app identity values, automation-token handling, and client-specific delivery assets are maintained privately.

## Normalization and mapping layer

Nested e-commerce objects are transformed into reporting-friendly tables. Store-specific mapping decisions belong here, such as how to treat discounts, refunds, shipping, product variants, fulfillment status, location, sales channel, and custom fields.

The public repo does not include a full mapping template because real stores differ and complete templates can expose implementation detail.

## Validation layer

Validation checks confirm whether key reporting fields are present and usable before the outputs are handed off.

Example validation categories:

- missing customer email where required for reporting;
- blank fulfillment status;
- missing product identifiers;
- unexpected currency or tax fields;
- incomplete order date values.

## Reporting table layer

The workflow produces reporting-friendly tables such as cleaned orders, customer summaries, product summaries, and monthly sales summaries.

Only small preview files are included in this public repo.

## Export and handoff layer

The final deliverables are designed for a client who needs files they can inspect:

- CSV previews;
- Excel-style workbook concept;
- SQLite-style handoff concept;
- Markdown report preview;
- validation notes.
