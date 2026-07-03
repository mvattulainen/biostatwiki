# Lessons learned from medical-device SAPs

## Strong practices observed

1. Clear endpoint hierarchy improves interpretability when present.
2. Explicit analysis populations reduce ambiguity.
3. Randomization and masking details are often better specified than estimands.
4. Safety summaries are commonly described even when not powered.
5. Crossover designs benefit from explicit mixed-model handling of within-subject correlation.

## Recurring weaknesses

1. Estimands are rarely explicit.
2. Safety precision is often under-justified.
3. Multiplicity is inconsistently handled.
4. Missing-data assumptions are often not stress-tested.
5. Intercurrent events are often implicit rather than prespecified.

## Implications for future SAP authoring

Future SAPs should include an estimand table, a claim-to-endpoint traceability section, explicit missing-data sensitivity analyses, and a safety precision rationale even when the primary objective is performance or feasibility.
