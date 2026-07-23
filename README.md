# Paper Review Copilot

> Turn top-tier papers into defensible group-meeting narratives and testable next ideas.

Paper Review Copilot is a Codex skill for researchers who present and discuss papers from leading conferences and journals. It turns a PDF into a reviewer-grade argument: what question matters, what is genuinely new, what the experiments establish, where the evidence stops, and what a lab should test next.

Built for Chinese and international group meetings. The goal is not "summarize this paper". The goal is a clear, evidence-located narrative that survives questions from an advisor or a critical audience.

## What It Delivers

- **Fast triage**: decide whether a paper merits deep reading.
- **Deep review**: reconstruct the research tension, causal mechanism, evidence, limitations, and bottom-line verdict.
- **Top-tier contribution audit**: test problem importance, mechanism-level novelty, technical depth, evidence strength, reproducibility, and field impact.
- **Reviewer-style experiment critique**: inspect baseline fairness, ablations, uncertainty, failure cases, and claims that exceed their evidence.
- **Related-work comparison**: compare papers through mechanisms, assumptions, regimes, and evidence rather than disconnected headline metrics.
- **Group-meeting deck plan**: produce a 10-12 slide, 12-15 minute narrative with claim-style titles, speaker notes, transitions, and anticipated questions.
- **Research idea cards**: convert verified gaps into falsifiable hypotheses and decisive experiments.

## The Standard

Every material conclusion records a source locator and is labeled as an author claim, direct evidence, reviewer inference, proposal, or unverified. The skill names the closest comparison target before judging novelty and keeps uncertainty visible instead of filling gaps with confident prose.

## Included References

- [`SKILL.md`](SKILL.md): end-to-end operating workflow.
- [`references/top-venue-rubric.md`](references/top-venue-rubric.md): reviewer-grade contribution and evidence standard.
- [`references/related-work-comparison.md`](references/related-work-comparison.md): mechanism-level comparison matrices and priority checks.
- [`references/group-meeting-deck.md`](references/group-meeting-deck.md): timed presentation narrative, slide template, and discussion preparation.
- [`references/research-idea-cards.md`](references/research-idea-cards.md): falsifiable follow-up research design.
- [`agents/openai.yaml`](agents/openai.yaml): agent metadata for skill discovery.

## Install As A Codex Skill

Copy this repository into your local skills directory using the folder name `group-meeting-paper-review`:

```text
$CODEX_HOME/skills/group-meeting-paper-review/
```

Then ask Codex to review a supplied paper, compare related work, prepare a group-meeting brief, audit the paper like a reviewer, or produce a presentation plan.

## Recommended Review Discipline

Provide the paper PDF or an official paper link when possible. For strong novelty conclusions, include the closest prior work and official artifacts. When evidence is incomplete, the skill is expected to say so explicitly rather than inventing a result.

## Scope

This repository contains the review workflow and reference checklists. It does not bundle papers, datasets, model weights, or proprietary research artifacts.

## License

Released under the MIT License. See [`LICENSE`](LICENSE).
