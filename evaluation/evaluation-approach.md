# Evaluation Approach

*How I am testing whether a reasoning architecture improves judgment rather than merely improving the writing*

> Work in progress | September 2026

## Status and Scope

This is a public evaluation methodology for assessing Full Stack v4.

It is a new portfolio-level evaluation layer. It is **not part of the canonical Full Stack v4 architecture** and does not modify the private Operating Manual or Execution Prompt.

The purpose is to make the evaluation of the system more inspectable without exposing the private implementation.

## Purpose

The central claim behind this repository is not that a reasoning framework can produce cleaner prose.

It is that deliberate reasoning friction may improve diagnosis, calibration, and decision support.

That claim needs a higher standard than a strong example.

This document defines the current public evaluation approach for Full Stack v4. It is a working methodology, not evidence that the system has already been formally validated.

The objective is to make three things inspectable.

1. What kind of reasoning improvement the system is intended to produce
2. How that improvement can be compared against a baseline
3. What evidence would strengthen, weaken, or overturn the belief that the system is useful

## Current Evidence Status

Full Stack v4 is functional and used in live GTM thought leadership and executive work.

The evidence today is repeated practical use, observed reasoning failures, framework revision, and later retesting.

That is evidence of development.

It is not formal validation.

A stronger evaluation approach needs to separate a compelling example from a repeatable result.

## What the Evaluation Should Test

The unit of evaluation is not writing quality alone.

It is the set of **inspectable reasoning artifacts and decisions** produced from the same case, including the diagnosis, evidence use, competing explanations, prognosis, confidence, and recommendation.

A useful comparison should examine whether Full Stack materially changes one or more of the following.

| Dimension | Evaluation question |
| --- | --- |
| **Evidence discipline** | Does the reasoning keep known facts, observations, inference, assumptions, and recommendations appropriately separated? |
| **Competing explanations** | Does it consider credible alternatives before accepting the first plausible diagnosis? |
| **Causal diagnosis** | Does it distinguish the visible symptom from the condition materially governing the outcome? |
| **Prognosis** | Does it explain what the current condition is likely to produce and what could change that trajectory? |
| **Pressure testing** | Does the conclusion survive credible counterarguments, missing context, and disconfirming evidence? |
| **Confidence calibration** | Does confidence reflect the strength of the evidence and causal logic rather than the fluency of the output? |
| **Decision usefulness** | Does the reasoning clarify a decision, change a recommendation, identify better evidence to collect, or prevent an unsupported intervention? |

Decision usefulness is the ultimate application test, but it cannot compensate for weak evidence, unsupported inference, or a weaker causal diagnosis.

If the system makes the reasoning longer without making the judgment more useful, that is not meaningful improvement.

## Baseline Comparison

The working evaluation design compares two responses to the same case.

### Baseline

The model receives the source material, decision question, and relevant context without the Full Stack reasoning architecture.

### Full Stack

The model receives the same case and context with Full Stack v4 applied.

The comparison should use the same underlying evidence.

For a structured comparison, hold constant where practical

- model and model version
- source packet
- decision question
- relevant system context unrelated to Full Stack
- output objective
- access to external tools or additional evidence

Generate the two conditions independently and preserve both original outputs.

Do not revise the framework during evaluation of a fixed test set. If testing reveals a possible framework improvement, treat it as a separate proposed framework change and evaluate it on later cases.

The purpose is not to reward the Full Stack response for being more detailed, more polished, or more assertive.

The question is whether the inspectable reasoning and decision support are materially better.

## What Counts as Material Improvement

A Full Stack response should be classified as improved only when the reasoning intervention produces a meaningful difference.

Examples include

- separating a fact from an unsupported interpretation
- keeping a credible competing explanation open
- moving the diagnosis earlier in the causal chain
- changing the identified governing constraint
- changing the prognosis
- reducing confidence because material evidence is missing
- identifying evidence that would distinguish competing explanations
- changing the recommendation because the diagnosis changed
- preventing action against a symptom when the likely constraint sits elsewhere
- producing a recommendation that better survives contact with operating reality

Better wording alone does not count.

More complexity alone does not count.

Disagreement with the baseline does not count.

The revised reasoning needs to be more defensible or more decision-useful.

## Working Outcome Categories

The current approach uses qualitative outcomes rather than manufactured precision.

| Outcome | Meaning |
| --- | --- |
| **Improved** | The reasoning intervention materially improves diagnosis, calibration, evidence discipline, or decision usefulness |
| **No material change** | The Full Stack response reaches essentially the same defensible reasoning as the baseline |
| **Degraded** | The framework introduces unnecessary complexity, weaker causal logic, unsupported inference, or a worse recommendation |
| **Indeterminate** | The available evidence is insufficient to decide which reasoning path is stronger |

These are working evaluation categories.

They are not benchmark scores and should not be presented as statistical validation.

## Case Design

Strong evaluation requires cases that can expose both strengths and failure modes.

The test set should include more than cases where the first answer is obviously wrong.

It should include cases where

- the obvious diagnosis is wrong
- the obvious diagnosis is substantially correct
- multiple explanations remain credible
- the evidence is incomplete
- a human motive is tempting to infer
- the visible symptom sits downstream of another operating condition
- the recommendation changes depending on the governing constraint
- additional reasoning adds little value

Including cases where the original diagnosis is correct matters.

A system that is rewarded only for finding a different answer can become performatively contrarian rather than more accurate.

## Evaluation Procedure

A structured test should follow the same basic sequence.

### 1. Freeze the case

Create a fixed source packet and decision question.

Do not add evidence to one condition that is unavailable to the other.

### 2. Generate the baseline

Capture the model's initial diagnosis, confidence, recommendation, and supporting rationale without Full Stack.

Preserve the original output.

### 3. Apply Full Stack v4

Run the same case through the current version of the reasoning architecture.

The private implementation can remain private.

The public evaluation record only needs to show the resulting inspectable differences necessary to assess the case.

### 4. Compare the outputs

Inspect the baseline and Full Stack responses against the seven evaluation dimensions.

The review should identify what changed and whether the change mattered.

### 5. Identify the decisive difference

A useful evaluation record should be able to answer a simple question.

**What did the reasoning architecture cause the system to notice, challenge, downgrade, or change that it otherwise did not?**

If the answer is only style, structure, or wording, the case does not demonstrate the intended value.

### 6. Record counterevidence

Document the strongest reason the Full Stack conclusion could still be wrong.

This prevents the evaluation process from becoming a demonstration exercise designed only to confirm the framework.

### 7. Retest the lesson

When a reusable lesson appears, test it against a different case before treating it as evidence for a broader framework change.

A single successful case may justify a working hypothesis.

It does not automatically justify a permanent rule.

## Failure Modes the Evaluation Should Look For

Evaluation should test the framework as aggressively as it tests the baseline.

Known risks include

### Premature closure

The system still accepts the first plausible explanation without meaningfully testing alternatives.

### Evidence inflation

An observation, statement, or inference quietly becomes stronger evidence than the source supports.

### Motive attribution

Observable behavior is converted into assumed intent without adequate evidence.

### Causal overreach

The system moves upstream in the causal chain but selects an explanation that is more interesting than it is supported.

### Forced contrarianism

The framework changes the diagnosis because it is designed to challenge rather than because the evidence justifies a different conclusion.

### Analysis without decision value

The response becomes more elaborate but does not materially clarify what should be believed, investigated, or done.

### False confidence

The output sounds stronger after pressure testing even though important uncertainty remains unresolved.

### Framework theater

The system visibly performs reasoning steps without producing better judgment.

A useful evaluation method needs to record these failures rather than explain them away.

## Human Judgment and Adjudication

Full Stack is intended to support human judgment, not replace it.

For consequential cases, the comparison should be reviewed by a person who understands the underlying domain and can assess whether the diagnosis and recommendation survive contact with the real operating environment.

The reviewer should not be asked only which response sounds better.

The reviewer should assess

- which claims are actually supported
- which causal chain is more defensible
- which uncertainties remain material
- which recommendation better follows from the diagnosis
- what additional evidence would change the conclusion
- whether the intervention is practical in the real business

Where practical, the evaluation should also reduce self-grading bias by

- using a domain-qualified reviewer other than the person who built the case
- hiding which condition used Full Stack when the outputs can reasonably be blinded
- randomizing response order
- preserving reviewer disagreement
- separating reasoning-quality review from writing-style preference

Blinding will not always be possible because the architecture may leave recognizable traces.

It is a bias-reduction technique, not a guarantee of objectivity.

Where reasonable reviewers disagree, the disagreement should remain visible.

Consensus should not be manufactured.

## Repository-Specific Working Evidence Maturity Model

The repository currently distinguishes practical use from formal validation.

For public reporting, I am using the following working maturity model to make that distinction clearer.

This is a **portfolio-specific organizing construct**, not an external research standard and not a component of canonical Full Stack v4.

| Level | Evidence type | What it can support |
| --- | --- | --- |
| **1. Anecdotal example** | One case shows a useful reasoning intervention | Demonstration that the architecture can matter in a specific instance |
| **2. Repeated observation** | Similar failure modes and improvements appear across multiple live cases | Evidence that the pattern may be reusable |
| **3. Structured testing** | Fixed cases, baseline comparisons, predefined criteria, and documented failures | Stronger evidence that the architecture produces repeatable reasoning differences |
| **4. Formal validation** | A defined evaluation protocol with sufficient independent review, repeatability, and methodological rigor | A stronger claim about reliability or generalizability |

This maturity model is part of the public evaluation approach.

It is not a claim that Full Stack has reached Level 4.

The current evidence is best described as repeated practical use and iterative testing, with structured evaluation still being developed.

## What Would Weaken the Full Stack Hypothesis

A serious evaluation approach needs conditions under which confidence should decrease.

Confidence in the framework should weaken if structured testing shows that

- baseline reasoning performs just as well on the dimensions that matter
- Full Stack routinely creates more analysis without changing decision quality
- competing explanations create noise more often than they reduce premature certainty
- the framework systematically favors more complicated causal explanations
- pressure testing increases confidence without improving evidentiary support
- the architecture frequently changes correct diagnoses into weaker ones
- domain reviewers judge the resulting recommendations as less practical
- improvements disappear when cases move outside the examples used to develop the framework

Negative results should change the evaluation of the system and may justify a proposed framework revision.

They should not be treated as exceptions merely because the framework is already useful in some contexts.

Any proposed change to canonical Full Stack should remain separate until explicitly approved and versioned.

## What Formal Validation Would Require

Formal validation would require more than publishing a collection of successful examples.

A stronger protocol would need, at minimum

- a versioned test set
- a fixed comparison procedure
- evaluation criteria defined before reviewing results
- preservation of baseline and Full Stack outputs
- explicit recording of degraded and indeterminate cases
- review that is not based solely on writing quality
- enough independent judgment to reduce self-grading bias
- testing across cases that were not used to create the framework

The exact protocol is not yet defined.

Until it is, the repository should continue to distinguish structured testing from formal validation.

## Public Evaluation Record

Future case studies can use a compact record like this.

| Field | Record |
| --- | --- |
| Case | Anonymized or reconstructed case identifier |
| Decision question | What needed to be diagnosed or decided |
| Evidence boundary | What information was available to both conditions |
| Baseline diagnosis | Initial reasoning without Full Stack |
| Full Stack diagnosis | Revised reasoning with Full Stack |
| Material change | What changed in diagnosis, confidence, evidence requirement, prognosis, or recommendation |
| Strongest counterargument | Best reason the revised conclusion could still be wrong |
| Outcome | Improved, No material change, Degraded, or Indeterminate |
| Reviewer note | Why the classification was assigned |
| Framework implication | No change, working hypothesis, or proposed framework modification |

Public examples should protect confidential employer, client, prospect, and individual information.

Reconstructed cases should be labeled as reconstructed.

## Public and Private Boundary

The evaluation approach should make the reasoning system testable without publishing the complete private implementation.

Public evidence can show

- the case and evidence boundary
- the baseline tendency
- the reasoning failure
- the intervention at an architectural level
- the revised diagnosis
- the change in confidence or recommendation
- the adjudication
- what remains uncertain

The detailed operating prompt, private decision rules, hidden reasoning traces, and proprietary execution mechanics do not need to be disclosed for the comparison to be inspectable.

## Current Next Step

The next step is not to claim validation.

It is to create a small set of structured, anonymized or reconstructed cases and apply this comparison method consistently.

That work should make failures visible as readily as successes.

The repository becomes more credible when the evaluation process can show not only where the reasoning architecture helps, but also where it does not.
