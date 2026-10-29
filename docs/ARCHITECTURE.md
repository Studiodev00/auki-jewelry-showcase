# Architecture

React components render the catalog and administrative workflows. Route handlers apply validation and authorization before invoking domain services. Drizzle connects these services to local PGlite; a PostgreSQL adapter is prepared. The request service persists the request before notification, tracks uncertainty/failure and supports controlled recovery.

```text
Catalog → favorites/bag → request form → validated request service → persistence
Persistence → notification transport → delivery status → owner follow-up
```

## Design rationale

Integer-cent arithmetic avoids floating-point pricing errors. Server-side totals prevent trusting browser prices. Bounded pagination limits catalog work. Separating persistence from email prevents a transport failure from silently losing a request.

## Boundaries

The declared production build now passes after a minimal route-signature correction. Real notification delivery, hosting and a PostgreSQL deployment were not exercised. The current storefront is Portuguese, not fully bilingual. Previously recorded browser and Lighthouse results remain historical.

The diagram is an explanatory abstraction of inspected source, not a deployment topology or operational runbook. [Overview](../README.md).
