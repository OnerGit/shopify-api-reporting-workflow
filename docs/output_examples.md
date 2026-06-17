# Output Examples

This repository includes public-safe output previews in `sample_outputs/`.

## Included previews

| File | What it shows |
|---|---|
| `report_preview.md` | A short run summary, output list, and validation warning examples |
| `report_preview_graphql.md` | A sanitized v0.2 GraphQL-shaped mock workflow report preview |
| `orders_cleaned_preview.csv` | A small cleaned order table preview |
| `customer_order_summary_preview.csv` | Customer-level order and gross sales summary shape |
| `sales_summary_by_month_preview.csv` | Monthly sales summary shape |
| `sales_summary_by_product_preview.csv` | Product-level sales summary shape |

## Intended client deliverables

A real client workflow could produce:

- cleaned order table;
- cleaned line item table;
- cleaned customer table;
- cleaned product table;
- customer order summary;
- sales by product;
- sales by month;
- validation report;
- Excel workbook;
- SQLite-style local reporting database.

## Public-safe preview policy

The preview files are intentionally small and sanitized. Full implementation and client-sensitive materials remain private, including:

- real Shopify order IDs;
- real customer names or emails;
- real store domains;
- access tokens or app configuration;
- full mock datasets;
- complete field mapping templates;
- private implementation paths.

## How to read the previews

The previews are meant to communicate output shape, not production completeness.

For example, a client can see that the workflow distinguishes cleaned order rows from customer summaries and product summaries. The exact columns, validation rules, and report definitions would be adapted to the store.

The GraphQL report preview shows how the v0.2 private workflow documents cursor-style pagination behavior at a case-study level. It does not include production GraphQL queries, connector code, credentials, store domains, or full mock fixtures.
