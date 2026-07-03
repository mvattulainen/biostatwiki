# SAP design-pattern taxonomy

| Design pattern | Typical statistical risks | Required SAP elements | Seen in |
| --- | --- | --- | --- |
| Single-arm performance goal | External validity, performance-goal justification, selection bias | Performance goal rationale, confidence interval method, sensitivity to threshold | Not present in current four SAPs |
| Randomized parallel-group | Randomization, treatment effect, missing data, multiplicity | Primary model, covariates, analysis sets, multiplicity | NCT05773781, NCT03340025, NO-NCT-IRAS286913 |
| Crossover | Period effects, carryover, within-subject correlation | Mixed model, sequence/period terms, carryover assessment | NCT04025762 |
| Diagnostic accuracy | Reference standard, indeterminate results, paired data | Sensitivity/specificity, CI method, reader effects, missing/invalid tests | Not present in current four SAPs |
| Post-market observational | Confounding, data completeness, generalizability | Descriptive plan, bias assessment, missingness, subgroup interpretation | Not present in current four SAPs |

Trusted-source anchor: ICH E9 identifies parallel-group, crossover, and other design configurations as having different assumptions and interpretation risks. Source: `ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf`, lines 586-638`. Semantic confidence: High.
