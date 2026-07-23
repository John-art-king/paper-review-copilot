---
name: group-meeting-paper-review
description: Analyze one or more academic papers for lab or group-meeting reporting. Use when the user provides a paper, PDF, DOI, title, arXiv link, or repository and asks for paper reading, literature review, related-work comparison, contribution or novelty analysis, research gaps, reproducibility assessment, anticipated questions, speaker notes, or a presentation outline.
---

# Group Meeting Paper Review

Produce an evidence-grounded technical review, not a polished paraphrase of the abstract. Separate what the paper states, what its evidence establishes, what is inferred, and what remains unknown.

## Choose the Mode

Infer the lightest mode that satisfies the request:

- **Quick brief**: one paper, central question, method, results, novelty, and limitations.
- **Deep review**: reconstruct the argument, inspect method and experiments, audit novelty, and propose follow-up work. Use this by default for group meetings.
- **Comparison review**: compare multiple papers using a common taxonomy and evidence matrix.
- **Presentation delivery**: produce a timed slide narrative, speaker notes, and anticipated questions after completing the analysis.

When details are missing, default to the user's language, a technical graduate audience, a 12-15 minute talk, and 10-12 content slides. State these defaults briefly instead of blocking progress.

## Route Supporting Work

- Use the PDF capability to extract and inspect supplied PDFs, including figures, tables, appendices, and page locations.
- Browse primary sources when the user asks about current related work, novelty, priority, or the state of the art. Prefer the publisher page, arXiv, proceedings, author repository, official code, and supplementary material.
- Use the presentation capability only after the analytical content is stable when the user requests an actual slide deck.
- Never treat a search snippet, abstract-only view, secondary blog, or generated summary as equivalent to the full paper.

## Maintain an Evidence Ledger

For every material claim, preserve:

1. the claim;
2. its source type;
3. a locator such as section, page, figure, table, equation, appendix, or repository file;
4. its status: author claim, observed evidence, reviewer inference, proposed idea, or unverified;
5. confidence: high, medium, or low.

Use compact inline labels when ambiguity matters: `[Author claim]`, `[Evidence]`, `[Inference]`, `[Proposal]`, and `[Unverified]`. Do not invent page numbers, quotations, baselines, datasets, or numerical results.

## Execute the Review

### 1. Frame the Paper

Identify the task, target user or system, input and output, operating constraints, and the exact failure in prior approaches. Reduce the paper to one falsifiable research question.

### 2. Reconstruct the Argument

Explain the chain:

`problem -> prior limitation -> key insight -> mechanism -> expected effect -> evidence -> conclusion`

Define essential terms and notation. Reconstruct the method as a pipeline with inputs, transformations, learned or fixed components, losses or objectives, and outputs. Explain why each major component should affect the claimed outcome.

### 3. Audit the Experiments

Inspect datasets, splits, baselines, metrics, implementation parity, hardware, hyperparameters, ablations, statistical variation, and failure cases. Check whether the experiments test the stated mechanism or only show an end metric improvement.

Ask counterfactual questions:

- Does the gain survive a matched compute, parameter, data, and tuning budget?
- Does an ablation isolate the proposed mechanism?
- Are the strongest and closest baselines present?
- Is the improvement practically meaningful, statistically stable, and consistent across regimes?
- Do evaluation conditions match the claimed deployment setting?

### 4. Audit Every Contribution

Always read [novelty-rubric.md](references/novelty-rubric.md) when assessing contributions, novelty, research gaps, or future work.

For each claimed contribution, identify:

- the closest prior approach;
- the exact technical or empirical delta;
- why that delta is non-trivial;
- evidence that the delta causes or enables the result;
- scientific or practical significance;
- missing evidence and plausible alternative explanations;
- a calibrated verdict.

Do not call renaming, routine module combination, scale increase, dataset substitution, unsupported optimization, or a new application alone a methodological innovation.

### 5. Derive Research Opportunities

Generate ideas from demonstrated limitations, untested assumptions, contradictory evidence, missing regimes, or deployment constraints. For each idea, provide:

- observed gap and source locator;
- testable hypothesis;
- proposed intervention;
- minimum decisive experiment;
- required baselines and metrics;
- expected result and falsification condition;
- feasibility, risk, and likely contribution type.

Rank ideas by evidence strength, research value, and feasibility. Prefer two or three defensible ideas over a long generic list. Distinguish a paper's contribution from the user's possible new contribution.

Label each idea as a direct extension, replication or benchmark, or cross-domain transfer. Do not present an adjacent user goal as a limitation of the paper unless the paper actually claims that scope.

### 6. Build the Group-Meeting Narrative

Read [report-formats.md](references/report-formats.md) when producing reading notes, a comparison, a talk outline, slide content, speaker notes, or anticipated questions.

Lead with the research tension and the paper's answer. Give method and evidence most of the time. End with a clear verdict, limitations, and the most promising follow-up question.

For papers on edge AI, model conversion, graph compilers, inference runtimes, quantization, hardware acceleration, or deployment, also read [edge-deployment-checklist.md](references/edge-deployment-checklist.md).

## Handle Incomplete Evidence

- If only an abstract is available, produce an abstract-level triage and say what cannot be judged.
- If the paper is inaccessible, use available primary metadata and ask for the PDF only when deeper claims depend on it.
- If related-work search is unavailable, avoid definitive claims such as "first" or "state of the art."
- If sources conflict, show the conflict and explain which interpretation has stronger evidence.
- If the paper does not support its claimed novelty, say so directly and precisely.

## Verify Before Delivery

Confirm that:

- every number and key factual claim has a source locator;
- every closest-prior-work comparison has a primary source or an explicit paper locator;
- author claims are separated from reviewer judgments;
- the method explanation includes a causal rationale, not only component names;
- the novelty verdict names the comparison target;
- experimental weaknesses are tied to the conclusions they weaken;
- research ideas include a falsifiable experiment;
- slide titles express claims and the timing fits the requested duration;
- strict length limits remove background detail before evidence locators or uncertainty labels;
- unresolved uncertainty is visible rather than silently filled in.
