# Verified features

- Search, category filters, bounded catalog pagination, product details and image enlargement.
- Favorites and shopping bag quantities/totals; prices are represented in integer cents and checked on the server.
- Product creation/editing/archiving, photo management, categories, editorial content and private previews.
- Order request: bag → contact information → review → request → owner follow-up. No online charges; legacy payment/shipping endpoints are disabled.
- Request persistence and notification state are separate. Email delivery has disabled, simulated and configured-provider modes.
- Responsive Portuguese interface. Full English localization was not found and is not advertised.

## Evidence level

These capabilities were found in the private source and related local records. Execution receipts exist for the checks listed in [Testing](TESTING.md); this package refresh reviewed those records without rerunning the applications. Presence in code, enabled configuration and live operation are different claims.

## Limits

The declared production build now passes after a minimal route-signature correction. Real notification delivery, hosting and a PostgreSQL deployment were not exercised. The current storefront is Portuguese, not fully bilingual. Previously recorded browser and Lighthouse results remain historical.

## Visual evidence

Owner-approved historical local storefront captures. They show the desktop/mobile presentation and do not demonstrate the newer request form or a live store.

[Overview and screenshots](../README.md).
