# Report Formats

Select only the format needed for the request. Keep evidence locators in notes even when the visible output is concise.

Under a strict length limit, preserve the bottom line, closest-work delta, decisive evidence, one consequential limitation, and the requested research ideas. Remove general background and secondary details before removing source locators, uncertainty labels, or falsification conditions.

## Deep-Review Output

Use this order:

1. **Bottom line**: one sentence on what the paper changes and one sentence on how convincing it is.
2. **Paper card**: title, authors, venue or status, year, links, code and data availability.
3. **Research question**: task, setting, constraints, and falsifiable question.
4. **Prior-work gap**: closest approaches and the precise unresolved limitation.
5. **Core insight**: the one idea the method depends on.
6. **Method pipeline**: inputs, stages, objectives, outputs, and causal rationale.
7. **Experimental evidence**: datasets, baselines, metrics, main results, ablations, and failure cases.
8. **Contribution ledger**: claim-by-claim novelty audit and confidence.
9. **Limitations**: technical, experimental, deployment, and reproducibility limits.
10. **Research opportunities**: two or three ranked, falsifiable idea cards.
11. **Questions for discussion**: questions that expose assumptions or affect the verdict.

## Comparison Review

Define a common taxonomy before comparing papers. Use a matrix such as:

| Paper | Problem and setting | Core mechanism | Key assumption | Evidence | Cost | Strength | Limitation | Novelty verdict |
|---|---|---|---|---|---|---|---|---|

Normalize claims before comparison. Do not compare a quality metric from one dataset with a latency result from another as if they share an evaluation protocol. Highlight cells that are not directly comparable.

End with:

- what is now established across papers;
- where results conflict;
- what remains untested;
- which paper offers the strongest evidence for each subproblem;
- the smallest experiment that would resolve the most important disagreement.

## Default 12-15 Minute Slide Narrative

Use 10-12 content slides. Allocate time approximately as follows:

| Slide purpose | Count | Time |
|---|---:|---:|
| Research tension and question | 1-2 | 1.5 min |
| Prior work and exact gap | 1 | 1.0 min |
| Core insight | 1 | 1.0 min |
| Method and mechanism | 2-3 | 3.5 min |
| Experimental design and results | 2-3 | 3.5 min |
| Novelty audit and critique | 1-2 | 2.0 min |
| Research opportunity and takeaway | 1-2 | 1.5 min |

Give every slide:

- a claim-style title;
- one primary visual or comparison;
- no more supporting detail than the speaker can explain in its time budget;
- a one-sentence speaker takeaway;
- source locators in speaker notes.

Prefer original figures or faithfully redrawn diagrams when permitted and useful. Explain axes, units, legends, and experimental conditions. Never show a result chart without stating the comparison and takeaway.

## Slide Content Template

For each slide, provide:

```text
Slide N - [claim-style title]
Purpose:
Visual:
On-slide content:
Speaker notes:
Evidence locators:
Transition:
```

## Anticipated Questions

Prepare concise answers in these categories:

- Why is the problem important?
- What is genuinely new relative to the closest work?
- Why should the mechanism work?
- Are comparisons fair?
- Which ablation is decisive?
- What fails, and under what conditions?
- Does the method generalize?
- What is the compute, memory, latency, energy, or data cost?
- Can the result be reproduced?
- What would be the next experiment?

For each answer, mark whether it is supported, inferred, or unknown. Do not bluff an answer that the paper does not provide.

## Presentation Quality Gate

Before delivery, verify:

- the audience can state the problem by slide 2;
- the closest prior work appears before the novelty claim;
- the method diagram explains data flow and mechanism;
- results include conditions and not only headline numbers;
- critique distinguishes fatal flaws from ordinary limitations;
- proposed ideas follow from evidence rather than fashion;
- the final slide contains a verdict, not a generic thank-you page;
- the narrative fits the allotted time without rushing.
