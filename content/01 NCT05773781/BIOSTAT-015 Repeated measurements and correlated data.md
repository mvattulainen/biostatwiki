---
study_name: PuraBond PROOF Study
nct_number: NCT05773781
source_sap: Prot_SAP_000_b.pdf
question_id: BIOSTAT-015
status: Partially supported
---

# BIOSTAT-015 Repeated measurements and correlated data

## Question

Does the analysis account for multiple lesions, multiple implants, bilateral organs, repeated visits, clustered sites, or repeated measurements within the same subject?

Question reference: [[Questions#BIOSTAT-015 Repeated measurements and correlated data]]

## Short SAP Evidence

The primary ANCOVA uses pre-surgical pain score as an adjusting covariate; repeated VAS visits are collected but not modeled longitudinally.

## Statistical Claim-to-Evidence

### Claim BIOSTAT-015-1: PuraBond PROOF Study is partially supported for repeated measurements and correlated data because correlation/repeated-measure implementation details may be incomplete

**Trusted source evidence:** ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 593-607. Semantic confidence: High.

> Repeated measurements, interactions, protocol violations, dropouts, and withdrawals can complicate analysis and interpretation. In crossover designs each subject is randomised to a treatment sequence and acts as his own control.

**SAP evidence:** Prot_SAP_000_b.pdf, lines 728-738. Semantic confidence: Medium.

> The primary ANCOVA uses pre-surgical pain score as an adjusting covariate; repeated VAS visits are collected but not modeled longitudinally.

**Status:** Partially supported

## Attribute assessment

Base this section on the complete SAP, not only the `Short SAP Evidence` section or the quoted SAP evidence in the claim block.

| Question attribute | Evidence found | Gap quality |
| --- | --- | --- |
| Correlation source | Repeated VAS assessments are collected over postoperative days 1, 2, 4, 7, 14, and 30, but the primary ANCOVA focuses on postoperative pain score. | Partly clear, but not fully reviewer-ready. |
| Model structure | ANCOVA for postoperative pain score with pre-surgical pain score as adjusting covariate; difference in means with two-sided 95% confidence intervals and p<0.05 | Partly clear, but not fully reviewer-ready. |
| Unit of analysis | ANCOVA for postoperative pain score with pre-surgical pain score as adjusting covariate; difference in means with two-sided 95% confidence intervals and p<0.05 | Partly clear, but not fully reviewer-ready. |
| Missing repeated measures | ANCOVA for postoperative pain score with pre-surgical pain score as adjusting covariate; difference in means with two-sided 95% confidence intervals and p<0.05 | Partly clear, but not fully reviewer-ready. |
| Interpretation of summary | ANCOVA for postoperative pain score with pre-surgical pain score as adjusting covariate; difference in means with two-sided 95% confidence intervals and p<0.05 | Partly clear, but not fully reviewer-ready. |

### Gap statement

Complete SAP review for PuraBond PROOF found evidence relevant to repeated measurements and correlated data in the protocol/SAP, as summarized in the attribute table. The gap quality judgment separates explicit SAP content from information that is only operational, inferable from surrounding sections, ambiguous for reviewer interpretation, or missing as a prespecified statistical rule.

## Same Question in Other SAP Evaluations
- [[02 NCT03340025/BIOSTAT-015 Repeated measurements and correlated data|NCT03340025 BIOSTAT-015 Repeated measurements and correlated data]]
- [[03 NO-NCT-IRAS286913/BIOSTAT-015 Repeated measurements and correlated data|NO-NCT-IRAS286913 BIOSTAT-015 Repeated measurements and correlated data]]
- [[04 NCT04025762/BIOSTAT-015 Repeated measurements and correlated data|NCT04025762 BIOSTAT-015 Repeated measurements and correlated data]]
