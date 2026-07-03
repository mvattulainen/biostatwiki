---
study_name: DAN06 Study
nct_number: NCT04025762
source_sap: SAP_001.pdf
question_id: BIOSTAT-010
status: Supported
---

# BIOSTAT-010 Multiplicity

## Question

How will type I error be controlled across multiple primary endpoints, co-primary endpoints, secondary endpoints, interim analyses, subgroups, and repeated looks at the data?

Question reference: [[Questions#BIOSTAT-010 Multiplicity]]

## Short SAP Evidence

FWER is controlled using fixed-sequence testing for key endpoints; FDR-adjusted p-values are planned for other secondary endpoints.

## Statistical Claim-to-Evidence

### Claim BIOSTAT-010-1: DAN06 Study is supported for multiplicity because multiplicity control is incomplete or should be checked against endpoint hierarchy

**Trusted source evidence:** MultipleEndpoints_FinalGuidance.pdf, lines 262-310. Semantic confidence: High.

> When there is more than one primary or secondary endpoint, it is important to ensure that multiple hypotheses do not inflate the overall Type I error rate. The analysis plan should describe the testing procedure with proper control.

**SAP evidence:** SAP_001.pdf, lines 175-195 and 444-470. Semantic confidence: High.

> FWER is controlled using fixed-sequence testing for key endpoints; FDR-adjusted p-values are planned for other secondary endpoints.

**Status:** Supported

## Attribute assessment

Base this section on the complete SAP, not only the `Short SAP Evidence` section or the quoted SAP evidence in the claim block.

| Question attribute | Evidence found | Gap quality |
| --- | --- | --- |
| Multiplicity sources | fixed-sequence gatekeeping controls FWER at two-sided alpha 0.05 for primary and key secondary endpoints; FDR-adjusted p-values are planned within other secondary endpoint categories | Mostly clear from complete SAP review. |
| Error-control method | fixed-sequence gatekeeping controls FWER at two-sided alpha 0.05 for primary and key secondary endpoints; FDR-adjusted p-values are planned within other secondary endpoint categories | Mostly clear from complete SAP review. |
| Endpoint hierarchy | fixed-sequence gatekeeping controls FWER at two-sided alpha 0.05 for primary and key secondary endpoints; FDR-adjusted p-values are planned within other secondary endpoint categories | Mostly clear from complete SAP review. |
| Interim or repeated looks | fixed-sequence gatekeeping controls FWER at two-sided alpha 0.05 for primary and key secondary endpoints; FDR-adjusted p-values are planned within other secondary endpoint categories | Mostly clear from complete SAP review. |
| Exploratory separation | fixed-sequence gatekeeping controls FWER at two-sided alpha 0.05 for primary and key secondary endpoints; FDR-adjusted p-values are planned within other secondary endpoint categories | Mostly clear from complete SAP review. |

### Gap statement

Complete SAP review shows a reviewer-ready multiplicity strategy for the primary and key secondary endpoint family: fixed-sequence gatekeeping controls FWER at two-sided alpha 0.05 and FDR adjustment is planned for other secondary categories. Remaining interpretation should still separate confirmatory endpoints from exploratory or descriptive analyses.

## Same Question in Other SAP Evaluations
- [[01 NCT05773781/BIOSTAT-010 Multiplicity|NCT05773781 BIOSTAT-010 Multiplicity]]
- [[02 NCT03340025/BIOSTAT-010 Multiplicity|NCT03340025 BIOSTAT-010 Multiplicity]]
- [[03 NO-NCT-IRAS286913/BIOSTAT-010 Multiplicity|NO-NCT-IRAS286913 BIOSTAT-010 Multiplicity]]
