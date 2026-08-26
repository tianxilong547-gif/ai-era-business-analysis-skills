---
name: review-analysis-sql
description: Review analytical SQL for business-grain, join, filter, time, deduplication, denominator, null, safety, and reconciliation risks. Use when SQL supports a metric, report, experiment, or diagnostic conclusion.
---

# Review analytical SQL

Review correctness before performance polish.

## Workflow

1. Read metric card, output grain, schemas and sample rows.
2. Trace grain through joins; flag many-to-many multiplication.
3. Check date boundaries, timezone, status, nulls, deduplication and denominators.
4. Identify hidden hardcodes and unstable current-date logic.
5. Verify sensitive columns are necessary and authorized.
6. Propose reconciliation queries for row count, distinct key, totals, and alternate cuts.
7. Separate blocking correctness issues from performance/style.

## Output and boundaries

Return severity-ordered findings, affected result, corrected logic, and validation queries. Do not execute writes or production queries without authorization. Pause when schemas are missing, the query mutates data, credentials are present, or business rules cannot be inferred.

Use [test cases](references/test-cases.md) when validating changes.
