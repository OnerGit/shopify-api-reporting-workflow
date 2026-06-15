# Screenshot Guide

These screenshots support the public case study without exposing private code, full mock data, credentials, store domains, client data, or private paths.

The public repository is a case-study repository. Screenshots are included to show workflow shape, output quality, testing evidence, and handoff value while keeping the runnable implementation private.

## Current screenshots

| File                            | Purpose                                                                                                                               | README usage |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| `01_case_study_overview.png`    | Optional README overview screenshot. Useful as a preview asset, but not required inside the README because it repeats README content. | Not embedded |
| `02_cli_run_success.png`        | Shows the private workflow completing local mock pagination, extraction, validation, and report generation.                           | Embedded     |
| `03_pytest_pass.png`            | Shows automated tests passing for the private workflow implementation.                                                                | Embedded     |
| `04_public_sample_outputs.png`  | Shows the public-safe preview files included in the public repo.                                                                      | Embedded     |
| `05_excel_workbook_preview.png` | Shows an Excel-style workbook with reporting-ready sheets.                                                                            | Embedded     |
| `06_report_preview.png`         | Shows the sanitized Markdown report preview with run summary, outputs, validation notes, and limitations.                             | Embedded     |
| `07_sqlite_tables_preview.png`  | Shows normalized SQLite-style reporting tables and summary tables.                                                                    | Embedded     |

## Recommended README order

Use the screenshots in this order:

1. `02_cli_run_success.png`
2. `03_pytest_pass.png`
3. `04_public_sample_outputs.png`
4. `05_excel_workbook_preview.png`
5. `06_report_preview.png`
6. `07_sqlite_tables_preview.png`

`01_case_study_overview.png` can stay in the folder as an optional overview asset, but it does not need to be embedded in the README.

## Screenshot-specific notes

### `02_cli_run_success.png`

This screenshot should show:

* local mock workflow start;
* two order pages loaded;
* four orders collected across two pages;
* workflow completed;
* validation issues count.

It should not show absolute local paths, private repository paths, credentials, or real store data.

### `03_pytest_pass.png`

This screenshot should show automated tests passing.

The recommended terminal command for a clean screenshot is:

```powershell
function prompt { "PS> " }
Clear-Host
pytest -q
```

The screenshot should focus on the test result rather than local machine details.

### `04_public_sample_outputs.png`

This screenshot should show public preview files from the public repository:

```powershell
function prompt { "PS> " }
Clear-Host
Get-ChildItem .\sample_outputs | Select-Object Name,Length
```

Expected preview files include:

* `report_preview.md`
* `orders_cleaned_preview.csv`
* `sales_summary_by_month_preview.csv`
* `sales_summary_by_product_preview.csv`
* `customer_order_summary_preview.csv`

The screenshot should reflect the public repository layout, not the private asset-generation path.

### `05_excel_workbook_preview.png`

This screenshot should show workbook tabs or sheets such as:

* `Orders`
* `Line Items`
* `Products`
* `Customers`
* `Sales by Month`
* `Sales by Product`
* `Customer Summary`

Use fake demo data only. Crop out any window title or address bar if it shows local paths.

### `06_report_preview.png`

This screenshot should show sections such as:

* Run Summary
* Extraction Summary
* Output Files
* Validation Issues
* Limitations

The screenshot should use `sample_outputs/report_preview.md` from the public repository or another sanitized preview.

### `07_sqlite_tables_preview.png`

This screenshot should show normalized tables such as:

* `orders`
* `line_items`
* `products`
* `customers`
* `sales_summary_by_month`
* `sales_summary_by_product`
* `customer_order_summary`

Crop out any full local database path.

## Capture rules

Before terminal screenshots, use:

```powershell
function prompt { "PS> " }
Clear-Host
```

Do not show:

* local absolute paths;
* private repository names or private folder paths;
* Windows user directories;
* Linux or macOS temporary or home directories;
* tokens, app secrets, passwords, access tokens, or bearer tokens;
* real Shopify store domains;
* real customer data;
* full mock fixtures;
* source code from the private implementation.

## Final screenshot checklist

Before committing screenshots, inspect each image manually and confirm:

* no private repository path is visible;
* no token or credential is visible;
* no real store domain is visible;
* no real client data is visible;
* the screenshot proves a useful case-study point;
* the README references only screenshots that exist.

Then run a text-file scan for Markdown and CSV files:

```powershell
Get-ChildItem . -Recurse -File | Select-String -SimpleMatch -Pattern 'local absolute path','private repository path','myshopify.com','shpat_','access_token','client_secret','Bearer ','password','secret','credentials'
```

This scan does not read image text, so screenshots still require manual visual review.
