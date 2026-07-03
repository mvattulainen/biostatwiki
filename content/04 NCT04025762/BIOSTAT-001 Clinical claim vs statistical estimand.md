---
study_name: DAN06 Study
nct_number: NCT04025762
source_sap: SAP_001.pdf
question_id: BIOSTAT-001
status: Partially supported
---

# BIOSTAT-001 Clinical claim vs statistical estimand

## Question

What exact clinical claim is the investigation intended to support, and what estimand defines that claim statistically?

Question reference: [[Questions#BIOSTAT-001 Clinical claim vs statistical estimand]]

## Short SAP Evidence

The SAP compares closed-loop insulin delivery with sensor augmented pump therapy and uses time in target glucose range as the primary endpoint.

## Statistical Claim-to-Evidence

### Claim BIOSTAT-001-1: DAN06 Study is partially supported for clinical claim vs statistical estimand because estimand attributes are not fully explicit

**Trusted source evidence:** ich-e9-r1-addendum-estimands-and-sensitivity-analysis-clinical-trials-guideline-statistical-principles-clinical-trials-step-5_en.pdf, lines 71-90. Semantic confidence: High.

> Precision in describing a treatment effect of interest is facilitated by constructing the estimand corresponding to a clinical question of interest. The statistical analysis of clinical trial data should be aligned to the estimand.

**SAP evidence:** SAP_001.pdf, lines 54-79. Semantic confidence: Medium.

> The SAP compares closed-loop insulin delivery with sensor augmented pump therapy and uses time in target glucose range as the primary endpoint.

**Status:** Partially supported

## Attribute assessment

Base this section on the complete SAP, not only the `Short SAP Evidence` section or the quoted SAP evidence in the claim block.

| Question attribute | Evidence found | Gap quality |
| --- | --- | --- |
| Treatment condition | all participants receive both closed-loop insulin delivery and sensor-augmented pump therapy in randomized order, separated by a four-week washout period | Mostly clear from complete SAP review. |
| Population | older adults with type 1 diabetes aged over 60 years who complete run-in competency/compliance requirements; approximately 36 randomized subjects | Mostly clear from complete SAP review. |
| Variable/endpoint | time spent in target glucose range 3.9 to 10.0 mmol/L over each 16-week treatment period, calculated from pooled CGM readings | Mostly clear from complete SAP review. |
| Intercurrent events | dropouts and reasons are tracked; adherence/retention analyses account for enrolled subjects, dropouts before/after randomization, and eligibility for primary analysis; explicit ICH E9(R1)-style intercurrent-event strategies are not specified. | Partly clear, but not fully reviewer-ready. |
| Population-level summary | Linear mixed model adjusting for period as fixed effect and site as random effect, accounting for within-subject correlation and reporting two-sided p-values and 95% confidence intervals. | Mostly clear from complete SAP review. |
| Missing data / analysis set | no imputation for primary, secondary CGM, insulin, or questionnaire analyses; primary inclusion requires at least 168 hours CGM data in at least one period; dropouts can be included if one period has enough data primary and secondary analyses are intention-to-treat by randomized treatment day; per-protocol primary analysis requires at least 60% CGM readings/control and 60% closed-loop use; safety includes all enrolled participants | Partly clear, but not fully reviewer-ready. |

### Gap statement

Complete SAP review shows that the clinical contrast is recoverable: open-label, multicentre, randomized, two-period crossover study comparing 16-week closed-loop insulin delivery with sensor-augmented pump therapy in older adults with type 1 diabetes. Treatment condition, population, endpoint concept, and broad summary measure are present, but the estimand is not presented as an explicit ICH E9(R1)-style construct tying endpoint timing, intercurrent events, missing data, and analysis population together in one reviewer-ready statement.

## Same Question in Other SAP Evaluations
- [[01 NCT05773781/BIOSTAT-001 Clinical claim vs statistical estimand|NCT05773781 BIOSTAT-001 Clinical claim vs statistical estimand]]
- [[02 NCT03340025/BIOSTAT-001 Clinical claim vs statistical estimand|NCT03340025 BIOSTAT-001 Clinical claim vs statistical estimand]]
- [[03 NO-NCT-IRAS286913/BIOSTAT-001 Clinical claim vs statistical estimand|NO-NCT-IRAS286913 BIOSTAT-001 Clinical claim vs statistical estimand]]
