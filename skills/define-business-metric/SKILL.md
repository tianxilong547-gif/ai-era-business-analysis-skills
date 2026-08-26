---
name: define-business-metric
description: Define, reconcile, and freeze business metric logic before analysis. Use when a metric is ambiguous, teams report different values, or numerator, denominator, grain, time, deduplication, and exclusions need agreement.
---

# Define a business metric

Build a metric card and conflict matrix covering meaning, formula, numerator/denominator, unit, grain, time/timezone, deduplication key, valid states, exclusions, source, owner, version, and limitations.

## Workflow

1. Inventory every definition and its intended decision.
2. Quantify how definitions differ and change results.
3. Do not merge definitions that answer different questions.
4. Recommend a primary definition only with a decision-specific reason.
5. Record unresolved choices and the human owner who must freeze them.
6. Preserve version/effective date; never silently overwrite an old metric.

## Output and boundaries

Return the metric card, conflicts, result impact, proposed primary/secondary definitions, and confirmation items. Pause if authoritative definitions conflict, no owner exists, or the definition affects compensation, compliance, or external reporting. Never infer a denominator or filter from a name alone.

Use [test cases](references/test-cases.md) when validating changes.
