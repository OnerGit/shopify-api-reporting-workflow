# Screenshot Guide

These screenshots support the public case study without exposing private code, full mock data, credentials, store domains, client data, or private paths.

The public repository is a portfolio case study. Screenshots should prove the workflow shape, output quality, testing evidence, and handoff value while keeping the runnable implementation private.

## Current screenshots

| File | Purpose | Status |
|---|---|---|
| `01_case_study_overview.png` | Optional README overview screenshot. Useful for social or portfolio previews, but not required inside the README because it repeats the README content. | Optional |
| `02_cli_run_success.png` | Shows the private workflow completing local mock pagination, extraction, validation, and report generation. | Recommended |
| `03_pytest_pass.png` | Shows automated tests passing for the private workflow implementation. | Recommended, but retake or crop if it shows the private repo path |
| `04_public_sample_outputs.png` | Shows the public-safe preview files included in the public repo. | Recommended, but retake if the command points to `data/public_export` instead of `sample_outputs` |
| `05_excel_workbook_preview.png` | Shows an Excel-style workbook with reporting-ready sheets. | Recommended |
| `06_report_preview.png` | Shows the sanitized Markdown report preview with run summary, outputs, validation notes, and limitations. | Recommended |
| `07_sqlite_tables_preview.png` | Shows normalized SQLite-style reporting tables and summary tables. | Recommended |

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

Should show:

- local mock workflow start;
- two order pages loaded;
- four orders collected across two pages;
- workflow completed;
- validation issues count.

It should not show the absolute private repository path.

### `03_pytest_pass.png`

Best command:

```powershell
function prompt { "PS> " }
Clear-Host
pytest -q
```

This keeps the screenshot focused on the test result and avoids exposing `rootdir`.

If using normal `pytest`, crop out any line that shows a private path such as `E:\projects\...`.

### `04_public_sample_outputs.png`

Best command from the public repo:

```powershell
function prompt { "PS> " }
Clear-Host
Get-ChildItem .\sample_outputs | Select-Object Name,Length
```

The screenshot should show public preview files such as:

- `report_preview.md`
- `orders_cleaned_preview.csv`
- `sales_summary_by_month_preview.csv`
- `sales_summary_by_product_preview.csv`
- `customer_order_summary_preview.csv`

Avoid showing `data/public_export` in this screenshot because that is a private repo generation path, not the final public repo layout.

### `05_excel_workbook_preview.png`

Should show workbook tabs or sheets such as:

- `Orders`
- `Line Items`
- `Products`
- `Customers`
- `Sales by Month`
- `Sales by Product`
- `Customer Summary`

Use fake demo data only. Crop out any window title or address bar if it shows the private path.

### `06_report_preview.png`

Should show sections such as:

- Run Summary
- Extraction Summary
- Output Files
- Validation Issues
- Limitations

The screenshot should use `sample_outputs/report_preview.md` from the public repo or another sanitized preview.

### `07_sqlite_tables_preview.png`

Should show normalized tables such as:

- `orders`
- `line_items`
- `products`
- `customers`
- `sales_summary_by_month`
- `sales_summary_by_product`
- `customer_order_summary`

Crop out any full local database path.

## Capture rules

Before terminal screenshots, use:

```powershell
function prompt { "PS> " }
Clear-Host
```

Do not show:

- absolute private paths such as `E:\projects\shopify-api-reporting-workflow-private`;
- Windows user directories such as `C:\Users\...`;
- Linux/macOS paths such as `/mnt/data`, `/tmp`, or `/home`;
- tokens, app secrets, passwords, access tokens, or bearer tokens;
- real Shopify store domains;
- real customer data;
- full mock fixtures;
- source code from the private implementation.

## Final screenshot checklist

Before committing screenshots, inspect each image manually and confirm:

- no private repository path is visible;
- no token or credential is visible;
- no real store domain is visible;
- no real client data is visible;
- the screenshot proves a useful portfolio point;
- the README references only screenshots that exist.

Then run a text-file scan for Markdown and CSV files:

```powershell
Get-ChildItem . -Recurse -File | Select-String -SimpleMatch -Pattern 'E:\projects\shopify-api-reporting-workflow-private','E:\','C:\','Users\','/mnt/data','/tmp/','/home/','myshopify.com','shpat_','access_token','client_secret','Bearer ','password','secret','credentials'
```

This scan does not read image text, so screenshots still require manual visual review.
