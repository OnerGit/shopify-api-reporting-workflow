# Workflow Overview

The workflow is designed around a practical client handoff: extract, validate, map, export, and explain.

## Step 1: Define reporting questions

Before implementation, the report definitions need to be agreed:

- Which date range should be used?
- Should sales be grouped by order date, payment date, fulfillment date, or refund date?
- Should gross sales, net sales, taxes, shipping, discounts, and refunds be shown separately?
- Which customer fields are required?
- Which product and variant fields are needed?

## Step 2: Extract Shopify-style records

The private implementation demonstrates a repeatable extraction pattern using sanitized API-shaped data.

In a real Shopify project, extraction would need to be adapted to Shopify GraphQL Admin API access, cursor pagination, app scopes, and store-specific resource needs.

## Step 3: Normalize nested records

Nested records are flattened into reporting-friendly tables:

- orders;
- line items;
- customers;
- products;
- summary tables.

The goal is to make the output usable in CSV, Excel, SQLite-style analysis, or downstream reporting tools.

## Step 4: Validate key fields

The workflow checks required reporting fields and records warnings before delivery.

Validation does not make business assumptions disappear. It makes them visible so the client can decide how missing or inconsistent data should be handled.

## Step 5: Export deliverables

The private workflow can produce deliverables shaped like:

- cleaned CSV tables;
- multi-sheet Excel-style workbook;
- SQLite-style database file;
- Markdown report;
- summary CSV files.

Only small sanitized preview files are committed here.

## Step 6: Handoff and iteration

The final handoff should document:

- included outputs;
- known validation warnings;
- field mapping assumptions;
- date and metric definitions;
- next adaptations needed for the actual store.
