---
name: group-meeting-paper-review
description: Turn conference and journal papers, PDFs, DOI/arXiv links, supplements, and code repositories into evidence-grounded research group-meeting packages. Use for paper triage, deep reading, novelty and rigor audits, mechanism-level related-work comparison, bilingual slide outlines, timed speaker notes, advisor-style Q&A rehearsal, and falsifiable follow-up research ideas.
---

# Research Group Meeting Paper Review

Turn a research paper into a defensible group-meeting argument. Do not produce a polished abstract paraphrase. Separate what the authors claim, what the artifacts establish, what the reviewer infers, and what remains unknown.

## Configure The Review

Infer missing settings without blocking progress. State the chosen profile in one compact line.

| Setting | Options | Default |
|---|---|---|
| Language | Chinese, English, or bilingual | User's language |
| Audience | Mixed lab, field specialists, or newcomers | Technical graduate audience |
| Duration | 5, 10, 15, 20, or 30 minutes | 15 minutes |
| Depth | Triage, deep review, comparison, meeting pack, or rehearsal | Lightest mode that satisfies the request |
| Stance | Explanatory, reviewer-critical, or research-opportunity | Reviewer-critical |

For bilingual delivery, keep slide titles and key terms bilingual but write speaker notes in the user's primary language. Preserve canonical English method, dataset, and metric names.

## Default Delivery

For a supplied paper, PDF, DOI, title, supplement, or repository, select one mode:

- **Paper triage**: research question, central mechanism, evidence quality, and one reason to read or skip.
- **Deep review**: reconstruct the argument, audit the top-tier contribution, inspect experiments, and identify limitations.
- **Comparison review**: compare papers through a shared mechanism-level taxonomy.
- **Meeting pack**: executive verdict, evidence ledger, timed deck, speaker notes, discussion prompts, and follow-up ideas.
- **Rehearsal**: advisor-style questions, concise defended answers, confidence labels, and evidence that would change the answer.

If the user asks to prepare a presentation, slides, or a group-meeting report, deliver a meeting pack rather than a summary.

## Establish Source Completeness

Inventory available sources before judging the work: main paper, appendix or supplement, official code and configs, project page, and closest prior work. Use primary sources for novelty and priority claims.

Distinguish three access levels:

- **Full evidence**: main paper plus relevant supplementary or official artifacts. Support a deep verdict.
- **Paper only**: support method and experiment review, but qualify reproducibility claims.
- **Abstract or metadata only**: support triage only. Do not issue a definitive novelty or rigor verdict.

## Evidence Discipline

Maintain an evidence ledger for every material conclusion:

1. claim;
2. source and locator: section, page, figure, table, equation, appendix, or artifact;
3. status: `[Author claim]`, `[Evidence]`, `[Inference]`, `[Proposal]`, or `[Unverified]`;
4. confidence: high, medium, or low.

Never invent page numbers, quotes, baselines, datasets, or results. Prefer an explicit unknown over a plausible completion. Do not turn rubric scores into an acceptance probability.

## Workflow

### 1. Frame The Research Tension

State the task, regime, constraints, and failure of the closest prior approach. Reduce the paper to one falsifiable research question and state why that question matters to the field.

### 2. Reconstruct The Causal Argument

Explain:

`research tension -> prior gap -> core insight -> mechanism -> expected effect -> evidence -> calibrated conclusion`

Define essential notation. Rebuild the method as inputs, transformations, objectives, outputs, and causal rationale. A component list is not a method explanation.

### 3. Audit The Contribution

Always read [top-venue-rubric.md](references/top-venue-rubric.md) for novelty, rigor, contribution, or acceptance-style discussion. Also read [venue-calibration.md](references/venue-calibration.md) when the venue, discipline, or paper type changes what counts as decisive evidence.

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

### 8. Assemble The Delivery

Always read [deliverable-contract.md](references/deliverable-contract.md) for a meeting pack or deep review. Fill only sections supported by the requested mode and available evidence. Use the templates in `assets/` when the user requests reusable Markdown artifacts.

For rehearsal, skeptical advisor questions, or discussion preparation, read [qa-rehearsal.md](references/qa-rehearsal.md). Answer from the evidence ledger, not from rhetorical confidence.

## Quality Gate

Before delivery, verify that:

- every key number and factual claim has a locator;
- the closest prior-work comparison names a primary source or is labeled unverified;
- author claims and reviewer judgments are visibly separate;
- the novelty verdict has a comparison target and calibrated confidence;
- experimental weaknesses are connected to the conclusion they weaken;
- each research idea has a falsification condition;
- slide titles state claims, not topics;
- the narrative fits the allocated time and leaves the audience with a verdict rather than a generic summary;
- every anticipated answer is marked supported, inferred, or unresolved;
- the final package distinguishes a paper limitation from a presentation omission.
