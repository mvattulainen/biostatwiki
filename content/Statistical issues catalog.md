# Statistical issues catalog

| Failure mode | Description | Seen in | Severity | Why it matters | Recommended fix |
| --- | --- | --- | --- | --- | --- |
| FM-001 | Estimand absent or incomplete | NCT05773781, NCT03340025, NO-NCT-IRAS286913, NCT04025762 | High | Ambiguous interpretation of treatment effect | Add estimand table with population, treatment condition, endpoint, intercurrent events, and summary measure |
| FM-002 | Safety sample size not justified | NCT05773781, NCT03340025, NO-NCT-IRAS286913, NCT04025762 | Medium | Safety conclusions may be overstated | Add adverse-event precision rationale |
| FM-003 | Multiplicity unclear | NCT05773781, NCT03340025, NO-NCT-IRAS286913 | High | Risk of unsupported confirmatory claims | Add endpoint hierarchy and FWER/FDR strategy |
| FM-004 | Missing-data sensitivity weak | NCT05773781, NCT03340025, NO-NCT-IRAS286913, NCT04025762 | Medium | Results may depend on untested assumptions | Add sensitivity or tipping-point analysis |
| FM-005 | Repeated-measure structure under-specified | NCT05773781, NCT03340025, NO-NCT-IRAS286913 | Medium | Correlation and visit timing can affect inference | Specify mixed model or repeated-measures method |
