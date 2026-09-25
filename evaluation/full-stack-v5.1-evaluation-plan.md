# Full Stack v5.1 Evaluation Plan

*How I plan to test Compressed Diagnosis without relabeling earlier evidence*

> Work in progress | September 2026

## Status and Scope

This document defines the public evaluation plan for the additive reasoning capability introduced in Full Stack v5.1.

That capability is **Compressed Diagnosis**.

Full Stack v5.1 preserves the governing v5 reasoning spine. It adds an explicit decision about whether additional diagnostic expansion is likely to improve the decision enough to justify the time, delay, opportunity cost, or other consequence required to obtain more evidence.

This plan is not evidence that Compressed Diagnosis has been validated.

Existing v4 evidence remains v4 evidence.

Existing v5 evidence remains v5 evidence.

The v5 evaluation cases, field observations, and evaluation plan should not be silently relabeled as proof that v5.1 works.

## What Changed in v5.1

Compressed Diagnosis adds one recurring reasoning capability.

The system can now inspect whether a strong prior makes additional diagnostic work low value relative to its cost.

A strong prior may come from repeated materially analogous operating experience, accumulated prior evidence, or another established pattern that has survived later outcome testing.

The capability does not permit prescription without diagnosis.

It permits diagnostic work to be compressed when the evidence is sufficient for the decision being made.

The public principles are

> **Experience can compress diagnosis without bypassing it.**

> **Learning may transfer across contexts. Diagnosis does not.**

Reasoning depth and diagnostic expansion remain separate.

Deep reasoning can conclude that more evidence collection is not worth the delay.

Compressed Diagnosis cannot override material contradictory evidence or turn familiarity, confidence, seniority, or repeated exposure into proof.

## Primary Evaluation Question

> **Can Full Stack v5.1 reduce unnecessary diagnostic expansion when a strong prior and bounded action justify it without creating premature certainty or weaker decisions?**

The companion question is

> **Does v5.1 expand the diagnosis when novelty, contradiction, irreversibility, asymmetric downside, or path dependency makes compression unsafe?**

## What the Evaluation Should Test

### Evidence sufficiency

Does the system distinguish evidence sufficiency from evidence volume?

Does it identify when the available prior is strong enough for the decision without pretending that the current case has been independently verified?

### Diagnostic compression

Does the system reduce diagnostic expansion only when the prior is materially analogous and the action context supports it?

Does it keep remaining uncertainty visible?

### Cost of additional information

Does the system ask whether more evidence is likely to change the decision enough to justify the delay or opportunity cost required to obtain it?

Does it avoid treating more information as automatically better reasoning?

### Contradictory evidence

Does material contradictory evidence defeat or materially weaken the prior?

Does the system expand the diagnosis rather than protect a familiar pattern?

### Reasoning depth independence

Can Deep Path reasoning still produce a compressed diagnosis when additional evidence has low expected decision value?

Can Compressed Diagnosis remain unavailable when the case contains material risk that requires diagnostic expansion?

### Prognosis and Strategic Adjudication

When diagnosis is compressed, does remaining uncertainty stay visible in Prognosis?

When consequence is material, does Strategic Adjudication compare the risk of acting under uncertainty with the cost of waiting?

### Diagnostic probes

When a bounded reversible intervention can produce discriminating evidence more efficiently than waiting, does the system define what would strengthen, weaken, or defeat the diagnosis?

Does the response re-enter the reasoning cycle as new evidence?

### Transfer across contexts

When learning from one case is brought into another, does the system reuse the learning without silently importing the earlier diagnosis?

## Required Case Types

### Strong prior with low-regret action

A repeated materially analogous pattern exists, no material contradiction is known, the first action is bounded and reversible, and delay carries meaningful cost.

The expected behavior is compression.

### Strong prior with irreversible downside

The historical pattern is strong, but the proposed action could create material difficult-to-reverse harm.

The expected behavior is diagnostic expansion or staged exposure rather than automatic compression.

### Familiar pattern with contradictory evidence

The case resembles a known pattern, but current evidence materially conflicts with it.

The expected behavior is to weaken or reject the prior.

### False analogy

Surface features match a familiar pattern while the causal structure differs.

The expected behavior is to detect the mismatch before the prior controls the diagnosis.

### Deep reasoning with low information value

The user selects the deepest reasoning level, but additional evidence is unlikely to change a bounded decision enough to justify delay.

The expected behavior is rigorous justification for compression rather than maximum evidence collection.

### Diagnostic probe

A reversible action can produce more discriminating evidence than passive observation.

The expected behavior is to define the probe, preserve uncertainty, and specify what response would change the model.

### Cross-context transfer

A useful lesson from one operating context is applied to a different context.

The expected behavior is to transfer the learning while re-diagnosing the new case.

### Favorable outcome through another mechanism

A compressed diagnosis leads to a successful outcome, but another credible mechanism could explain the result.

The expected behavior is confidence update without causal overclaim.

## Evaluation Procedure

### 1. Freeze the case

Preserve the evidence available before the decision.

Record the prior pattern being used, what makes the analogy material, known contradictions, the proposed action, reversibility, downside, and the cost of delay.

### 2. Run the historical v5 condition

Use the frozen v5 architecture.

Preserve the diagnosis, evidence requests, reasoning depth, prognosis, action decision, and confidence.

### 3. Run the v5.1 condition

Use the same frozen case.

Record whether Compressed Diagnosis activated and why.

Record what additional evidence was not pursued and why.

### 4. Compare diagnostic expansion

Determine whether v5.1 reduced, preserved, or increased diagnostic work.

Do not treat less analysis as improvement by itself.

### 5. Compare the decision

Inspect whether the recommendation or action changed.

When it did, identify which v5.1 reasoning distinction caused the change.

### 6. Inspect residual uncertainty

Confirm that compression did not convert uncertainty into false fact, motive, or causality.

### 7. Inspect evidence acquisition value

Determine whether skipped evidence was actually unlikely to change the decision enough to justify delay.

If later evidence shows that the skipped information would have materially changed the decision, record that as a failure or boundary condition.

### 8. Inspect diagnostic probes

When an intervention functioned as a probe, preserve the predicted strengthening and weakening signals before the result is known.

Then evaluate the response through Recursive Evidence Re-entry.

### 9. Preserve outcome attribution discipline

A successful outcome can strengthen confidence.

It does not automatically prove that the compressed diagnosis was correct.

A failed outcome can weaken confidence without proving that compression itself was the cause.

### 10. Preserve the original outputs

Do not improve either condition after the comparison.

If evaluation exposes a framework weakness, record it separately and test it before changing the framework again.

## Working Outcome Categories

| Outcome | Meaning |
| --- | --- |
| **Material improvement** | v5.1 changes diagnostic effort or action in a way that improves decision quality or avoids material delay without weakening evidence discipline |
| **Useful compression** | v5.1 reduces diagnostic work while preserving a defensible decision and visible uncertainty |
| **No material difference** | v5 and v5.1 reach materially similar reasoning and action |
| **Over-compression** | v5.1 acts on a prior that should have been challenged or expanded |
| **Under-compression** | v5.1 gathers additional evidence that has little expected decision value relative to its cost |
| **Indeterminate** | the case does not provide enough evidence to distinguish the conditions |

## Failure Modes the Evaluation Must Look For

### Intuition laundering

Experience is treated as proof merely because the operator is confident or senior.

### Familiarity substitution

Recognition of a familiar surface pattern is mistaken for evidence that the causal structure matches.

### Premature compression

The system stops diagnostic expansion before material contradiction, novelty, or downside is adequately inspected.

### Diagnostic bureaucracy

The system continues gathering evidence when the information is unlikely to change the decision enough to justify delay.

### Route collapse

Deep reasoning is mistaken for maximum evidence collection, or Compressed Diagnosis is mistaken for Fast Path.

### Evidence-value confusion

The framework evaluates evidence quality without evaluating whether obtaining more evidence is worth the cost.

### Probe confirmation bias

A diagnostic probe is designed so almost any response appears to confirm the preferred diagnosis.

### Transfer collapse

A lesson from one context is treated as a diagnosis of another context without re-evaluation.

### Outcome laundering

A favorable result is treated as proof that the original compressed diagnosis was causally correct.

### Contradiction suppression

Current evidence that materially weakens the prior is discounted because the historical pattern feels established.

## Evidence Boundary

The current basis for Compressed Diagnosis includes repeated naturalistic operator observation and framework-development work that exposed the mechanism clearly enough to audit architecturally.

That is meaningful development evidence.

It is not formal validation.

Private operating examples should not be published merely to make the framework appear better supported.

Public evidence should remain proportional to what can be safely disclosed and what the evaluation actually tested.

## Relationship to Earlier Evaluation

The [Full Stack v5 Evaluation Plan](full-stack-v5-evaluation-plan.md) remains the historical plan for Strategic Adjudication and the v5 refinements.

The [Evaluation Approach](evaluation-approach.md) and [Independent Review Protocol v1](independent-review-protocol.md) remain part of the broader evaluation discipline.

v5.1 should inherit useful evaluation controls without relabeling earlier results.

## Next Evidence Step

The next evidence work should use naturally occurring cases where diagnostic delay, experienced priors, reversibility, or information value are already part of the real decision.

The objective is not to manufacture cases that make Compressed Diagnosis look useful.

The objective is to find where compression improves judgment, where it adds no value, and where it fails.
