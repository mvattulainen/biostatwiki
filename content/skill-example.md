---
name: biostat-sap-review
description: Review every statistical analysis plan in the local GNO `saps` collection against the 20 biostatistical questions in questions.yml, using only trusted-source evidence from the local GNO `biostat` collection, and write Obsidian-friendly markdown outputs under wiki/.
---

# Biostat SAP Review

Use this skill when asked to review statistical analysis plans, SAPs, clinical investigation statistical methods, or the biostatistics wiki outputs in this repository.

## Scope

- Analyze every SAP in the local GNO collection `saps`.
- Identify each SAP by NCT number. If no NCT number is available, use `NO-NCT-[short source identifier]` and record the missing NCT number as a gap.
- Use only the local GNO collection `biostat` for trusted-source evidence.
- Do not browse the web or use sources outside the two GNO collections unless the user explicitly changes the scope.
- Load the 20 review questions from `questions.yml`.
- Create `wiki/index.md` if it is missing. Leave existing `wiki/index.md` content unchanged.

## GNO Retrieval

Use GNO MCP tools when exposed by the runtime. If MCP tools are unavailable, use the equivalent `gno` CLI commands.

1. Use `gno_query` first for normal retrieval.
2. Use `gno_search` for exact NCT numbers, identifiers, document IDs, requirement IDs, standard numbers, product names, and quoted phrases.
3. For retrieval via CLI, use the tested low-fallback pattern:

   ```bash
   gno query "<question or claim text>" -c biostat -n 5 -C 6 --no-expand --json --explain
   gno query "<NCT number, SAP section, question, or claim text>" -c saps -n 5 -C 6 --no-expand --json --explain
   ```

   Use the equivalent MCP options when exposed: collection filter, JSON/explain output, candidate limit 6, expansion disabled, and reranking enabled when available. Do not print internal retrieval commands or URIs in generated wiki pages.
4. Treat rerank as successful only when the JSON metadata shows `"reranked": true` and the explain results contain `rerankScore`. The explain line `fallbacks=expansion_disabled` is expected when `--no-expand` is used and does not invalidate rerank. Any `fallbacks=rerank_error`, missing `rerankScore`, or `"reranked": false` means rerank failed for that query.
5. Do not use GNO rerank score as the published confidence. The LLM must assess confidence as `Low`, `Medium`, or `High`, meaning the degree to which the quoted paragraph semantically matches the search string or claim being supported. Use `High` only when the quoted paragraph directly addresses the claim; use `Medium` when it supports the claim indirectly or partially; use `Low` when it is weakly related and retained only as the best available evidence.
6. If rerank fails after retrying with `-C 6 --no-expand`, use `gno_search` or the best available non-rerank retrieval result for evidence selection, but still report only the LLM-assessed semantic confidence: `Low`, `Medium`, or `High`.
7. Use `gno_get` or `gno_multi_get` to fetch exact passages before writing.
8. Preserve source filename or human-readable source identifier, page/line/heading anchors when available, and verbatim paragraph extracts.
9. Under evidence fields, aim to quote 2 complete relevant paragraphs from each source: the highest-match paragraph and the second-highest-match paragraph. If only 1 relevant paragraph is available, quote that complete paragraph. Do not reduce evidence to 1 or 2 sentences when a complete relevant paragraph is available.
10. Keep quoted paragraphs focused on the claim and avoid excessive copied material.
11. If the local collections do not support a claim, write `Insufficient evidence`.
12. Do not make unsupported claims.
13. GNO is an internal retrieval mechanism, not a published citation format. In generated wiki pages, do not print `gno://...` URIs, raw GNO command lines, or reproducible GNO queries. Cite sources by document title, source filename or SAP identifier, and location details when available.

Use collection filters:

- SAP evidence: `saps`
- Trusted-source evidence: `biostat`

## Output Layout

Write outputs under `wiki/`.

For each SAP, create one folder:

```text
wiki/
+-- index.md
+-- Trusted sources.md
+-- 01 NCT04025762/
    +-- BIOSTAT-001 Clinical claim and estimand.md
    +-- BIOSTAT-002 Primary endpoint definition.md
    +-- ...
    +-- BIOSTAT-020 Generalizability and RWE.md
    +-- BIOSTAT-021 Reviewer card.md
    +-- BIOSTAT-022 SAP completeness checklist.md
+-- Questions.md
+-- Question attributes.md
+-- Fair use.md
+-- Site review.md
+-- Cross-SAP statistical comparison matrix.md
+-- Statistical issues catalog.md
+-- Reviewer question bank.md
+-- Estimand reconstruction table.md
+-- Design patterns.md
+-- Lessons learned.md
+-- Strong and weak patterns/
    +-- BIOSTAT-001 Clinical claim and estimand.md
    +-- ...
    +-- BIOSTAT-020 Generalizability and RWE.md
```

Folder names use a two-digit sequence and the NCT number. Preserve stable folder names on later passes.

## Question Notes

Create one note for each item in `questions.yml`.

Each `BIOSTAT-001` to `BIOSTAT-020` note must include:

```markdown
---
study_name:
nct_number:
source_sap:
question_id:
status:
---

# BIOSTAT-000 Question title

## Question

Question reference: [[Questions#BIOSTAT-000 Question title]]

## Short SAP Evidence

## Statistical Claim-to-Evidence

### Claim 000-1: Full claim title with no truncation

Do not add a separate `Statistical claim` subsection. The claim is stated in full in the claim title.

**Trusted source evidence:** Source document title or source filename, exact location if available, and semantic confidence `Low`, `Medium`, or `High`.

> Quote the highest-match complete paragraph and the second-highest-match complete paragraph from the trusted source. If only 1 relevant paragraph is available, quote that complete paragraph.

**SAP evidence:** Source SAP identifier or filename, exact location if available, and semantic confidence `Low`, `Medium`, or `High`.

> Quote the highest-match complete paragraph and the second-highest-match complete paragraph from the SAP. If only 1 relevant paragraph is available, quote that complete paragraph.

**Status:** Supported | Partially supported | Contradicted | Missing | Insufficient evidence | Not applicable

## Attribute assessment

| Question attribute | Evidence found | Gap quality |
| --- | --- | --- |

### Gap statement

Write one specific paragraph explaining the gap quality judgment for this question in this SAP. The statement must distinguish between absence of evidence and partial/reconstructable evidence. For BIOSTAT-001, explain whether treatment, population, variable/endpoint, intercurrent events, population-level summary, and missing data or analysis set are explicit, recoverable, ambiguous, or missing. For other questions, adapt the attributes to the question.

## Same Question in Other SAP Evaluations

- [[OTHER NCT CODE BIOSTAT-000 Question title]]
```

Use these evidence statuses only:

- `Supported`
- `Partially supported`
- `Contradicted`
- `Missing`
- `Insufficient evidence`
- `Not applicable`

Every material claim in the note must have at least one evidence claim block under `## Statistical Claim-to-Evidence`. Every claim block must include a full, untruncated claim title, trusted-source evidence, SAP evidence, and status. Evidence fields must include the source document title or source filename, exact location if available, semantic confidence `Low`, `Medium`, or `High`, and complete relevant quoted paragraphs as described in the GNO retrieval rules. Do not include `gno://...` URIs or raw GNO commands in the generated page.

Do not include separate `Gap` or `Challenging the gap` subsections or fields in BIOSTAT-001 to BIOSTAT-020 notes. Gap interpretation belongs only in `## Attribute assessment` and its `### Gap statement`.

For `## Attribute assessment`, read the full original SAP and the full relevant trusted source context before writing. Include a table with exactly these columns:

```markdown
| Question attribute | Evidence found | Gap quality |
| --- | --- | --- |
```

Choose question-specific attributes rather than repeating the same generic attributes on every page. For BIOSTAT-001, use estimand-oriented attributes such as treatment condition, population, variable/endpoint, intercurrent events, population-level summary, and missing data / analysis set. For other questions, use attributes that decompose that question's statistical issue, for example endpoint definition components, timing components, sample-size assumptions, multiplicity controls, missing-data assumptions, intercurrent-event strategies, analysis populations, protocol-deviation rules, repeated-measure correlation structure, site/operator handling, diagnostic accuracy elements, subgroup prespecification, adaptive/Bayesian decision rules, or generalizability/RWE components.

Under the table, add `### Gap statement` and write one paragraph. The paragraph should synthesize what is explicit, what is recoverable from context, what is ambiguous, and what is missing. Avoid generic boilerplate.

After each `## Question` section in BIOSTAT-001 to BIOSTAT-020 notes, add a link to the exact matching question section in `Questions.md` using an Obsidian heading link:

```markdown
Question reference: [[Questions#BIOSTAT-001 Clinical claim vs statistical estimand]]
```

Use the exact BIOSTAT code and question title for the anchor.

At the end of each BIOSTAT-001 to BIOSTAT-020 note, include `## Same Question in Other SAP Evaluations`. Add Obsidian links to the same BIOSTAT question in other SAP folders. If no other SAP evaluation exists yet, write `No other SAP evaluations available yet.`

## Reviewer Card

`BIOSTAT-021 Reviewer card.md` contains reviewer talking points, not a long report.

Include:

- Study name and NCT number
- One-paragraph review stance
- Highest-priority talking points
- Questions to ask the sponsor or study team
- Claims that appear well supported
- Claims needing caution because evidence is missing, partial, or contradicted

## Completeness Checklist

`BIOSTAT-022 SAP completeness checklist.md` assesses coverage of the 20 questions.

Use one row per question:

```markdown
| ID | Topic | Covered in SAP | Evidence quality | Main gap | Note |
| --- | --- | --- | --- | --- | --- |
```

Use `Yes`, `Partial`, `No`, or `Not applicable` for `Covered in SAP`.

## Vault-Level Pages

Create these pages directly under `wiki/`, the same folder as `index.md`.

### Questions.md

Present the questions from `questions.yml`. For each question, include a unique `Impact` section specific to that question's statistical and reviewer consequences. Do not reuse generic impact language across questions. Elaborate the impact using trusted-source evidence from the `biostat` collection. Include complete relevant quoted paragraphs as described in the GNO retrieval rules, with source identifier, exact location if available, and semantic confidence `Low`, `Medium`, or `High`. Do not include `gno://...` URIs or raw GNO commands.

For each question section in `Questions.md`, include an Obsidian heading link to the matching section in `Question attributes.md`:

```markdown
Attribute reference: [[Question attributes#BIOSTAT-001 Clinical claim vs statistical estimand]]
```

Use the exact BIOSTAT code and question title for the anchor.

### Question attributes.md

Create and maintain this page directly under `wiki/`.

For each of the 20 questions, create one section with the BIOSTAT code and question title. Each section defines the question-specific attributes that should be assessed in that question's BIOSTAT pages. Use the attributes as a reusable checklist, not as a substitute for SAP-specific evidence review.

Use this format for each question:

```markdown
## BIOSTAT-001 Clinical claim vs statistical estimand

| Question attribute | What to look for | Gap quality guidance |
| --- | --- | --- |
| Treatment condition | Intervention, comparator, device use, dose/regimen, background treatment | Mostly clear when treatment and comparator are explicit and align with the objective |
| Population | Eligibility population and analysis population | Partly clear when eligibility is explicit but analysis population linkage is weak |
| Variable/endpoint | Endpoint variable, scale, timing, derivation, baseline adjustment | Major gap when the primary endpoint can be interpreted multiple ways |
| Intercurrent events | Analgesia, rescue treatment, withdrawal, reoperation, complications, death, missed visits, device discontinuation | Major gap when no explicit strategy is given for events that can alter interpretation |
| Population-level summary | Difference in means, risk difference, odds ratio, hazard ratio, CI, hypothesis test | Partly clear when a model is given but the estimand summary is not explicitly named |
| Missing data / analysis set | ITT, modified ITT, per protocol, complete case, imputation, sensitivity analysis | Potential tension when missing-data handling does not preserve the intended estimand |
```

Replace the example content with attribute lists tailored to all 20 questions. Attributes must be grounded in the question text and trusted-source concepts from `biostat`, but the page should remain concise.

### Trusted sources.md

Create and maintain this page directly under `wiki/`. Do not use table format. Present trusted sources as one markdown section per source. Generate the inventory from `gno ls biostat --json` or the equivalent GNO MCP listing. The section heading must be the document title exactly as it appears in the original source, not a paraphrase. Use GNO internally to fetch metadata and the quoted abstract or summary, but do not print `gno://...` URIs or raw GNO commands.

Each source section must include:

- Exact document title from the original source
- Author(s) exactly as listed in the original document
- Number of times the trusted source is referred to elsewhere in the `wiki/` folder
- Year
- Quoted abstract or summary from the local GNO source text
- Notes about its review use

Use this format:

```markdown
## Document title

**Author:** ...

**Referenced elsewhere in wiki:** 0

**Year:** ...

**Quoted abstract or summary:**

> Complete abstract or concise source-summary paragraph from the local source text.

**Notes:** ...
```

### Fair use.md

Create this page if it is missing. Explain why limited quotation of SAPs and trusted sources is used for review, scholarship, comparison, and critique. State that the page is maintained by the human author. Do not rewrite this page after creation.

### skill-example.md

Do not create, edit, rewrite, normalize, delete, or lint `wiki/skill-example.md`. This page is maintained fully by the human user.

### Method index.md

Do not create or maintain `Method index.md`. If `wiki/Method index.md` exists during a generation or cleanup pass, remove it unless the user explicitly asks to preserve it.

### Cross-SAP statistical comparison matrix.md

Create and maintain:

```markdown
# Cross-SAP statistical comparison matrix

| Question ID | Topic | SAP 1 | SAP 2 | SAP 3 | SAP 4 | Best example | Common weakness | Reviewer concern |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| BIOSTAT-001 | Clinical claim / estimand | Partial | Weak | Strong | Partial | SAP 3 | Estimand not explicit | Claim not statistically anchored |
| BIOSTAT-007 | Sample size | Strong | Partial | Weak | Strong | SAP 1 | Safety precision often missing | Underpowered safety interpretation |
| BIOSTAT-010 | Multiplicity | Weak | N/A | Partial | Strong | SAP 4 | Exploratory endpoints not separated | Inflated type I error |
| BIOSTAT-011 | Missing data | Partial | Weak | Strong | Partial | SAP 3 | MNAR sensitivity missing | Robustness unclear |
```

Replace example content with findings from the generated SAP evaluations.

### Statistical issues catalog.md

Create and maintain:

```markdown
| Failure mode | Description | Seen in | Severity | Why it matters | Recommended fix |
| --- | --- | --- | --- | --- | --- |
| FM-001 | Estimand absent | SAP defines endpoint but not treatment condition/intercurrent-event strategy | SAP 1, SAP 2 | High | Ambiguous interpretation of treatment effect | Add estimand table |
| FM-002 | Safety sample size not justified | Sample size only supports effectiveness endpoint | SAP 2, SAP 3 | Medium | Safety conclusions may be overstated | Add adverse-event precision rationale |
| FM-003 | Multiplicity unclear | Multiple endpoints listed without testing hierarchy | SAP 1, SAP 3 | High | Risk of unsupported confirmatory claims | Add endpoint hierarchy/FWER strategy |
| FM-004 | Missing-data sensitivity weak | Primary method given, but no robustness analysis | SAP 2, SAP 4 | Medium | Results may depend on untested assumptions | Add sensitivity/tipping-point analysis |
```

Replace example content with recurring issues found across SAP evaluations.

### Reviewer question bank.md

Create and maintain:

```markdown
| ID | Topic | Reviewer question | Trigger | Suggested evidence needed |
| --- | --- | --- | --- | --- |
| RQ-001 | Estimand | What treatment effect is the primary analysis estimating? | Endpoint defined but estimand absent | Protocol objective, endpoint, analysis population, intercurrent-event handling |
| RQ-002 | Performance goal | Why is the performance goal clinically and historically justified? | Single-arm design | Literature, registry, prior studies, comparability rationale |
| RQ-003 | Missing data | How robust is the primary result to informative missingness? | No sensitivity analysis | Missingness summary, sensitivity analysis, tipping-point analysis |
| RQ-004 | Safety | What adverse-event rate could this sample size reasonably detect? | Small sample size | Precision calculation, confidence intervals |
```

Replace example content with questions triggered by actual SAP weaknesses.

### Estimand reconstruction table.md

Create and maintain:

```markdown
# Estimand reconstruction table

| SAP | Population | Treatment/device condition | Endpoint | Intercurrent events | Summary measure | Status |
| --- | --- | --- | --- | --- | --- | --- |
| SAP 1 | Enrolled and treated subjects | Use of device according to IFU | Primary performance endpoint | Discontinuation not clearly addressed | Mean change | Partial |
| SAP 2 | Randomized subjects | Device vs control | Binary success at 30 days | Reintervention unclear | Risk difference | Weak |
| SAP 3 | Per-protocol subjects | Device exposure completed | Continuous outcome | Missing visits imputed | Mean difference | Moderate |
```

Replace example content with reconstructed estimands from SAP evaluations.

### Design patterns.md

Create and maintain:

```markdown
# SAP design-pattern taxonomy

| Design pattern | Typical statistical risks | Required SAP elements |
| --- | --- | --- |
| Single-arm performance goal | External validity, performance-goal justification, selection bias | Performance goal rationale, confidence interval method, sensitivity to threshold |
| Randomized parallel-group | Randomization, treatment effect, missing data, multiplicity | Primary model, covariates, analysis sets, multiplicity |
| Crossover | Period effects, carryover, within-subject correlation | Mixed model, sequence/period terms, carryover assessment |
| Diagnostic accuracy | Reference standard, indeterminate results, paired data | Sensitivity/specificity, CI method, reader effects, missing/invalid tests |
| Post-market observational | Confounding, data completeness, generalizability | Descriptive plan, bias assessment, missingness, subgroup interpretation |
```

Ground the taxonomy in trusted-source evidence where available.

### Lessons learned.md

Create and maintain:

```markdown
# Lessons learned from medical-device SAPs

## Strong practices observed

## Recurring weaknesses

## Implications for future SAP authoring
```

Populate with cross-SAP lessons grounded in generated reviews.

## Strong and Weak Patterns

Create `wiki/Strong and weak patterns/`.

For each of the 20 questions, create one markdown file named with the BIOSTAT code and topic. Each file describes strong and weak patterns for that question. Ground the text in trusted sources from the `biostat` collection and quote complete relevant paragraphs as described in the GNO retrieval rules, with source identifier, exact location if available, and semantic confidence `Low`, `Medium`, or `High`. Do not include `gno://...` URIs or raw GNO commands.

Each pattern page should include:

```markdown
# BIOSTAT-000 Topic strong and weak patterns

## Trusted-source anchor

> Quote the highest-match complete paragraph and the second-highest-match complete paragraph from a trusted source. If only 1 relevant paragraph is available, quote that complete paragraph.

Source: ...
Semantic confidence: Low | Medium | High

## Strong patterns

## Weak patterns observed

## Recommended fixes
```

## Audit Workflow

Use this workflow when asked to audit, review, lint, or check the generated wiki against this skill.

1. Read this `SKILL.md`, `questions.yml`, and the current `wiki/` folder before writing.
2. Do not modify `wiki/Fair use.md` after creation.
3. Do not touch `wiki/skill-example.md`; it is fully human-maintained.
4. Check BIOSTAT-001 to BIOSTAT-020 pages for:
   - question reference links to the matching `Questions.md` heading
   - required evidence blocks
   - source identifiers without internal GNO URIs or raw commands
   - semantic confidence as `Low`, `Medium`, or `High`, not numeric rerank confidence
   - no separate `Gap`, `Challenging the gap`, or `Alternative interpretation` subsections or fields
   - `## Attribute assessment` with a table containing `Question attribute`, `Evidence found`, and `Gap quality`
   - `### Gap statement` with a page-specific paragraph that distinguishes explicit, recoverable, ambiguous, and missing information
5. Check vault-level pages for:
   - removal of `Method index.md` if it exists
   - existence and completeness of `Question attributes.md` for BIOSTAT-001 through BIOSTAT-020
   - each question section in `Questions.md` links to the matching `Question attributes.md` heading
   - trusted-source sections rather than a trusted-source table
   - exact original source titles and exact source authors where available
   - trusted-source reference counts based on mentions elsewhere in `wiki/`
   - no internal retrieval URIs in published text
6. Create or update `wiki/Site review.md`.

`Site review.md` must include:

```markdown
# Site review

## Summary

## Content not matching the skill definition

## Gaps and missing evidence

## Weak claims

## Inconsistencies

## Contradictions

## Recommended fixes
```

Findings should cite the page path and heading or line number when practical. Do not silently fix human-maintained pages.

## Iteration Stopping Condition

Iterate within the generated `wiki/` outputs until:

1. Every question in `questions.yml` has a corresponding note for every SAP.
2. Every note contains the required question, SAP evidence, `Statistical Claim-to-Evidence`, and same-question cross-links.
3. Every material claim has at least one evidence claim block.
4. Every evidence claim block has source document, exact location if available, complete relevant quoted paragraphs as described in the GNO retrieval rules, semantic confidence `Low`, `Medium`, or `High`, and assessment status.
5. Every BIOSTAT-001 to BIOSTAT-020 note has `## Attribute assessment`, a three-column attribute table, and a page-specific `### Gap statement`; no note has separate `Gap`, `Challenging the gap`, or `Alternative interpretation` fields.
6. Unsupported claims are removed or represented in the attribute assessment and gap statement.
7. Vault-level pages exist and are updated, including `Trusted sources.md` and `Question attributes.md`, except `Fair use.md`, which is created only if missing and then left unchanged, and `skill-example.md`, which is not touched.
8. Strong and weak pattern pages exist for BIOSTAT-001 through BIOSTAT-020.
9. Two consecutive passes find no new high- or medium-priority gaps.

Stop after the condition is met. Do not continue polishing language.
