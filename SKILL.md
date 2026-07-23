---
name: group-meeting-paper-review
description: Turn top-tier conference and journal papers into evidence-grounded group-meeting narratives. Use for paper reading, novelty audits, reviewer-style critique, related-work comparison, speaker notes, anticipated questions, and testable follow-up ideas.
---

# Top-Tier Group Meeting Paper Review

Turn a paper from a top conference or journal into a defensible group-meeting narrative. Do not produce a polished abstract paraphrase. Separate author claims, direct evidence, reviewer inference, and unresolved uncertainty.

## Default Delivery

For a supplied paper, PDF, DOI, title, or repository, infer the lightest adequate mode:

- **Paper triage**: research question, central mechanism, evidence quality, and one reason to read or skip.
- **Deep review**: reconstruct the argument, audit the top-tier contribution, inspect experiments, and identify limitations.
- **Comparison review**: compare papers through a shared mechanism-level taxonomy.
- **Presentation delivery**: a timed 12-15 minute narrative with 10-12 content slides, speaker notes, and anticipated questions.

Unless the user specifies otherwise, use the user's language, a technical graduate audience, a 12-15 minute slot, and 10-12 content slides.

## Evidence Discipline

Maintain an evidence ledger for every material conclusion:

1. claim;
2. source and locator: section, page, figure, table, equation, appendix, or artifact;
3. status: `[Author claim]`, `[Evidence]`, `[Inference]`, `[Proposal]`, or `[Unverified]`;
4. confidence: high, medium, or low.

Never invent page numbers, quotes, baselines, datasets, or results. Abstract-only access supports triage, not a definitive novelty or rigor verdict.

## Workflow

### 1. Frame The Research Tension

State the task, regime, constraints, and failure of the closest prior approach. Reduce the paper to one falsifiable research question and state why that question matters to the field.

### 2. Reconstruct The Causal Argument

Explain:

`research tension -> prior gap -> core insight -> mechanism -> expected effect -> evidence -> calibrated conclusion`

Define essential notation. Rebuild the method as inputs, transformations, objectives, outputs, and causal rationale. A component list is not a method explanation.

### 3. Audit Top-Tier Contribution

Always read [top-venue-rubric.md](references/top-venue-rubric.md) for novelty, rigor, contribution, or acceptance-style discussion.

For every claimed contribution, name the closest mechanism-level predecessor, the exact delta, why it could matter, the evidence that isolates it, alternative explanations, and the smallest missing test. Do not equate scale, renaming, a routine combination, or a new application with methodological novelty.

### 4. Inspect Experimental Validity

Check dataset and split choice, baseline strength, compute and tuning parity, ablations, uncertainty, failure cases, reproducibility artifacts, and the match between claims and measured evidence.

Ask whether the gain survives matched budgets, whether the ablation isolates the mechanism, whether the result generalizes outside the favorable setting, and whether omitted evidence could reverse the conclusion.

### 5. Compare Related Work When Needed

Read [related-work-comparison.md](references/related-work-comparison.md) for multiple papers, priority claims, or state-of-the-art discussion. Browse primary sources: official proceedings, publisher pages, arXiv, supplements, code, and project pages.

Do not compare metrics from incompatible data, protocol, compute budget, or operating regime as though they were directly comparable.

### 6. Produce Testable Follow-Up Ideas

Read [research-idea-cards.md](references/research-idea-cards.md) for future work. Keep two or three ideas that arise from documented limitations, missing regimes, contradictory evidence, or untested assumptions. Every idea needs a falsifiable hypothesis and a decisive experiment.

### 7. Build The Group-Meeting Narrative

Read [group-meeting-deck.md](references/group-meeting-deck.md) for reading notes, presentation outlines, slides, speaker notes, or anticipated questions.

Lead with the field-level tension, establish the closest prior work before claiming novelty, spend most time on mechanism and evidence, then end with a clear verdict, limitations, and next research question.

## Quality Gate

Before delivery, verify that:

- every key number and factual claim has a locator;
- the closest prior-work comparison names a primary source or is labeled unverified;
- author claims and reviewer judgments are visibly separate;
- the novelty verdict has a comparison target and calibrated confidence;
- experimental weaknesses are connected to the conclusion they weaken;
- each research idea has a falsification condition;
- slide titles state claims, not topics;
- the narrative fits the allocated time and leaves the audience with a verdict rather than a generic summary.
