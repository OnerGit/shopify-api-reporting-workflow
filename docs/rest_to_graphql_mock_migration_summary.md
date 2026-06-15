# REST To GraphQL Mock Migration Summary

The REST-style v0.1 path remains intact in the private implementation. The v0.2 path adds a GraphQL-shaped mock workflow that normalizes fake local connection-style records into the same reporting-ready output shape.

## What changed in v0.2

- the mock input shape moves closer to GraphQL connections;
- order pagination is represented with local `edges`, `node`, `cursor`, and `pageInfo` structures;
- the public report preview documents cursor-style pagination behavior;
- the output concept remains client-facing CSV, Excel-style, SQLite-style, and report handoff material.

## What did not change

- no real Shopify API calls;
- no OAuth flow;
- no tokens or credentials;
- no real store domains;
- no client data;
- no public production connector code;
- no public full mock fixtures or field mapping templates.

The purpose of the migration is case-study realism, not a public implementation release.
