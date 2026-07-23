# Paper Review Copilot

> Turn dense research papers into evidence-backed group meeting discussions.

Paper Review Copilot is a reusable Codex skill for researchers, students, and engineering teams who need more than a paper summary. It reconstructs the paper's argument, audits novelty and experiments, tracks evidence locators, and turns the result into a focused discussion or presentation plan.

Built for Chinese and international lab meetings: move from "summarize this paper" to evidence-grounded review, novelty auditing, reproducibility checks, and presentation preparation.

## Why It Is Useful

Most paper notes answer what the authors wrote. This skill also asks whether the claims are supported, what the closest prior work actually adds, which comparisons are fair, and what experiment would falsify the next research idea.

## Core Capabilities

- **Quick brief**: a compact, source-located briefing for fast triage.
- **Deep review**: research question, prior-work gap, mechanism, method pipeline, experiments, limitations, and discussion questions.
- **Novelty audit**: contribution ledger with closest prior work, exact delta, mechanism, evidence, alternative explanations, and calibrated verdicts.
- **Evidence ledger**: separates author claims, direct evidence, inference, and unknowns instead of hiding uncertainty.
- **Experiment audit**: checks baselines, ablations, data splits, metrics, compute, reproducibility, and failure cases.
- **Comparison review**: normalizes multiple papers before comparing their mechanisms, assumptions, evidence, and cost.
- **Presentation planning**: produces a 10-12 slide narrative with claim-style titles, visuals, speaker notes, transitions, and anticipated questions.
- **Edge deployment review**: evaluates model formats, conversion correctness, runtime contracts, quantization, latency, memory, power, and hardware evidence.

## What Makes It Different

The output is designed to be useful in a lab meeting and defensible in a research discussion:

1. Every material number or claim should have a locator.
2. Novelty is compared at the mechanism level, not only by title keywords.
3. Serialization success, numerical correctness, runtime execution, and hardware acceleration are treated as different outcomes.
4. Research ideas include a hypothesis, intervention, decisive experiment, metrics, positive result, and falsification condition.

## Included References

- [`SKILL.md`](SKILL.md): the complete workflow and operating instructions.
- [`references/novelty-rubric.md`](references/novelty-rubric.md): contribution ledger, evidence hierarchy, novelty dimensions, and idea cards.
- [`references/report-formats.md`](references/report-formats.md): deep-review, comparison, and presentation formats.
- [`references/edge-deployment-checklist.md`](references/edge-deployment-checklist.md): conversion and edge-device evaluation checklist.
- [`agents/openai.yaml`](agents/openai.yaml): agent metadata for skill discovery.

## Install As A Codex Skill

Copy this repository into your local skills directory using the folder name `group-meeting-paper-review`:

```text
$CODEX_HOME/skills/group-meeting-paper-review/
```

Then ask Codex to review a supplied paper, compare papers, prepare a group meeting brief, or audit an edge-deployment paper. The skill supports quick briefs, deep reviews, comparison reviews, and presentation-oriented outputs.

## Recommended Review Discipline

Provide the paper PDF or an official paper link when possible. For strong novelty conclusions, include the closest prior work and official artifacts. When evidence is incomplete, the skill is expected to say so explicitly rather than inventing a result.

## Scope

This repository contains the review workflow and reference checklists. It does not bundle papers, datasets, model weights, or proprietary research artifacts.

## License

Released under the MIT License. See [`LICENSE`](LICENSE).
