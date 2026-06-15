# Limitations

This repository is intentionally narrow.

## Not a runnable project

There is no public source code, package configuration, dependency file, test suite, Docker setup, or command-line workflow.

The runnable implementation is kept outside this public case-study repository.

## Not a Shopify app

This is not a Shopify embedded app, public app, custom app scaffold, OAuth flow, webhook service, or production Admin API connector.

## Not a complete API integration guide

The documentation describes workflow concepts, not a step-by-step connector implementation.

A real integration would need secure handling for:

- Shopify Admin API credentials;
- approved access scopes;
- cursor pagination;
- rate limits;
- retries;
- privacy-sensitive customer fields;
- store-specific reporting definitions.

## Not a complete mapping specification

The repo does not include full field mapping templates. Real Shopify reporting often depends on store-specific decisions for:

- product variants;
- refunds;
- discounts;
- taxes;
- shipping;
- fulfillment status;
- sales channel;
- locations;
- custom attributes.

## Not a replacement for business metric definitions

Gross sales, net sales, taxes, discounts, refunds, and shipping must be defined with the client before report numbers are treated as final.

The workflow can make those assumptions explicit, but it cannot decide them automatically.
