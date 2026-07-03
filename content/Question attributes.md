# Question attributes

This page defines the reusable attribute checklist for each BIOSTAT question. The SAP-specific evidence and gap quality judgments are recorded in each SAP evaluation page under `Attribute assessment`.

## BIOSTAT-001 Clinical claim vs statistical estimand

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Treatment condition | Intervention, comparator, device use, dose/regimen, and background treatment | Mostly clear when treatment and comparator are explicit and align with the objective |
| Population | Eligibility population and analysis population | Partly clear when eligibility is explicit but analysis population linkage is weak |
| Variable/endpoint | Endpoint variable, scale, timing, derivation, and baseline adjustment | Major gap when the primary endpoint can be interpreted multiple ways |
| Intercurrent events | Rescue treatment, withdrawal, discontinuation, reintervention, complications, death, missed visits, and device discontinuation | Major gap when no explicit strategy is given for events that can alter interpretation |
| Population-level summary | Difference in means, risk difference, odds ratio, hazard ratio, confidence interval, or hypothesis test | Partly clear when a model is given but the estimand summary is not explicitly named |
| Missing data / analysis set | ITT, modified ITT, per-protocol, complete case, imputation, and sensitivity analysis | Potential tension when missing-data handling does not preserve the intended estimand |

## BIOSTAT-002 Primary endpoint definition

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Endpoint concept | Clinical outcome, performance measure, safety measure, or diagnostic target | Mostly clear when the endpoint maps directly to the intended purpose |
| Operational definition | Scale, instrument, adjudication rule, numerator, denominator, and derivation | Major gap when different operational readings are possible |
| Clinical meaningfulness | Patient relevance, clinical threshold, or accepted performance construct | Partly clear when measurable but not clinically justified |
| Measurement objectivity | Blinding, objective instrumentation, central reading, or standardized assessment | Gap increases when subjective assessment is not protected against bias |
| Alignment with claim | Traceability from intended purpose to endpoint and analysis | Major gap when endpoint success would not support the claimed benefit |

## BIOSTAT-003 Endpoint timing

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Primary time point | Visit, window, follow-up duration, or index time | Mostly clear when a single analysis time point and window are explicit |
| Clinical timing rationale | Why the selected timing captures onset, durability, recovery, or risk | Gap increases when timing is stated but not justified |
| Windowing rules | Allowed visit windows and handling of out-of-window assessments | Partly clear when windows are operational but not tied to analysis |
| Repeated time points | Handling of multiple visits or longitudinal summaries | Major gap when several time points exist but the primary time point is ambiguous |
| Missing or delayed visits | Rules for missed, delayed, or early assessments | Major gap when visit timing interacts with missing-data handling |

## BIOSTAT-004 Superiority, non-inferiority, equivalence, or performance goal

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Testing framework | Superiority, non-inferiority, equivalence, or performance-goal framework | Mostly clear when the framework is explicitly named |
| Margin or threshold | Numerical margin, null value, performance goal, or success criterion | Major gap when no defensible threshold is specified |
| Clinical justification | Clinical, historical, or regulatory rationale for the margin or threshold | Partly clear when a number is given without justification |
| Statistical decision rule | Alpha, confidence interval, hypothesis test, and directionality | Major gap when the rule for success is not reproducible |
| Applicability to endpoint | Consistency between framework, endpoint type, and estimand | Gap increases when framework and endpoint are mismatched |

## BIOSTAT-005 Performance goal justification

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| External data source | Historical study, registry, literature, standard, or prior trial used to set the goal | Mostly clear when source and selection criteria are explicit |
| Population comparability | Similarity of eligibility, disease severity, device generation, care setting, and operators | Major gap when historical patients differ materially from planned patients |
| Endpoint comparability | Same endpoint definition, timing, ascertainment, and analysis metric | Major gap when endpoint definitions differ |
| Threshold derivation | How the performance goal value was calculated or selected | Partly clear when the value is stated but derivation is absent |
| Sensitivity to assumptions | Analyses testing alternative thresholds or external-data assumptions | Gap increases when no robustness check is planned |

## BIOSTAT-006 Comparator selection

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Comparator type | Control device, sham, standard care, placebo, no treatment, or historical control | Mostly clear when comparator type is explicit |
| Comparator relevance | Clinical relevance to the decision being supported | Gap increases when comparator does not match real clinical alternatives |
| Bias protection | Randomization, blinding, allocation concealment, concurrent control, or adjustment | Major gap when comparator choice creates uncontrolled bias |
| Treatment contrast | What treatment effect the comparator enables | Partly clear when contrast is inferable but not stated |
| External-control comparability | If historical or external, comparability of population, endpoint, timing, and care context | Major gap when external control comparability is not justified |

## BIOSTAT-007 Sample size

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Effectiveness sample size | Planned N and calculation for the primary effectiveness endpoint | Mostly clear when N, assumptions, alpha, and power are explicit |
| Safety precision | Exposure and precision for adverse events or device deficiencies | Gap increases when N is justified only for effectiveness |
| Attrition allowance | Dropout, missing data, non-evaluable subjects, and replacement assumptions | Partly clear when attrition is mentioned without sensitivity |
| Key precision requirement | Confidence interval width, event-rate precision, or estimation target | Major gap when precision expectations are absent |
| Feasibility vs evidence | Whether N is evidence-driven rather than convenience-driven | Major gap when sample size is justified only by feasibility |

## BIOSTAT-008 Power assumptions

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Event or success rates | Rates used in sample-size or power calculations | Mostly clear when rates are cited and plausible |
| Variability assumptions | Standard deviations, correlations, or distributional assumptions | Gap increases when variability is not evidence-based |
| Effect size | Expected treatment difference, margin, or clinically important difference | Major gap when effect size is optimistic or unsupported |
| Dropout or missingness | Assumed attrition and missing-data impact | Partly clear when dropout is included but not justified |
| Assumption sensitivity | Sensitivity of power or sample size to alternative assumptions | Major gap when no robustness of assumptions is shown |

## BIOSTAT-009 Safety evidence sufficiency

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Safety population | Who contributes to safety analyses and exposure denominators | Mostly clear when safety set and denominators are explicit |
| Follow-up duration | Duration adequate for expected adverse events and device deficiencies | Gap increases when follow-up is too short for important risks |
| Adverse-event capture | Severity, seriousness, relatedness, device deficiency, and procedure-relatedness | Partly clear when events are listed but coding/summarization is thin |
| Rare-event precision | What adverse-event rates the sample size can reasonably detect or bound | Major gap when safety interpretation exceeds sample size |
| Benefit-risk linkage | How safety findings will qualify effectiveness conclusions | Gap increases when safety is disconnected from the review claim |

## BIOSTAT-010 Multiplicity

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Multiplicity sources | Multiple endpoints, time points, interim looks, subgroups, or analyses | Mostly clear when all testing families are identified |
| Error-control method | Hierarchy, gatekeeping, alpha split, fallback, closed testing, or adjustment method | Major gap when confirmatory claims lack type I error control |
| Endpoint hierarchy | Primary, secondary, exploratory, and safety endpoint ordering | Partly clear when labels exist but testing order is absent |
| Interim or repeated looks | Alpha spending or rules for repeated analyses | Major gap when repeated looks are planned without adjustment |
| Exploratory separation | Clear separation of exploratory findings from confirmatory claims | Gap increases when exploratory results could be overclaimed |

## BIOSTAT-011 Missing data

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Missing-data sources | Expected missing visits, withdrawal, death, device issues, noncompliance, or unusable data | Mostly clear when sources are anticipated prospectively |
| Primary handling method | Complete case, imputation, model-based handling, weighting, or retrieval strategy | Partly clear when a method is stated without assumptions |
| Missingness assumption | MCAR, MAR, MNAR, treatment-policy, hypothetical, or other assumption | Major gap when the assumption behind the method is unstated |
| Sensitivity analyses | Tipping-point, MNAR, pattern-mixture, worst-case, or alternative assumptions | Major gap when robustness to informative missingness is not tested |
| Safety missingness | Handling and summarization of missing safety or exposure data | Gap increases when only effectiveness missingness is addressed |

## BIOSTAT-012 Intercurrent events

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Intercurrent-event types | Death, rescue therapy, reintervention, explant, crossover, discontinuation, alternative treatment, or withdrawal | Mostly clear when relevant events are prospectively listed |
| Estimand strategy | Treatment policy, hypothetical, composite, while-on-treatment, or principal-stratum strategy | Major gap when events are collected but no analysis strategy is given |
| Endpoint impact | How each event affects endpoint definition and interpretation | Gap increases when events can alter the clinical meaning of response |
| Analysis implementation | Rules for coding, censoring, imputation, exclusion, or composite failure | Partly clear when operational handling is present but not tied to estimand |
| Sensitivity or supportive analyses | Alternative event strategies or robustness analyses | Major gap when no alternative interpretation is tested |

## BIOSTAT-013 Analysis populations

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Analysis-set definitions | ITT, modified ITT, per-protocol, as-treated, safety, implanted, evaluable, or attempted-procedure set | Mostly clear when each set has inclusion/exclusion rules |
| Claim-to-set alignment | Which analysis set supports each effectiveness, safety, or performance claim | Gap increases when sets are defined but not tied to claims |
| Post-randomization exclusions | Exclusions after randomization, implantation, or procedure attempt | Major gap when exclusions may break comparability |
| Safety denominators | Exposure-based and treated-subject denominators | Partly clear when safety set is named but denominator rules are thin |
| Sensitivity across sets | Supportive analyses comparing ITT, per-protocol, and other sets | Gap increases when conclusions depend on one narrow set |

## BIOSTAT-014 Protocol deviations

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Deviation taxonomy | Major, minor, inclusion/exclusion, treatment, assessment, timing, or compliance deviations | Mostly clear when deviations are prospectively categorized |
| Exclusion rules | Which deviations remove subjects or data from per-protocol/evaluable analyses | Major gap when exclusion rules are retrospective or subjective |
| Bias risk | Whether deviation handling could introduce treatment-related or outcome-related selection | Gap increases when exclusions occur after outcomes are known |
| Blinded review | Blinded deviation review before database lock or unblinding | Partly clear when process is stated but not protected from bias |
| Sensitivity analyses | Analyses retaining/excluding deviations to assess robustness | Gap increases when deviation impact is not tested |

## BIOSTAT-015 Repeated measurements and correlated data

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Correlation source | Multiple lesions, implants, eyes, sites, operators, visits, or repeated measures | Mostly clear when clustering/repetition is identified |
| Model structure | Mixed model, GEE, clustered variance, repeated-measures covariance, or subject random effect | Major gap when correlated data are analyzed as independent |
| Unit of analysis | Subject, lesion, implant, eye, visit, site, or device unit | Partly clear when unit is inferable but not explicit |
| Missing repeated measures | Handling of missed visits or incomplete longitudinal records | Gap increases when longitudinal missingness is not specified |
| Interpretation of summary | Time-specific, overall, area-under-curve, change-from-baseline, or responder summary | Major gap when repeated measures exist but summary is ambiguous |

## BIOSTAT-016 Site and operator effects

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Site effects | Number of sites and site-level heterogeneity | Mostly clear when site effects are modeled or summarized |
| Operator effects | Investigator, surgeon, reader, technician, or learning-curve effects | Gap increases when specialized operator skill could influence outcomes |
| Modeling approach | Fixed effects, random effects, stratification, interaction, or descriptive heterogeneity analysis | Partly clear when adjustment is stated without rationale |
| Minimum data per site/operator | Sparse-site rules and pooling decisions | Major gap when site/operator effects are impossible to assess but claims generalize broadly |
| Generalizability impact | Whether results are reproducible across intended settings and users | Gap increases when study performance may reflect selected operators |

## BIOSTAT-017 Diagnostic performance

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Accuracy measures | Sensitivity, specificity, PPV, NPV, ROC/AUC, agreement, or likelihood ratios | Mostly clear when measures match the diagnostic claim |
| Reference standard | Definition, timing, adjudication, and uncertainty in the reference standard | Major gap when reference-standard validity is not addressed |
| Indeterminate/invalid results | Handling of equivocal, invalid, missing, or unreadable tests | Gap increases when excluded results could inflate accuracy |
| Paired-data structure | Within-subject paired comparisons, reader effects, or repeated specimens | Partly clear when design is described but correlation is ignored |
| Precision and thresholds | Confidence intervals, diagnostic thresholds, and decision cutoffs | Major gap when accuracy estimates lack uncertainty or prespecified thresholds |

## BIOSTAT-018 Subgroup analyses

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Prespecified subgroups | Subgroups defined before analysis with clinical rationale | Mostly clear when subgroups and rationale are explicit |
| Power and precision | Whether subgroup analyses are powered or exploratory | Major gap when underpowered subgroup findings support claims |
| Multiplicity handling | Adjustment or exploratory labeling for multiple subgroup tests | Gap increases when many subgroups are tested without control |
| Interaction analysis | Treatment-by-subgroup interaction rather than within-subgroup p-values only | Partly clear when subgroup summaries are planned but interaction is absent |
| Interpretation limits | Rules preventing overinterpretation of favorable subgroup findings | Gap increases when subgroup claims are not constrained |

## BIOSTAT-019 Adaptive, Bayesian, or borrowing designs

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Adaptive feature | Interim adaptation, sample-size re-estimation, enrichment, stopping rule, Bayesian prior, borrowing, or external control | Mostly clear when the design feature is prospectively specified |
| Decision rules | Timing, data used, boundaries, posterior thresholds, or adaptation algorithms | Major gap when adaptations are discretionary |
| Operating characteristics | Type I error, power, bias, precision, and simulation assumptions | Major gap when performance is not demonstrated prospectively |
| Prior or external-data relevance | Similarity and commensurability of borrowed/historical data | Gap increases when borrowing could overwhelm current evidence |
| Information control | Blinding, firewalls, DMC roles, and interim confidentiality | Partly clear when governance is described but analysis impact is not |

## BIOSTAT-020 Generalizability and real-world evidence

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Target population | Intended patients, indications, severity, eligibility, and exclusions | Mostly clear when enrolled population matches intended use |
| Sites and users | Clinical sites, operators, readers, settings, and use environment | Gap increases when evidence comes from narrow or expert-only settings |
| Follow-up and care context | Duration, visit schedule, standard care, and real-world care compatibility | Partly clear when follow-up is adequate but care context is artificial |
| Representativeness | Demographic, clinical, geographic, and disease-spectrum diversity | Major gap when selected participants limit the claim |
| Real-world data quality | Source reliability, completeness, confounding, and fitness for purpose | Gap increases when RWE is used without data-quality or bias assessment |
