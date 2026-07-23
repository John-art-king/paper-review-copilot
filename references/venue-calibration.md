# Venue And Field Calibration

Use this guide when the paper type or research community changes the meaning of novelty, rigor, and decisive evidence. Do not use one universal acceptance formula.

## Identify The Evaluation Regime

Record:

- discipline and subfield;
- conference, journal, workshop, or preprint status;
- method, theory, systems, dataset, benchmark, replication, or application contribution;
- maturity of the field and strength of available baselines;
- official venue criteria when an acceptance-style judgment is explicitly requested.

Treat venue criteria as time-sensitive. Verify current criteria from the official venue or publisher source before citing them.

## Calibrate Decisive Evidence

| Research regime | Evidence that usually matters most | Frequent failure mode |
|---|---|---|
| Empirical machine learning | Matched baselines, robust ablations, multiple datasets, uncertainty, leakage controls | Gains explained by scale, data, or tuning |
| Systems | End-to-end implementation, realistic workloads, strong competing systems, resource and sensitivity analysis | Microbenchmark gains that disappear end to end |
| Theory | Clear assumptions, correct proof, relation to known results, non-vacuous implications | Strong theorem under unrealistic or hidden assumptions |
| Scientific or domain application | Domain-valid protocol, external validity, meaningful endpoints, expert-grounded interpretation | Benchmark improvement without scientific or practical validity |
| Dataset or benchmark | Construct validity, contamination controls, annotation quality, coverage, stable evaluation | Leaderboard movement without measuring the intended capability |
| Replication or negative result | Faithful protocol, sufficient power, transparent deviations, diagnostic analysis | Null result caused by mismatched implementation or budget |

## Calibrate The Verdict

Judge the paper against its claimed contribution type and community standard. A systems paper need not contain a theorem; a theory paper need not win a benchmark; a dataset paper can be substantive without a new model. Still require the evidence to support the paper's own causal and scope claims.

Never infer acceptance probability from rubric scores. Phrase the result as a contribution and evidence verdict, then state which venue-specific question remains unresolved.
