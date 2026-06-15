# Client Work Mapping

This case study maps to common Upwork and small-business data requests.

## Client request: recurring Shopify exports

Possible implementation scope:

- define required order, customer, and product fields;
- extract records for a recurring date range;
- export cleaned CSV or Excel deliverables;
- document validation warnings.

## Client request: sales summary by month or product

Possible implementation scope:

- map order and line-item fields;
- define sales metric assumptions;
- group by month, product, variant, or sales channel;
- produce summary CSV and Excel-style outputs.

## Client request: API data cleanup before reporting

Possible implementation scope:

- normalize nested API responses;
- standardize column names;
- flag missing required fields;
- separate raw-like input handling from reporting-ready outputs.

## Client request: lightweight reporting handoff

Possible implementation scope:

- deliver cleaned CSV files;
- deliver an Excel workbook;
- deliver a SQLite-style local database;
- provide a short handoff report with assumptions and warnings.

## Questions to ask before a real project

- Which Shopify resources are required?
- Which access scopes are approved?
- Which dates define the reporting period?
- How should refunds, discounts, taxes, and shipping be represented?
- Are customer emails or names required, and how should privacy be handled?
- Should the deliverable be CSV, Excel, database, dashboard-ready tables, or all of these?
- How often should the workflow run?
