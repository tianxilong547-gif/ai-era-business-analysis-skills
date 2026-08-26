---
name: verify-claim-sources
description: Verify factual claims and citations used in business analysis. Use for external facts, policies, product capabilities, market statements, or AI-generated claims whose source, date, scope, and wording must be checked.
---

# Verify claim sources

Treat each sentence as one or more atomic claims.

## Workflow

1. Split compound statements into independently verifiable claims.
2. Prefer primary/authoritative sources; record identity, date and access date.
3. Check exact scope, geography, population, time and wording.
4. Compare conflicts and explain likely differences.
5. Mark verified, partially supported, contradicted, outdated, or unavailable.
6. Rewrite to the strongest wording evidence allows.

## Output and boundaries

Return a claim-source ledger, usable wording, conflicts, freshness limits, and missing evidence. Never invent a URL, quotation, clause, statistic, or capability. If a source cannot be opened, mark it unverified and remove it from decision-ready conclusions.

Use [test cases](references/test-cases.md) when validating changes.
