---
study_name: DAN06 Study
nct_number: NCT04025762
source_sap: SAP_001.pdf
question_id: BIOSTAT-015
status: Supported
---

# BIOSTAT-015 Repeated measurements and correlated data

## Question

Does the analysis account for multiple lesions, multiple implants, bilateral organs, repeated visits, clustered sites, or repeated measurements within the same subject?

Question reference: [[Questions#BIOSTAT-015 Repeated measurements and correlated data]]

## Short SAP Evidence

A linear mixed model adjusts for period, random site effect, and correlated data from the same subject.

## Statistical Claim-to-Evidence

### Claim BIOSTAT-015-1: DAN06 Study is supported for repeated measurements and correlated data because correlation/repeated-measure implementation details may be incomplete

**Trusted source evidence:** ich-e-9-statistical-principles-clinical-trials-step-5_en.pdf, lines 593-607. Semantic confidence: High.

> Repeated measurements, interactions, protocol violations, dropouts, and withdrawals can complicate analysis and interpretation. In crossover designs each subject is randomised to a treatment sequence and acts as his own control.

**SAP evidence:** SAP_001.pdf, lines 152-162. Semantic confidence: High.

> A linear mixed model adjusts for period, random site effect, and correlated data from the same subject.

**Status:** Supported

## Attribute assessment

Base this section on the complete SAP, not only the `Short SAP Evidence` section or the quoted SAP evidence in the claim block.

| Question attribute | Evidence found | Gap quality |
| --- | --- | --- |
| Correlation source | Crossover/repeated-period data are modeled with subject-level correlation accounted for in a mixed model. | Mostly clear from complete SAP review. |
| Model structure | linear mixed model adjusting for period as fixed effect and site as random effect, with baseline included as a third observation; model accounts for within-subject correlation and reports two-sided p-values and 95% confidence intervals | Mostly clear from complete SAP review. |
| Unit of analysis | linear mixed model adjusting for period as fixed effect and site as random effect, with baseline included as a third observation; model accounts for within-subject correlation and reports two-sided p-values and 95% confidence intervals | Mostly clear from complete SAP review. |
| Missing repeated measures | linear mixed model adjusting for period as fixed effect and site as random effect, with baseline included as a third observation; model accounts for within-subject correlation and reports two-sided p-values and 95% confidence intervals | Mostly clear from complete SAP review. |
| Interpretation of summary | linear mixed model adjusting for period as fixed effect and site as random effect, with baseline included as a third observation; model accounts for within-subject correlation and reports two-sided p-values and 95% confidence intervals | Mostly clear from complete SAP review. |

### Gap statement

Complete SAP review for DAN06 found evidence relevant to repeated measurements and correlated data in the protocol/SAP, as summarized in the attribute table. The gap quality judgment separates explicit SAP content from information that is only operational, inferable from surrounding sections, ambiguous for reviewer interpretation, or missing as a prespecified statistical rule.

## Same Question in Other SAP Evaluations
- [[01 NCT05773781/BIOSTAT-015 Repeated measurements and correlated data|NCT05773781 BIOSTAT-015 Repeated measurements and correlated data]]
- [[02 NCT03340025/BIOSTAT-015 Repeated measurements and correlated data|NCT03340025 BIOSTAT-015 Repeated measurements and correlated data]]
- [[03 NO-NCT-IRAS286913/BIOSTAT-015 Repeated measurements and correlated data|NO-NCT-IRAS286913 BIOSTAT-015 Repeated measurements and correlated data]]
