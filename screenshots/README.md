# Screenshot Guide

These screenshots support the public case study without exposing private code, full mock data, credentials, store domains, client data, or private paths.

Screenshots are included to show workflow shape, output quality, testing evidence, and handoff value while keeping the runnable implementation private.

## Current screenshots

| File | Purpose | README usage |
|---|---|---|
| `01_case_study_overview.png` | Optional visual overview of the public case study. | Not embedded |
| `02_cli_run_success.png` | Shows the v0.1 private REST-style mock workflow completing local pagination, extraction, validation, and report generation. | Embedded |
| `03_pytest_pass.png` | Shows private workflow tests passing, as evidence of implementation quality. | Embedded |
| `04_public_sample_outputs.png` | Shows the public-safe preview files included in this repository. | Embedded |
| `05_excel_workbook_preview.png` | Shows an Excel-style workbook with reporting-ready sheets and fake data. | Embedded |
| `06_report_preview.png` | Shows the sanitized Markdown report preview with run summary, outputs, validation notes, and limitations. | Embedded |
| `07_sqlite_tables_preview.png` | Shows normalized SQLite-style reporting tables and summary tables. | Embedded |
| `08_graphql_cli_run_success.png` | Shows the v0.2 private GraphQL-shaped mock workflow completing against fake local fixtures with cursor-style pagination. | Embedded |

The current public screenshot set covers the mock workflow and sanitized output previews. v0.3-v0.5 are represented through written summaries rather than additional screenshots.

## Public Safety

The screenshot set is curated to show case-study evidence while keeping implementation and client-sensitive material private. It avoids:

- local absolute paths;
- private repository names or private folder paths;
- user home directories;
- tokens, app secrets, passwords, access tokens, or bearer tokens;
- real Shopify store domains;
- real customer data;
- full mock fixtures;
- source code from the private implementation;
- production GraphQL query templates;
- development-store validation evidence that has not been manually sanitized;
- connector template internals, app identity values, or automation-token details.

## Recommended README Flow

The README presents screenshots as evidence for the case study rather than instructions for running this repository:

1. v0.1 mock workflow run evidence;
2. private test evidence;
3. public sample output preview;
4. Excel-style workbook preview;
5. Markdown report preview;
6. SQLite-style handoff preview;
7. v0.2 GraphQL-shaped mock workflow evidence.

## GraphQL v0.2 screenshot

`08_graphql_cli_run_success.png` documents the completed v0.2 private mock workflow. It is evidence of a local GraphQL-shaped case-study path that simulates `edges`, `node`, `cursor`, and `pageInfo` pagination with fake fixtures.

The screenshot represents the mock workflow only; real Shopify API validation and production connector work remain private delivery concerns.
