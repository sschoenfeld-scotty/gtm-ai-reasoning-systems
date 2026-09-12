# Full Stack v5 Evaluation Plan

*How I plan to test the reasoning capability added in v5 without rewriting the v4 evidence history*

> Work in progress | September 2026

## Status and Scope

This document defines the public evaluation plan for the new reasoning capability introduced in Full Stack v5.

It is not evidence that v5 has already been validated.

Existing Full Stack v4 evidence remains v4 evidence. The reconstructed cases, Evaluation Approach, and Independent Review Protocol were developed around v4 and should not be silently relabeled as proof that v5 Strategic Adjudication works.

The purpose of this plan is narrower.

It asks whether v5 improves decision quality in cases where the diagnosis may already be correct but the decision to intervene is still uncertain.

## What Changed in v5

Full Stack v5 preserves the diagnostic disciplines developed through v4 and adds an explicit decision gate between prognosis and intervention.

That gate, **Strategic Adjudication**, asks two additional questions at a public level.

1. Does the proposed action create credible material downside that is difficult or impossible to reverse?
2. Is the diagnosed problem worth solving relative to credible competing uses of scarce resources?

A separate conditional **Communication Function** check is also available when misunderstanding the purpose or audience of a statement could materially change the diagnosis.

The evaluation therefore has to test more than whether v5 produces a different answer.

It has to test whether the new reasoning changes the decision for a defensible reason.

## Primary Evaluation Question

The central evaluation question is

> **When Full Stack v4 and Full Stack v5 reach the same or materially similar diagnosis, does v5 make a better decision about whether and how to act?**

That isolates the new reasoning capability rather than giving v5 credit for diagnostic improvements inherited from v4.

## Primary Comparison Design

The strongest first comparison is **v4 versus v5 on the same frozen case**.

Both conditions should receive the same source packet, decision question, model context, tool access, and output objective.

The v4 condition uses the preserved v4 implementation.

The v5 condition uses the current v5 implementation.

The comparison should focus on whether the new decision gate changes the recommendation, confidence, risk boundary, or resource-allocation judgment in a way that is better supported by the same evidence.

A separate baseline-versus-v5 comparison can still be useful for broader system evaluation, but it does not isolate the incremental value of the v5 architecture change as cleanly.

## What the Evaluation Should Test

| Dimension | Evaluation question |
| --- | --- |
| **Diagnostic continuity** | Does v5 preserve a sound diagnosis rather than changing it merely to justify a different recommendation? |
| **Communication function discipline** | When communication purpose matters, does v5 distinguish plausible functions without converting incentive or context into unsupported motive? |
| **Ruin and irreversibility** | Does v5 identify credible material irreversible downside without treating theoretical catastrophe as an automatic veto? |
| **Strategic worth** | Does v5 make scarce-resource tradeoffs explicit rather than assuming every diagnosed constraint deserves intervention? |
| **Decision boundary** | Does the new reasoning change action only when the evidence supports a materially different strategic choice? |
| **Non-intervention quality** | When v5 recommends not fixing a diagnosed problem, is that conclusion based on explicit evidence and tradeoffs rather than avoidance or preference? |
| **Confidence calibration** | Does uncertainty remain visible around risk, opportunity cost, communication intent, and strategic value? |
| **Operating usefulness** | Does the resulting decision survive practical scrutiny around ownership, timing, implementation, and consequences? |

## Required Case Types

The first v5 case set should deliberately include situations capable of exposing both value and failure.

### Correct diagnosis, wrong intervention

The governing constraint is correctly identified, but fixing it is strategically inferior to tolerating, containing, deferring, exiting, or reallocating resources.

### Attractive optimization with irreversible downside

The intervention has meaningful expected upside but also a credible path to material downside that cannot easily be reversed or contained.

### Fixable constraint with stronger competing use of resources

The diagnosed problem is real and solvable, but another use of capital, attention, time, talent, trust, or organizational capacity has greater strategic value.

### Misread communication function

A statement appears operational on the surface, but the decision quality changes when its broader communication function is considered.

### False-positive ruin case

The severe-downside story sounds plausible but is not sufficiently credible or material. A strong v5 response should avoid turning caution into paralysis.

### False-positive opportunity-cost case

The framework is tempted to use focus or resource tradeoffs as an excuse to avoid necessary but difficult work. A strong v5 response should reject unsupported non-intervention.

## Evaluation Procedure

### 1. Freeze the case

Create a fixed evidence packet and decision question.

Do not give one version evidence that the other does not receive.

### 2. Run the v4 condition

Capture the diagnosis, prognosis, confidence, recommendation, and supporting rationale using the preserved v4 implementation.

Do not alter v4 to make it more competitive with v5.

### 3. Run the v5 condition

Use the same case and context with the current v5 architecture.

Capture the diagnosis, Strategic Adjudication result when material, confidence, recommendation, and supporting rationale.

### 4. Separate diagnosis from decision

The comparison should explicitly record whether the diagnosis changed.

If the diagnosis is materially the same but the recommendation changes, identify the exact strategic reason for the change.

That is the core v5 test.

### 5. Inspect the new reasoning for false positives

A v5 result is not better merely because it is more cautious, more strategic-sounding, or more complex.

Reviewers should test whether the claimed irreversible downside is credible, whether the opportunity cost is explicit, and whether the competing use of resources is real rather than invented.

### 6. Record the strongest counterargument

For every v5 recommendation, record the strongest credible reason that v4 may still be the better decision.

This is especially important when v5 recommends non-intervention.

### 7. Preserve the original outputs

Do not rewrite either condition after seeing the comparison.

If evaluation reveals a framework weakness, record it as a proposed future change and test it separately.

## Working Outcome Categories

The existing qualitative categories remain useful.

| Outcome | Meaning in the v5 comparison |
| --- | --- |
| **Improved** | v5 materially improves the strategic decision while preserving or strengthening evidence discipline |
| **No material change** | v5 adds little because the v4 recommendation was already strategically sound |
| **Degraded** | v5 introduces unsupported risk aversion, invented opportunity cost, unnecessary complexity, or a worse decision |
| **Indeterminate** | The frozen evidence is insufficient to determine which decision is stronger |

These are not benchmark scores or statistical validation.

## What Counts as Material Improvement

Material improvement requires more than a different recommendation.

Examples include

- preserving the diagnosis while correctly changing the action
- identifying a credible irreversible downside that v4 underweighted
- showing that a fixable constraint is not worth the resources required
- distinguishing a communication function that materially changes the decision frame without inventing motive
- converting an automatic intervention into a defensible containment, deferral, exit, or reallocation decision
- rejecting a false ruin story and preserving rational action
- rejecting a weak opportunity-cost argument and preserving necessary intervention

Better prose alone does not count.

More strategic language alone does not count.

Longer reasoning alone does not count.

## Failure Modes the Evaluation Must Look For

### Generalized risk aversion

Strategic Adjudication becomes a reason to avoid action whenever downside exists.

### Catastrophe inflation

A theoretical severe outcome is treated as a credible decision boundary without enough evidence.

### Opportunity-cost invention

The system invents a better alternative use of resources rather than grounding the tradeoff in the case.

### Executive-intuition laundering

Preference is restated as strategic judgment without evidence.

### Communication-intent overreach

Audience, incentives, or timing are converted into asserted motive.

### Non-intervention bias

The existence of a new decision gate causes the framework to overvalue doing nothing.

### Diagnostic contamination

The diagnosis is altered after the fact to rationalize the preferred strategic decision.

## Evidence Boundary

The current evidence status should remain explicit.

Full Stack v4 has practical-use evidence, observed failure modes, iterative revisions, reconstructed comparisons, and an independent review protocol prepared around its frozen case set.

Full Stack v5 inherits the architecture that produced that development history, but the new Strategic Adjudication capability has not yet earned the same evidence status.

Until v5-specific cases are run and reviewed, the correct claim is

> **v5 is an accepted architecture change with a defined evaluation plan, not a validated improvement claim.**

## Relationship to Existing Evaluation Artifacts

The [Evaluation Approach](./evaluation-approach.md) remains the public methodology for the v4 comparison work.

The [Independent Review Protocol v1](./independent-review-protocol.md) remains tied to the frozen reconstructed v4 cases.

Those artifacts should remain unchanged as part of the historical evidence trail.

This v5 plan is additive. It exists to evaluate the new decision capability without rewriting the meaning of earlier evidence.

## Next Evidence Step

The next useful step is to build a small frozen v5 case set that includes both positive and negative tests of Strategic Adjudication.

The case set should be designed so v5 has an opportunity to improve the decision, add no value, and make the decision worse.

A framework becomes more credible when the evaluation is capable of showing that it failed.
