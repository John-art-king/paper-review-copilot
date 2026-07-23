# Advisor-Style Q&A Rehearsal

Use this guide after the evidence ledger and presentation argument are stable. The goal is to expose weak reasoning before the meeting, not to generate polished evasions.

## Question Ladder

Generate questions across five levels:

1. **Comprehension**: What exactly is the task, input, output, and mechanism?
2. **Causality**: Why should this component produce the claimed effect?
3. **Fairness**: Are data, compute, tuning, and evaluation budgets matched?
4. **Boundary**: Where does the method fail, and which assumption breaks first?
5. **Research value**: What should the lab test, reproduce, or challenge next?

Include at least one question that attacks the central novelty claim and one that attacks the strongest experimental result.

## Answer Contract

For every question, provide:

```text
Question:
Short answer:
Evidence and locator:
Status: supported | inferred | unresolved
Residual uncertainty:
What would change the answer:
```

Keep the short answer speakable in 20-40 seconds. Do not hide an unresolved issue behind background explanation.

## Red-Team Round

End with three adversarial prompts:

- the strongest plausible rejection argument;
- the simplest alternative explanation for the headline gain;
- the missing experiment most likely to reverse the verdict.

Then revise the final slide or speaker notes wherever the current narrative overstates the evidence.
