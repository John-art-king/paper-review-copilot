# Meeting Pack Preview

> Synthetic demonstration only. The paper, method, numbers, and locators below are fictional and exist solely to show the output contract.

## Review Profile

Chinese · field specialists · 15 minutes · meeting pack · reviewer-critical

## Executive Verdict

- **Research question:** Can selective retrieval reduce long-context reasoning cost without discarding evidence needed for multi-hop answers?
- **Core insight:** Route each reasoning step to a small evidence subset instead of pruning the context once at input time.
- **Mechanism:** step-aware query state -> evidence routing -> constrained reasoning -> lower active context.
- **Strongest evidence:** under a matched model and token budget, the full method improves answer accuracy over static pruning; see fictional Table 2.
- **Largest uncertainty:** the routing ablation changes both selection policy and training signal, so the claimed causal mechanism is not isolated.
- **Verdict:** promising mechanism with incomplete causal evidence. Worth discussing; reproduce the routing comparison before building on it.

## Claim-Evidence Ledger

| Claim | Status | Locator | Establishes | Does not establish | Confidence |
|---|---|---|---|---|---|
| Step-aware routing improves accuracy at matched active context | Evidence | Fictional Table 2 | Better result under the reported protocol | Generalization beyond two datasets | Medium |
| Dynamic routing is the cause of the gain | Author claim | Fictional Sec. 3, Table 4 | Components jointly matter | Routing alone explains the gain | Low |
| The method is practical for long documents | Inference | Fictional Fig. 5 | Lower active-token count | End-to-end latency or memory benefit | Low |

## Novelty Delta

**Closest predecessor:** static evidence pruning before generation.  
**Exact delta:** evidence is reselected after each reasoning state update.  
**Why it may matter:** later reasoning steps can recover evidence that an input-only selector would discard.  
**Missing decisive test:** compare static and dynamic routing with identical selector capacity, supervision, and retrieval calls.

## Three Claim-Style Slides

1. **Input-only pruning fails when later reasoning changes what evidence matters**
2. **The paper turns evidence selection into a step-conditioned operation**
3. **Reported gains are credible, but the routing mechanism remains under-isolated**

## Advisor-Style Question

**Question:** How do you know the gain comes from dynamic routing rather than extra supervision?  
**Short answer:** We do not know from the reported ablation.  
**Status:** unresolved.  
**What would change the answer:** a matched-supervision static selector and a routing-only intervention.

## Follow-Up Idea

**Hypothesis:** dynamic evidence recovery helps only when supporting facts become identifiable after an intermediate reasoning step.  
**Decisive experiment:** stratify examples by whether later-hop evidence is lexically recoverable from the initial query, then compare matched static and dynamic selectors.  
**Falsification:** no interaction between recoverability stratum and routing strategy.
