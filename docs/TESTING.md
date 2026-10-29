# Testing

Evidence date: October 29, 2026 (America/New_York). These results come from earlier recorded runs. The five-project package refresh reviewed the receipts and original-file hashes; it did not rerun application tests, lint or builds. Tests ran in isolated private copies using existing installed dependencies; no dependency reinstall was performed. JavaScript checks used Node 24.22.1.

| Check | Result |
|---|---|
| Vitest | 151 tests in 7 files passed |
| ESLint | PASS |
| TypeScript | PASS |
| Declared production build (Next.js / Turbopack) | PASS in an isolated local copy |
| npm dependency audit | 0 reported vulnerabilities |

## Historical evidence

October 27 request-flow report: 186 passing tests (151 unit/integration, 24 browser regression, 5 delivery, 6 request-flow checks). Lighthouse homepage medians across three local runs per profile: performance 95 mobile / 100 desktop; accessibility 100/100; best practices 100/100; SEO 66/66 with intentional noindex. These browser and Lighthouse results were inspected, not rerun today.

## Reproducibility and limits

The source is private, so these tests cannot be run from this documentation repository. The owner retains command receipts and redacted logs separately. Tests used fixtures/mocks without production credentials. No database migration, real email or Discord operation was authorized or executed.

The declared production build now passes after a minimal route-signature correction. Real notification delivery, hosting and a PostgreSQL deployment were not exercised. The current storefront is Portuguese, not fully bilingual. Previously recorded browser and Lighthouse results remain historical.

A dependency audit is a dated registry observation, not proof of exploitability or a security certification. No coverage percentage is claimed. [Overview](../README.md).

## Build correction

The disabled checkout and shipping handlers now require the Request argument expected by generated Next.js route types. Their existing HTTP 410 behavior is unchanged. The isolated build used real local dependency directories, an ephemeral synthetic authentication secret, an in-memory local database setting and disabled outbound delivery. No production server was started. The validated two-file correction was applied locally after retaining verified original backups.
