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

| Question attribute | Evidence found | Gap quality |
| --- | --- | --- |
| Correlation source | The SAP evidence states: A linear mixed model adjusts for period, random site effect, and correlated data from the same subject. | Mostly clear from current evidence. |
| Model structure | Not explicitly identified in current SAP evidence excerpt. | No major gap identified from current evidence. |
| Unit of analysis | Not explicitly identified in current SAP evidence excerpt. | No major gap identified from current evidence. |
| Missing repeated measures | Not explicitly identified in current SAP evidence excerpt. | No major gap identified from current evidence. |
| Interpretation of summary | Not explicitly identified in current SAP evidence excerpt. | No major gap identified from current evidence. |

### Gap statement

The main gap quality judgment is: None. The SAP evidence provides some basis for assessing repeated measurements and correlated data where noted in the table, but the reviewer-facing weakness is the difference between information that is explicitly specified and information that must be reconstructed from partial SAP wording.

## Same Question in Other SAP Evaluations
- [[01 NCT05773781/BIOSTAT-015 Repeated measurements and correlated data|NCT05773781 BIOSTAT-015 Repeated measurements and correlated data]]
- [[02 NCT03340025/BIOSTAT-015 Repeated measurements and correlated data|NCT03340025 BIOSTAT-015 Repeated measurements and correlated data]]
- [[03 NO-NCT-IRAS286913/BIOSTAT-015 Repeated measurements and correlated data|NO-NCT-IRAS286913 BIOSTAT-015 Repeated measurements and correlated data]]
