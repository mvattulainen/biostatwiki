# Questions

## BIOSTAT-001 Clinical claim vs statistical estimand

**Question:** What exact clinical claim is the investigation intended to support, and what estimand defines that claim statistically?

Attribute reference: [[Question attributes#BIOSTAT-001 Clinical claim vs statistical estimand]]

**Impact:** If the clinical claim and estimand are not aligned, the SAP may analyze a quantity that does not answer the sponsor's intended device claim. Reviewers may then treat the result as difficult to interpret even when the endpoint analysis itself is technically correct.

Source: ich-e9-r1-addendum-estimands-and-sensitivity-analysis-clinical-trials-guideline-statistical-principles-clinical-trials-step-5_en.pdf, lines 71-90. Semantic confidence: High.

> Precision in describing a treatment effect of interest is facilitated by constructing the estimand corresponding to a clinical question of interest. The statistical analysis of clinical trial data should be aligned to the estimand.

## BIOSTAT-002 Primary endpoint definition

**Question:** Is the primary endpoint objectively defined, clinically meaningful, measurable, and aligned with the device's intended purpose?

Attribute reference: [[Question attributes#BIOSTAT-002 Primary endpoint definition]]

**Impact:** An imprecise or weakly justified primary endpoint can make a positive result clinically ambiguous. Reviewers need the endpoint definition to be objective, measurable, and tied to the intended purpose before they can judge whether the analysis supports benefit.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 300-323. Semantic confidence: High.

> There should be sufficient evidence that the primary variable can provide a valid and reliable measure of some clinically relevant and important treatment benefit. To avoid multiplicity concerns arising from post hoc definitions, it is critical to specify the precise definition of the primary variable.

## BIOSTAT-003 Endpoint timing

**Question:** At what time point should the primary endpoint be assessed, and is that time point clinically and statistically justified?

Attribute reference: [[Question attributes#BIOSTAT-003 Endpoint timing]]

**Impact:** Endpoint timing determines what clinical state the analysis actually measures. A statistically significant result at an arbitrary or poorly justified time point may not support the claimed duration, onset, or persistence of device benefit.

Source: ICH_E8-R1_Guideline_Step4_2021_1006.pdf, lines 247-256. Semantic confidence: High.

> Good planning and implementation derive from attention to clear objectives, appropriate participants, methods to minimise bias, and endpoints that are well-defined, measurable, clinically meaningful, and relevant to patients.

## BIOSTAT-004 Superiority, non-inferiority, equivalence, or performance goal

**Question:** Is the study testing superiority, non-inferiority, equivalence, or comparison against a performance goal, and is the margin or threshold justified?

Attribute reference: [[Question attributes#BIOSTAT-004 Superiority, non-inferiority, equivalence, or performance goal]]

**Impact:** The selected testing framework controls how success is interpreted. Without a clear superiority, non-inferiority, equivalence, or performance-goal rationale, reviewers cannot determine whether the decision rule protects against an unsupported effectiveness claim.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 762-823. Semantic confidence: High.

> Superiority, equivalence, and non-inferiority trials have different objectives. For equivalence or non-inferiority, the protocol should contain a clear statement of intention and a clinically justified margin.

## BIOSTAT-005 Performance goal justification

**Question:** If a single-arm study is used, what external data justify the performance goal, and are those data comparable to the planned population and endpoint?

Attribute reference: [[Question attributes#BIOSTAT-005 Performance goal justification]]

**Impact:** A single-arm performance goal is only as credible as the external data used to set it. Weak comparability between historical evidence and the planned study population can make the threshold look convenient rather than clinically justified.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 803-823. Semantic confidence: High.

> Active comparators should be chosen with care, with efficacy established and quantified in well designed trials. Equivalence margins should be specified and justified clinically.

## BIOSTAT-006 Comparator selection

**Question:** Is the chosen comparator, control device, sham, standard of care, or historical control appropriate for the clinical question?

Attribute reference: [[Question attributes#BIOSTAT-006 Comparator selection]]

**Impact:** Comparator choice affects bias, interpretability, and clinical relevance. An inappropriate control can make the treatment effect hard to attribute to the device or hard to generalize to actual clinical decision-making.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 762-808. Semantic confidence: High.

> The appropriateness of placebo control versus active control should be considered on a trial by trial basis. Active comparators should be chosen with care and should have relevant design features.

## BIOSTAT-007 Sample size

**Question:** Is the sample size sufficient for the primary effectiveness endpoint, safety endpoint, and any key precision requirements?

Attribute reference: [[Question attributes#BIOSTAT-007 Sample size]]

**Impact:** Sample size determines whether the study can answer its primary effectiveness question with adequate precision. It also limits how strongly safety and secondary findings can be interpreted, especially in small medical-device studies.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 878-899. Semantic confidence: High.

> The number of subjects in a clinical trial should always be large enough to provide a reliable answer to the questions addressed. The method by which sample size is calculated should be given with estimates and the basis of those estimates.

## BIOSTAT-008 Power assumptions

**Question:** Are assumptions about event rates, success rates, standard deviations, dropout, and treatment effect clinically plausible and evidence-based?

Attribute reference: [[Question attributes#BIOSTAT-008 Power assumptions]]

**Impact:** Power assumptions translate clinical expectations into statistical feasibility. If event rates, variability, dropout, or effect sizes are optimistic or uncited, reviewers may question whether the study was prospectively designed to provide reliable evidence.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 894-910. Semantic confidence: High.

> The basis of sample-size estimates should be given. It is important to investigate sensitivity of the sample size estimate to deviations from assumptions, and assumptions should normally be based on published data or earlier trials.

## BIOSTAT-009 Safety evidence sufficiency

**Question:** Is the study large enough and long enough to characterize important adverse events, device deficiencies, and procedure-related risks?

Attribute reference: [[Question attributes#BIOSTAT-009 Safety evidence sufficiency]]

**Impact:** Safety evidence requires enough exposure and follow-up to characterize important harms. A study powered only for effectiveness may still be too small or short to support strong safety conclusions.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 878-884. Semantic confidence: High.

> A trial sized on the basis of safety questions or important secondary objectives may need larger numbers of subjects than a trial sized on the basis of the primary efficacy question.

## BIOSTAT-010 Multiplicity

**Question:** How will type I error be controlled across multiple primary endpoints, co-primary endpoints, secondary endpoints, interim analyses, subgroups, and repeated looks at the data?

Attribute reference: [[Question attributes#BIOSTAT-010 Multiplicity]]

**Impact:** Multiplicity affects the false-positive risk across endpoints, subgroups, interim analyses, and repeated looks. Without a prespecified control strategy, apparently favorable findings may be treated as exploratory rather than confirmatory.

Source: MultipleEndpoints_FinalGuidance.pdf, lines 262-310. Semantic confidence: High.

> When there is more than one primary or secondary endpoint, it is important to ensure that multiple hypotheses do not inflate the overall Type I error rate. The analysis plan should describe the testing procedure with proper control.

## BIOSTAT-011 Missing data

**Question:** What missing-data mechanisms are anticipated, how will missing values be handled, and which sensitivity analyses will test robustness?

Attribute reference: [[Question attributes#BIOSTAT-011 Missing data]]

**Impact:** Missing data can change both bias and precision. If the SAP does not state the assumed missingness mechanism and sensitivity analyses, reviewers cannot judge whether conclusions are robust to plausible departures from the primary analysis assumptions.

Source: guideline-missing-data-confirmatory-clinical-trials_en.pdf, lines 57-96. Semantic confidence: High.

> Just ignoring missing data is not an acceptable option. The reason for missing data and handling of missing data represent critical factors, and robustness should be investigated through appropriate sensitivity analyses.

## BIOSTAT-012 Intercurrent events

**Question:** How will deaths, reinterventions, rescue therapy, device explants, crossovers, discontinuations, or alternative treatments be handled in the primary analysis?

Attribute reference: [[Question attributes#BIOSTAT-012 Intercurrent events]]

**Impact:** Intercurrent events define what outcome is being estimated when treatment is stopped, changed, rescued, or complicated by death or reintervention. If these events are handled only operationally, the clinical meaning of the treatment effect can remain ambiguous.

Source: ich-e9-r1-addendum-estimands-and-sensitivity-analysis-clinical-trials-guideline-statistical-principles-clinical-trials-step-5_en.pdf, lines 109-126. Semantic confidence: High.

> The addendum distinguishes discontinuation of randomised treatment from study withdrawal. The former is an intercurrent event to be addressed in the estimand; the latter gives rise to missing data.

## BIOSTAT-013 Analysis populations

**Question:** Which analysis sets will be used, such as intention-to-treat, modified ITT, per-protocol, as-treated, safety set, implanted set, evaluable set, or procedure-attempted set?

Attribute reference: [[Question attributes#BIOSTAT-013 Analysis populations]]

**Impact:** Analysis populations determine which subjects contribute to each claim. Exclusions after randomization or implantation can introduce bias unless the SAP explains how ITT, per-protocol, safety, and evaluable sets support distinct interpretations.

Source: ich-e9-r1-addendum-estimands-and-sensitivity-analysis-clinical-trials-guideline-statistical-principles-clinical-trials-step-5_en.pdf, lines 131-140. Semantic confidence: High.

> Analysis sets should be considered in the estimand framework because excluding planned measurements or subjects can mean randomisation is not fully preserved.

## BIOSTAT-014 Protocol deviations

**Question:** Which deviations will exclude subjects from per-protocol analyses, and can these rules be applied without introducing bias?

Attribute reference: [[Question attributes#BIOSTAT-014 Protocol deviations]]

**Impact:** Protocol-deviation rules can protect interpretability, but they can also create biased exclusions. Reviewers need prospective, objective rules to determine whether per-protocol analyses are supportive rather than selectively favorable.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 940-954. Semantic confidence: High.

> Data capture should focus on information necessary to implement the planned analysis, confirm protocol compliance, or identify important protocol deviations.

## BIOSTAT-015 Repeated measurements and correlated data

**Question:** Does the analysis account for multiple lesions, multiple implants, bilateral organs, repeated visits, clustered sites, or repeated measurements within the same subject?

Attribute reference: [[Question attributes#BIOSTAT-015 Repeated measurements and correlated data]]

**Impact:** Correlated observations violate simple independence assumptions. Multiple implants, bilateral organs, clustered sites, or repeated visits require analysis methods that account for within-subject or within-cluster dependence.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 593-607. Semantic confidence: High.

> Repeated measurements, interactions, protocol violations, dropouts, and withdrawals can complicate analysis and interpretation. In crossover designs each subject is randomised to a treatment sequence and acts as his own control.

## BIOSTAT-016 Site and operator effects

**Question:** Could outcomes vary by site, investigator, surgeon, operator, software reader, or learning curve, and how will this be modeled or assessed?

Attribute reference: [[Question attributes#BIOSTAT-016 Site and operator effects]]

**Impact:** Site, investigator, operator, and learning-curve effects can determine whether observed performance is reproducible beyond the study setting. Ignoring these effects may overstate generalizability or hide clinically important heterogeneity.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 720-759. Semantic confidence: High.

> Centre differences and treatment-by-centre heterogeneity can affect interpretation and generalisability. Mixed models may be used to explore heterogeneity when the number of sites is large.

## BIOSTAT-017 Diagnostic performance

**Question:** For diagnostic devices, are sensitivity, specificity, PPV, NPV, ROC/AUC, agreement, indeterminate results, and reference-standard uncertainty handled appropriately?

Attribute reference: [[Question attributes#BIOSTAT-017 Diagnostic performance]]

**Impact:** Diagnostic performance claims depend on reference standards, paired-data structure, and handling of indeterminate or invalid results. Weak specification can inflate accuracy estimates or obscure uncertainty in sensitivity and specificity.

Source: ICH_E8-R1_Guideline_Step4_2021_1006.pdf, lines 144-150. Semantic confidence: High.

> Clinical studies can concern therapeutic, preventative, or diagnostic products, and the drug term includes diagnostic medicinal products in the broad ICH E8 sense.

## BIOSTAT-018 Subgroup analyses

**Question:** Which subgroup analyses are prespecified, clinically justified, and powered or interpreted only as exploratory?

Attribute reference: [[Question attributes#BIOSTAT-018 Subgroup analyses]]

**Impact:** Subgroup analyses are prone to low power and false-positive findings. Unless prespecified and interpreted cautiously, they should inform hypothesis generation rather than support independent device claims.

Source: MultipleEndpoints_FinalGuidance.pdf, lines 290-327. Semantic confidence: High.

> Multiple analyses of subgroups can inflate Type I error if used to conclude benefit. Definitive conclusions should be prespecified and included in the multiple-testing strategy.

## BIOSTAT-019 Adaptive, Bayesian, or borrowing designs

**Question:** If the study uses interim adaptation, Bayesian priors, historical borrowing, or external controls, are operating characteristics, prior-data relevance, and decision rules prospectively justified?

Attribute reference: [[Question attributes#BIOSTAT-019 Adaptive, Bayesian, or borrowing designs]]

**Impact:** Adaptive, Bayesian, or borrowing designs can improve efficiency but require transparent prospective rules. Without operating characteristics, prior-data relevance, and decision criteria, reviewers may question type I error, bias, and interpretability.

Source: ich-e20-guideline-adaptive-designs-clinical-trials-step-2b_en.pdf, lines 107-126. Semantic confidence: High.

> An adaptive design allows prospectively planned modifications based on interim analysis of accumulating data. The focus is on planning, conduct, analysis, and interpretation so trials produce reliable and interpretable information.

## BIOSTAT-020 Generalizability and real-world evidence

**Question:** Do the investigation population, sites, operators, follow-up, and real-world data sources support generalization to the intended users, patients, and use environment?

Attribute reference: [[Question attributes#BIOSTAT-020 Generalizability and real-world evidence]]

**Impact:** Generalizability determines whether evidence from the investigation applies to intended users, patients, operators, and use environments. Limited sites, selected populations, or artificial follow-up can narrow the defensible claim.

Source: ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 668-699. Semantic confidence: High.

> Multicentre trials can provide a better basis for generalisation by recruiting from a wider population and broader clinical settings, but implementation should be clear and similar at all centres.
