# Novelty and Evidence Rubric

Use this rubric to test contribution claims and derive defensible research opportunities. Do not collapse the dimensions into one total score; a single total hides whether a claim is new but unsupported, or useful but incremental.

## Evidence Hierarchy

Prefer evidence in this order:

1. Main paper methods, equations, tables, figures, and explicit limitations.
2. Supplementary material, appendices, released code, configs, and artifacts.
3. Closest prior papers and their official artifacts.
4. Author talks, project pages, and issue discussions.
5. Surveys, reviews, and secondary explanations.

Use lower tiers for orientation, not as the sole basis for a strong novelty verdict.

## Contribution Ledger

Create one row per claimed contribution:

| Field | Required content |
|---|---|
| Claim | What the authors say is contributed |
| Type | Problem/formulation, method, system, theory, empirical finding, dataset/benchmark, or application |
| Closest prior work | The most similar mechanism, not merely a paper on the same topic |
| Exact delta | What is added, removed, generalized, constrained, or measured differently |
| Mechanism | Why the delta should change the result |
| Supporting evidence | Exact experiment, theorem, ablation, or artifact and locator |
| Alternative explanation | Scale, tuning, data, compute, implementation quality, or evaluation bias |
| Missing test | The smallest test needed to reduce uncertainty |
| Verdict | Calibrated conclusion and confidence |

## Score Separate Dimensions

Assign 0-3 on each dimension only when useful for comparison.

### Prior-Art Difference

- **0**: Already present in close prior work or only renamed.
- **1**: Small variant, routine composition, or narrow transfer.
- **2**: Meaningful new mechanism, formulation, or operating regime.
- **3**: Enables a capability or understanding unavailable in the closest prior work.

### Technical Substance

- **0**: No identifiable technical delta.
- **1**: Mostly tuning, scaling, or straightforward engineering.
- **2**: Non-obvious design with a coherent mechanism.
- **3**: Deep mechanism, theory, or system architecture with broad implications.

### Causal Evidence

- **0**: Claim is not tested.
- **1**: End metric improves, but the mechanism is not isolated.
- **2**: Relevant ablations or controlled comparisons support the claim.
- **3**: Multiple controlled tests, theory, or converging evidence rule out major alternatives.

### Significance

- **0**: No meaningful effect or consequence shown.
- **1**: Small benefit in a narrow setting.
- **2**: Useful improvement or insight across relevant settings.
- **3**: Changes feasible practice, capability, cost frontier, or scientific understanding.

### Generality and Reproducibility

- **0**: Critical details or artifacts are missing; one fragile setting only.
- **1**: Partially specified or narrowly evaluated.
- **2**: Reproducible in several relevant settings with adequate details.
- **3**: Strong artifacts, transparent protocols, and broad robustness evidence.

## Calibrated Verdicts

Use one of these verdict forms and explain why:

- **Substantive contribution, strong evidence**
- **Substantive contribution, incomplete evidence**
- **Credible incremental contribution**
- **Engineering integration with practical value**
- **Empirical or benchmark contribution**
- **Weakly differentiated or unsupported claim**
- **Cannot judge from available evidence**

Avoid "no innovation" when the accurate conclusion is narrower, such as a useful system integration without methodological novelty.

## Red Flags

Actively check for:

- comparison against outdated or weak baselines;
- unequal compute, data, parameter, tuning, or preprocessing budgets;
- novelty defined by terminology rather than mechanism;
- no ablation for the claimed key component;
- improvements within noise or on one favorable metric;
- selective datasets, hardware, or operating points;
- hidden dependence on proprietary data or tooling;
- deployment claims based only on simulator or desktop measurements;
- accuracy reported without latency, memory, energy, or compatibility tradeoffs;
- "first" claims unsupported by a systematic prior-art search.

## Find the Closest Prior Work

Search by mechanism and problem structure, not only the paper title's keywords. Locate:

1. the earliest clear precursor;
2. the closest mechanism-level predecessor;
3. a contemporary competing approach;
4. a newer challenger when judging current relevance.

Compare assumptions, objective, mechanism, data, compute, evaluation protocol, and operating regime. Record publication dates and distinguish preprint date from venue date when priority matters.

Support each prior-work comparison with that work's primary source. If the comparison comes only from the reviewed paper's related-work section, label it as the reviewed authors' characterization rather than an independently verified fact.

## Derive New Research Ideas

Use at least one of these evidence-backed sources:

- an assumption that fails outside the paper's setting;
- an unexplained ablation or contradictory result;
- an unsupported causal claim;
- a missing data, hardware, scale, robustness, or distribution regime;
- a metric that misses an important cost or failure mode;
- a deployment mismatch between evaluation and intended use;
- an interaction between two papers that neither tests.

Reject ideas that only say "use a larger model," "add attention," "try more datasets," or "combine A and B" without a mechanism and falsification test.

## Idea Card

For every retained idea, fill in:

| Field | Content |
|---|---|
| Evidence-backed gap | What is missing and where the evidence appears |
| Hypothesis | A statement that can be false |
| Intervention | The smallest method or system change that tests it |
| Decisive experiment | Dataset/workload, baseline, control, and protocol |
| Metrics | Quality plus relevant cost and robustness measures |
| Positive result | What outcome supports the hypothesis |
| Falsification | What outcome rejects it |
| Contribution if successful | Method, system, theory, empirical, or benchmark |
| Feasibility and risk | Data, compute, implementation, and evaluation constraints |
