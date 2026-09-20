# Human Pattern 1

> Public architecture note | Full Stack v5 capability | September 2026

## Status

Human Pattern 1 is an established capability inside Full Stack v5.

It is not a standalone framework, a personality model, or a motive-detection system.

The private Full Stack Operating Manual and Execution Prompt remain the canonical implementation. This document publishes enough of the architecture to make the reasoning inspectable without exposing the complete operating procedure.

## Why It Exists

Human behavior can be causally important without making human motive directly observable.

A manager may preserve weak pipeline because of fear, incentives, role ambiguity, reporting mechanics, political pressure, poor judgment, or some combination of those conditions.

A buyer may delay because priorities changed, procurement incentives differ from the economic buyer's, internal risk increased, budget moved, or the original urgency was never as strong as the seller believed.

The visible behavior can be real while the explanation remains uncertain.

That creates two opposite reasoning failures.

The first is **motive inflation**. A plausible explanation becomes treated as fact.

The second is **behavioral paralysis**. The system refuses to make a useful decision until motive can be known with certainty.

Human Pattern 1 is designed to avoid both.

## Governing Ideas

> **Begin with behavior before motive.**

Observed behavior can establish that something happened or repeated. It does not automatically establish why.

> **A stated explanation is evidence of the current account, not privileged access to motive.**

What a person says about their reasoning matters. It can be well supported, incomplete, strategic, mistaken, or difficult to verify. The framework does not assume either honesty or deception.

> **Systemic and structural conditions can produce behavior that looks personal.**

Compensation design, role constraints, reporting mechanics, approval systems, resource limits, organizational politics, governance, manager behavior, and performance pressure can shape behavior.

That does not mean the system always explains the person.

Structural pressure and individual agency can operate together.

> **Experience can inform the prior. It does not prove the current case.**

Repeated analogous operating experience can legitimately change which explanation appears more plausible. Current-case evidence still has to update that prior.

> **Behavioral uncertainty does not automatically require decision uncertainty.**

A decision may remain supportable even when the exact behavioral driver is unresolved.

## Public Architecture

Human Pattern 1 uses a small set of distinctions rather than a psychological story.

### 1. Separate behavior, account, and inference

The framework keeps three things distinct.

**Observed behavior**  
What the person or group actually did, said, changed, avoided, repeated, or stopped doing.

**Stated account**  
What the actor says explains the behavior.

**Inferred driver**  
The explanation that currently appears to fit the evidence best.

Keeping those states separate prevents a confident narrative from silently upgrading itself into fact.

### 2. Test the operating system before over-attributing the person

When behavior materially affects the diagnosis, the framework asks whether the surrounding system could plausibly produce the same pattern.

This can include incentives, authority, information asymmetry, reporting rules, organizational pressure, role design, workflow, governance, resource constraints, or political conditions.

The question is not whether the behavior is "really" structural or personal.

The question is whether the diagnosis changes when both explanations are considered.

### 3. Preserve a credible alternative when it matters

Human Pattern 1 does not generate long lists of possible motives for analytical appearance.

It preserves the strongest credible alternative when that alternative could materially change the diagnosis, confidence, prognosis, or candidate action.

If two explanations would lead to the same reasoning outcome, the uncertainty can remain unresolved.

### 4. Use experience without laundering it into evidence

Experienced operators often recognize patterns faster than a generic reasoning process can reconstruct them from first principles.

That can be useful.

It can also create premature closure.

Human Pattern 1 therefore allows materially similar experience to inform prior plausibility while keeping the present case challengeable.

Seniority alone is not evidence.

Pattern recognition remains revisable.

### 5. Add human context without surrendering independent judgment

Sometimes the model lacks context that a person close to the situation possesses.

When that missing context could actually change the reasoning, Full Stack can seek a targeted human judgment.

The architecture preserves the model's pre-existing read before incorporating the new context.

The user's experience can strengthen, weaken, or fail to resolve the behavioral inference. It is not automatically adopted as truth.

### 6. Stop when more behavioral certainty would not improve the decision

Behavioral reasoning is not useful merely because it produces a richer explanation of people.

The framework asks whether resolving the ambiguity would materially change the reasoning.

If not, it preserves the uncertainty and continues.

This is deliberate reasoning friction with a stopping rule.

### 7. Hand unresolved behavioral uncertainty downstream

Human Pattern 1 does not decide whether to act, wait, stage, contain, or accept uncertainty.

That responsibility remains with Strategic Adjudication.

The behavioral layer calibrates what is known about the human explanation.

The decision layer weighs that uncertainty alongside reversibility, irreversible downside, scarce-resource tradeoffs, cost of delay, and opportunity cost.

## Behavioral Inference Discipline

Behavioral Inference Discipline is the sixth named Full Stack v5 refinement.

Its primary execution home is Human Pattern 1, but it also interacts with Evidence Discipline, Competing Explanations, Perspective Triangulation, Operator Proof, Anchoring Resistance, and Strategic Adjudication.

The refinement was added because the earlier behavioral guardrail was necessary but incomplete.

Saying "behavior does not prove motive" prevents overclaiming.

It does not by itself tell the system

- when behavioral ambiguity deserves more analysis
- how to distinguish personal explanations from system-generated behavior
- how to use experienced pattern recognition without treating it as proof
- when missing human context is worth requesting
- when unresolved motive can remain unresolved
- where the final action decision belongs

Behavioral Inference Discipline makes those responsibilities more explicit without creating another peer stage in Full Stack's reasoning spine.

## Relationship to the Behavioral Inference Engine

The [Behavioral Inference Engine](../research/behavioral-inference-engine.md) remains a work-in-progress research direction.

Several bounded BIE disciplines are now sufficiently defined to inform Full Stack v5 through Behavioral Inference Discipline.

The unresolved BIE problem is longitudinal.

How should behavioral hypotheses persist across interactions?

How should confidence accumulate or decay?

What should happen when context changes?

When should contradictory evidence revise the model?

When should an outlier change the model rather than remain an exception?

The boundary is

> **Full Stack decides how much behavioral inference the current decision requires. BIE develops how behavioral understanding should accumulate and revise across time.**

## What Human Pattern 1 Is Not

Human Pattern 1 is not

- a personality assessment
- a psychological diagnosis
- a motive detector
- a behavioral scoring system
- a substitute for direct evidence
- a claim that experienced operators are automatically right
- a requirement to explain every human action before making a decision
- a longitudinal model of an individual

The goal is better diagnosis, not more sophisticated speculation about people.

## Evidence and Limits

Human Pattern 1 and Behavioral Inference Discipline are part of the current Full Stack v5 architecture.

That status means the reasoning design has been accepted into the framework.

It does **not** mean the refinement has been formally validated.

The [Full Stack v5 Evaluation Plan](../evaluation/full-stack-v5-evaluation-plan.md) now includes positive and negative tests for the behavioral reasoning layer, including cases where structural conditions are mistaken for personal motive, experience produces premature closure, human context changes the inference, or motive remains uncertain while the decision can still proceed.

The evaluation standard is not whether the framework produces a richer behavioral narrative.

The standard is whether the added reasoning improves diagnosis or decision quality without creating unsupported motive claims or unnecessary analytical friction.

## Public and Private Boundary

This note publishes the architectural distinctions and the reasoning problem they address.

The private implementation retains the complete trigger logic, operating sequence, clarification procedure, execution wording, and integration details used to run the system.

The public claim should remain proportional to what has actually been designed and tested.
