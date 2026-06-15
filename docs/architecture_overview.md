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

In a real Shopify project, this layer would need to use the Shopify GraphQL Admin API, approved access scopes, cursor pagination, retry handling, and secure credential storage.

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
