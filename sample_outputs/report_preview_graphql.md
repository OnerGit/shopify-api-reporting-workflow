# Shopify-style API Reporting Demo Report

## Run Summary

- Source format: mock_graphql
- Input directory: `data/mock_graphql`
- Output directory: `data/output/graphql`
- Date range: `2026-01-01` to `2026-03-31`
- Workflow: local GraphQL-shaped mock fixtures only
- No real Shopify API calls
- No OAuth
- No tokens
- No production connector

## Extraction Summary

- Orders: 4
- Order pages: 2
- Products: 4
- Customers: 4

## GraphQL Cursor Pagination

- GraphQL order pages: 2
- GraphQL order cursors processed: 4
- hasNextPage transitions: true -> false


## Output Files

- `sales_summary_by_month.csv`
- `sales_summary_by_product.csv`
- `customer_order_summary.csv`
- `orders_cleaned.csv`
- `line_items_cleaned.csv`
- `products_cleaned.csv`
- `customers_cleaned.csv`
- `shopify_reporting_demo.xlsx`
- `ecommerce_reporting.sqlite`
- `report.md`

## Validation Issues

- [warning] orders row `gid://shopify/Order/1004` field `customer_email`: Required field customer_email is blank
- [warning] orders row `gid://shopify/Order/1003` field `fulfillment_status`: Required field fulfillment_status is blank

## Limitations

- No real Shopify API calls.
- No OAuth, Admin API token handling, or production connector.
- Fake demo data only.
- No production GraphQL query templates or connector code.
