---
name: assess-data-quality
description: Assess whether business-analysis data is fit for a decision. Use before analysis or when duplicates, missing values, inconsistent periods, late data, sample bias, or irreproducible results may affect conclusions.
---

# Assess data quality

Run completeness, uniqueness, validity, consistency, timeliness, representativeness, and reproducibility checks.

## Workflow

1. Read the metric card and expected grain.
2. Reconcile expected vs actual rows, entities, dates and coverage.
3. Test key duplication, valid states, ranges, units and nulls.
4. Compare cross-table and cross-period definitions.
5. Record refresh/month-close status and sample selection.
6. Recalculate representative outputs independently.
7. For every defect, state direction, magnitude, treatment, residual risk, and whether it blocks the decision.

## Output and boundaries

Return a quality report and verdict: fit, fit with limitations, or not fit. Do not silently drop outliers or impute critical values. Stop downstream conclusions when a defect can reverse direction, sensitive data lacks authorization, or grain cannot be established.

Use [test cases](references/test-cases.md) when validating changes.
