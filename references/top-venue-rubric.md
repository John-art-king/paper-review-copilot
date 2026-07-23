# Top-Venue Contribution Rubric

Use this rubric to evaluate a paper as a demanding group-meeting audience or reviewer would. Do not collapse every dimension into one score. A paper can be important but weakly evidenced, technically novel but narrowly useful, or empirically strong but incremental.

## Evidence Hierarchy

Prefer evidence in this order:

1. Main paper methods, equations, tables, figures, and explicit limitations.
2. Supplementary material, appendices, released code, configs, and artifacts.
3. Closest prior papers and their official artifacts.
4. Author project pages, talks, and issue discussions.
5. Surveys and secondary explanations.

Use lower tiers for orientation, not as sole support for a strong verdict.

## Contribution Ledger

Create one row per claimed contribution.

| Field | Required content |
|---|---|
| Claim | What the authors say is contributed |
| Closest predecessor | Most similar mechanism, not merely same task |
| Exact delta | Added, removed, generalized, constrained, or measured differently |
| Causal rationale | Why the delta should change the outcome |
| Decisive evidence | Exact experiment, theorem, ablation, or artifact with locator |
| Alternative explanation | Scale, data, compute, tuning, implementation, or evaluation bias |
| Missing test | Smallest test that would reduce uncertainty |
| Verdict | Calibrated conclusion and confidence |

## Assess Separate Dimensions

Use a 0-3 score only when comparing papers or structuring discussion.

### Research Importance

- **0**: marginal or poorly motivated problem.
- **1**: useful narrow problem with limited consequence.
- **2**: meaningful unresolved limitation in an active field.
- **3**: changes an important capability, scientific understanding, or practical frontier.

### Mechanism-Level Novelty

- **0**: already present in close prior work or only renamed.
- **1**: routine variant, composition, or transfer.
- **2**: meaningful new mechanism, formulation, or operating regime.
- **3**: enables a capability or explanation unavailable to the closest predecessor.

### Technical Substance

- **0**: no identifiable technical delta.
- **1**: primarily tuning, scale, or straightforward engineering.
- **2**: non-obvious design with coherent rationale.
- **3**: deep method, theory, or system insight with broad implications.

### Evidence And Rigor

- **0**: key claim is untested.
- **1**: headline metric improves but mechanism remains unisolated.
- **2**: matched comparisons and relevant ablations support the claim.
- **3**: converging experiments, theory, or robust controls rule out major alternatives.

### Reproducibility And Generality

- **0**: critical details or artifacts missing; one fragile setting.
- **1**: partially specified or narrowly evaluated.
- **2**: adequate artifacts and several relevant settings.
- **3**: transparent protocols, strong artifacts, and broad robustness evidence.

## Red Flags

Actively inspect for outdated baselines, unequal compute or data budgets, novelty defined by terminology, missing key ablations, selective datasets, unstable gains, hidden proprietary dependencies, and "first" claims unsupported by a systematic search.

## Calibrated Verdicts

Use one and explain why:

- **Substantive contribution with strong evidence**
- **Substantive contribution with incomplete evidence**
- **Credible incremental contribution**
- **Empirical or benchmark contribution**
- **Engineering integration with practical value**
- **Weakly differentiated or unsupported claim**
- **Cannot judge from available evidence**
