# Full Stack v5 Evaluation Plan

*How I plan to test the reasoning capability added in v5 and its current refinements without rewriting the v4 evidence history*

> Work in progress | September 2026

## Status and Scope

This document defines the public evaluation plan for the new reasoning capability introduced in Full Stack v5 and the later refinements now inside the current v5 architecture.

It is not evidence that v5 has already been validated.

Existing Full Stack v4 evidence remains v4 evidence. The reconstructed cases, Evaluation Approach, and Independent Review Protocol were developed around v4 and should not be silently relabeled as proof that v5 Strategic Adjudication, Reasoning Depth Routing, Reflexivity, Cascade Integrity, Decision Trace Integrity, or Anchoring Resistance work.

The purpose of this plan is narrower.

It asks whether v5 improves decision quality in cases where the diagnosis may already be correct but the decision to intervene is still uncertain, whether it obtains explicit user consequence before routing and honors that declaration as the minimum reasoning depth, whether it escalates when observable reasoning risk warrants it, whether it detects causal feedback created by signaling without inventing causality, whether it catches material translation failure without assuming organizational handoffs are inherently destructive, whether it preserves enough decision history to evaluate later reasoning without confusing retrospective explanation with contemporaneous evidence, and whether Deep Path reasoning can resist a substantive user-supplied anchor without manufacturing disagreement or unnecessary process.

## What Changed in v5

Full Stack v5 preserves the diagnostic disciplines developed through v4 and adds an explicit decision gate between prognosis and intervention.

That gate, **Strategic Adjudication**, asks two additional questions at a public level.

1. Does the proposed action create credible material downside that is difficult or impossible to reverse?
2. Is the diagnosed problem worth solving relative to credible competing uses of scarce resources?

A separate conditional **Communication Function** check is also available when misunderstanding the purpose or audience of a statement could materially change the diagnosis.

Five later refinements now sit inside the same v5 architecture.

- **Reasoning Depth Routing** requires explicit user-declared consequence before routing, treats that declaration as the minimum reasoning depth, and allows observable reasoning risk to escalate the route.
- **Reflexivity** sits inside System Dynamics and tests whether signaling itself changes the resources or behavior that govern feasibility.
- **Cascade Integrity** sits inside Operator Proof and tests whether strategic intent materially changes as it travels through organizational handoffs.
- **Decision Trace Integrity** distinguishes retrospective rationale from contemporaneous decision evidence and preserves a compact decision state when consequence warrants later comparison.
- **Anchoring Resistance** activates on Deep Path work when the user supplies a substantive preferred hypothesis, diagnosis, conclusion, recommendation, or argument. It tests what the evidence supports independently, compares that with the strongest defensible preferred position, and checks whether the initial frame materially affected evidence selection, weighting, confidence, diagnosis, or action.

The evaluation therefore has to test more than whether v5 produces a different answer.

It has to test whether the added reasoning changes the decision or execution path for a defensible reason without creating avoidable analytical weight, unsupported causal stories, unjustified distrust of self-report, unnecessary trace bureaucracy, unsupported consequence inference, routing-gate bypass, user-anchor capture, or unnecessary Deep Path ceremony.

## Primary Evaluation Question

The central evaluation question remains

> **When Full Stack v4 and Full Stack v5 reach the same or materially similar diagnosis, does v5 make a better decision about whether and how to act?**

That isolates the major v5 reasoning capability rather than giving v5 credit for diagnostic improvements inherited from v4.

The current refinements add five secondary questions.

> **Does v5 obtain explicit user consequence before routing, honor it as the minimum reasoning depth, and escalate only when observable reasoning risk warrants it?**

> **When signaling changes the system, does v5 detect the reflexive loop without confusing influence with proof of causality?**

> **When a decision passes through an organization, does v5 identify material translation variance without assuming middle management is the problem?**

> **When a prior decision is revisited, does v5 distinguish the current explanation from contemporaneous evidence of what was believed, expected, and chosen at the time?**

> **When Deep Path work begins with a substantive preferred position, does v5 test the evidence independently enough to detect material framing effects without treating the user's view as presumptively wrong?**

## Primary Comparison Design

The strongest first comparison is **v4 versus v5 on the same frozen case**.

Both conditions should receive the same source packet, decision question, model context, tool access, and output objective.

The v4 condition uses the preserved v4 implementation.

The v5 condition uses the current v5 implementation.

The comparison should focus on whether the new decision gate or later v5 refinements change the recommendation, confidence, risk boundary, resource-allocation judgment, reasoning depth, causal model, execution assessment, interpretation of prior reasoning, or handling of a user-supplied preferred position in a way that is better supported by the same evidence.

A separate baseline-versus-v5 comparison can still be useful for broader system evaluation, but it does not isolate the incremental value of the v5 architecture change as cleanly.

## What the Evaluation Should Test

| Dimension | Evaluation question |
| --- | --- |
| **Diagnostic continuity** | Does v5 preserve a sound diagnosis rather than changing it merely to justify a different recommendation? |
| **Communication function discipline** | When communication purpose matters, does v5 distinguish plausible functions without converting incentive or context into unsupported motive? |
| **Ruin and irreversibility** | Does v5 identify credible material irreversible downside without treating theoretical catastrophe as an automatic veto? |
| **Strategic worth** | Does v5 make scarce-resource tradeoffs explicit rather than assuming every diagnosed constraint deserves intervention? |
| **Reasoning depth routing** | Does v5 obtain explicit user consequence before routing, treat that declaration as the minimum reasoning depth, and escalate only when observable reasoning properties such as reversibility, evidence quality, causal uncertainty, stakeholder complexity, material tradeoffs, or credible irreversible downside warrant deeper scrutiny? |
| **Reflexivity discipline** | When signaling changes resources or behavior, does v5 identify the feedback loop without treating narrative influence as automatic proof of the later outcome? |
| **Cascade integrity** | Does v5 identify material translation variance across organizational handoffs without assuming that local adaptation is necessarily distortion? |
| **Decision trace integrity** | Does v5 distinguish retrospective rationale from contemporaneous evidence and preserve enough original decision state to support later evaluation when consequence warrants it? |
| **Anchoring resistance** | On Deep Path work with a substantive preferred position, does v5 establish an independent evidentiary baseline, test the strongest defensible version of the preferred position, and identify material framing effects without manufacturing disagreement or discarding relevant evidence merely because it was collected after the preference formed? |
| **Decision boundary** | Does the new reasoning change action only when the evidence supports a materially different strategic choice? |
| **Non-intervention quality** | When v5 recommends not fixing a diagnosed problem, is that conclusion based on explicit evidence and tradeoffs rather than avoidance or preference? |
| **Confidence calibration** | Does uncertainty remain visible around risk, opportunity cost, communication intent, reflexivity, translation effects, retrospective rationale, anchoring risk, and strategic value? |
| **Operating usefulness** | Does the resulting decision survive practical scrutiny around ownership, timing, implementation, handoffs, trace burden, framing risk, and consequences? |

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

### Reflexive narrative loop

A strategic signal changes capital, talent, customer confidence, partner behavior, competitive behavior, or another operating condition that materially changes whether the original claim can become true.

A strong v5 response should detect the loop while keeping the causal attribution appropriately qualified.

### False-positive reflexivity case

A narrative and an operational outcome move together, but the frozen evidence does not establish that the signal changed the resources or behavior governing the outcome.

A strong v5 response should resist turning correlation or sequence into a reflexive causal story.

### Cascade translation failure

Executive intent is coherent, but incentives, handoffs, process design, or localized risk management materially change the behavior that reaches the frontline or customer.

A strong v5 response should identify where the translation changed without reducing the explanation to motive attribution.

### Beneficial local translation

A local manager or operating team modifies an executive directive because field evidence exposes a weakness in the original decision.

A strong v5 response should not treat every deviation from executive intent as execution failure.

### Explicit routine consequence with Fast Path appropriate

The user explicitly states that the task is routine and easily reversible. The evidence is adequate, the causal scope is narrow, and there is no material stakeholder complexity, scarce-resource tradeoff, or credible irreversible downside.

A strong v5 response should make Fast Path eligible without adding analytical ceremony that does not improve the decision.

### No consequence declaration

The user invokes Full Stack but does not establish how consequential it would be to get the reasoning wrong.

A strong v5 response should ask the mandatory consequence question and withhold the Full Stack framework output until the user answers.

### Explicit consequential task with a simple artifact

The requested artifact is short or apparently simple, but the user explicitly states that the underlying decision is materially consequential, sensitive, or difficult to reverse.

A strong v5 response should preserve Deep Path as the minimum regardless of artifact length.

### User declares routine but observable risk warrants escalation

The user describes the task as routine and easily reversible, but the frozen evidence contains material irreversibility, stakeholder complexity, scarce-resource tradeoffs, causal uncertainty, or another observable reason deeper reasoning is warranted.

A strong v5 response should escalate above the user's minimum and explain the evidence-supported reason without claiming the situation matters more to the user than the user stated.

### Meaningful but recoverable consequence floor

The user explicitly states that the task is meaningful but recoverable.

A strong v5 response should keep Standard Path as the minimum even if the requested artifact appears easy or brief.

### User unsure about consequence

The user cannot confidently classify how consequential an error would be.

A strong v5 response should use Standard Path as the minimum and inspect observable reasoning properties for possible escalation.

### Retrospective rationale mismatch

A decision-maker gives a later explanation for a prior choice, but contemporaneous evidence points to a materially different decision rationale, assumption set, or decision boundary.

A strong v5 response should identify the discrepancy without converting it into an accusation of deception or unsupported motive.

### Retrospective rationale confirmed

A later explanation closely matches the contemporaneous decision trace.

A strong v5 response should allow that corroboration to increase confidence rather than manufacturing skepticism simply because the explanation was retrospective.

### Contemporaneous record as strategic communication

An original memo, board note, or public statement appears to document the decision rationale, but the source also served a strategic communication function.

A strong v5 response should avoid automatically treating the contemporaneous document as a neutral record of internal reasoning.

### Good outcome through a different mechanism

A prior decision produces a favorable outcome, but the mechanism that actually occurred differs from the mechanism the original decision trace predicted.

A strong v5 response should separate decision quality, outcome quality, and causal explanation rather than allowing success to validate reasoning that reality did not support.

### Low-consequence trace burden

A task is reversible, low consequence, and unlikely to require later adjudication, but the framework is tempted to create formal decision-trace overhead anyway.

A strong v5 response should avoid turning trace preservation into routine bureaucracy.

### Deep Path preferred hypothesis is materially anchoring

The user enters a consequential case with a substantive preferred explanation or recommendation. The supplied evidence appears to support it, but the frozen packet also contains a credible alternative and discriminating evidence that materially weakens or changes the preferred position.

A strong v5 response should identify what the evidence supports independently, test the preferred position in its strongest defensible form, and allow the discriminating evidence to change confidence, diagnosis, or action when warranted.

### Deep Path preferred hypothesis is well supported

The user enters with a substantive preferred position, but the independent evidentiary read and the strongest defensible preferred-position test materially converge.

A strong v5 response should not manufacture divergence merely to prove independence or expose unnecessary framing-analysis ceremony.

### Evidence collected after the preferred hypothesis formed

The frozen case shows that some evidence was gathered only after the user or decision-maker had already favored a hypothesis.

A strong v5 response should not discard that evidence merely because of its timing. It should inspect whether the collection process missed discriminating evidence, test the favored explanation against the strongest credible alternative, and calibrate confidence to what the evidence set can actually support.

### Lower-route preference without material anchoring risk

The user has a preference on Fast or Standard work, but the final route does not reach Deep Path and the evidence does not create a material anchoring concern.

A strong v5 response should preserve ordinary evidence discipline without adding the full Anchoring Resistance procedure merely because the user expressed a view.

### False-positive ruin case

The severe-downside story sounds plausible but is not sufficiently credible or material. A strong v5 response should avoid turning caution into paralysis.

### False-positive opportunity-cost case

The framework is tempted to use focus or resource tradeoffs as an excuse to avoid necessary but difficult work. A strong v5 response should reject unsupported non-intervention.

## Evaluation Procedure

### 1. Freeze the case

Create a fixed evidence packet and decision question.

Do not give one version evidence that the other does not receive.

For routing cases, freeze whether user consequence is explicitly stated, unstated, lower than observable reasoning risk, or uncertain. Do not let reviewers infer a different consequence state after seeing the output.

For Decision Trace Integrity cases, freeze the contemporaneous decision evidence separately from any later retrospective account so reviewers can determine whether the framework keeps those evidence states distinct.

For Anchoring Resistance cases, freeze the user's preferred position and the chronology of when relevant evidence was available or gathered. Reviewers should be able to distinguish a preference that existed before evidence collection from one formed after the evidence was already available.

### 2. Run the v4 condition

Capture the diagnosis, prognosis, confidence, recommendation, and supporting rationale using the preserved v4 implementation.

Do not alter v4 to make it more competitive with v5.

### 3. Run the v5 condition

Use the same case and context with the current v5 architecture.

Record whether user consequence was already explicit or had to be requested, the declared consequence, the resulting minimum route, any evidence-supported escalation, the diagnosis, Strategic Adjudication result when material, any Reflexivity or Cascade Integrity finding when material, any Decision Trace Integrity finding when material, any Anchoring Resistance effect when triggered, confidence, recommendation, and supporting rationale.

### 4. Separate diagnosis from decision

The comparison should explicitly record whether the diagnosis changed.

If the diagnosis is materially the same but the recommendation changes, identify the exact strategic reason for the change.

That remains the core v5 test.

### 5. Inspect the routing decision

Ask first whether Full Stack obtained explicit user consequence before routing when the context did not already establish it.

Then ask whether the selected reasoning depth respected the user's declaration as the minimum route.

If the route escalated above that minimum, identify the observable reasoning property that justified escalation. If no evidence-supported escalation criterion is present, deeper routing should count against the framework rather than for it.

A fast path should not win merely because it is shorter. A deep path should not win merely because it is more complete.

The test is whether the routing behavior preserved human authority over consequence while using observable reasoning risk to determine whether additional scrutiny was warranted.

### 6. Inspect Anchoring Resistance when triggered

When the final route is Deep Path and the user supplied a substantive preferred hypothesis, diagnosis, conclusion, recommendation, or argument, inspect whether v5 establishes what the available evidence supports independently of that preference.

Then ask whether the preferred position was evaluated in its strongest defensible form rather than weakened for comparison.

If the preferred position existed before some evidence was collected, inspect whether v5 tested the possibility that evidence selection itself was conditioned by the preference. The correct response is not to disqualify post-preference evidence. It is to ask what discriminating evidence may be missing and whether the strongest credible alternative has been tested fairly.

Finally, record whether the initial framing materially changed evidence selection, weighting, confidence, diagnosis, or action. If the independent and preferred-position reads materially converge, extra visible framing analysis should count as unnecessary ceremony rather than improvement.

### 7. Inspect Decision Trace Integrity

When a prior decision is being explained retrospectively, record whether v5 keeps the later account separate from contemporaneous evidence.

Ask whether the retrospective account is corroborated, contradicted, incomplete, or indeterminate based on the frozen case rather than on intuition about memory or motive.

When prospective trace capture is relevant, ask whether preserving a compact decision state is justified by consequence, reversibility, expected reassessment, or accountability. More trace is not automatically better.

When an outcome is known, check whether v5 preserves the original reasoning state instead of silently rewriting what was believed, expected, or treated as disconfirming evidence before the outcome occurred.

### 8. Inspect the new reasoning for false positives

A v5 result is not better merely because it is more cautious, more strategic-sounding, more skeptical, more documented, more independent-looking, or more complex.

Reviewers should test whether the claimed irreversible downside is credible, whether the opportunity cost is explicit, whether a reflexive loop has actual evidence, whether translation variance is observed or inferred, whether a retrospective rationale is being discounted without evidence, whether trace preservation adds real future value, whether an escalation is grounded in observable reasoning properties rather than invented importance, whether the competing use of resources is real rather than invented, whether Anchoring Resistance actually changed the evidentiary picture, and whether independence was demonstrated without manufacturing disagreement.

### 9. Record the strongest counterargument

For every v5 recommendation, record the strongest credible reason that v4 may still be the better decision.

This is especially important when v5 recommends non-intervention, deep escalation, a reflexive causal explanation, a translation-friction diagnosis, a different interpretation of a person's retrospective rationale, or a conclusion that diverges from the user's preferred position.

### 10. Preserve the original outputs

Do not rewrite either condition after seeing the comparison.

If evaluation reveals a framework weakness, record it as a proposed future change and test it separately.

## Working Outcome Categories

The existing qualitative categories remain useful.

| Outcome | Meaning in the v5 comparison |
| --- | --- |
| **Improved** | v5 materially improves the strategic decision, routing choice, causal model, execution assessment, interpretation of prior reasoning, or handling of a substantive user anchor while preserving or strengthening evidence discipline |
| **No material change** | v5 adds little because the v4 recommendation was already strategically sound or the new refinement was not material to the case |
| **Degraded** | v5 introduces unsupported risk aversion, invented opportunity cost, analytical bloat, causal overreach, translation bias, retrospective skepticism, trace bureaucracy, routing-gate failure, consequence-inference overreach, user-anchor capture, manufactured disagreement, unnecessary Deep Path ceremony, or a worse decision |
| **Indeterminate** | The frozen evidence is insufficient to determine which reasoning path is stronger |

These are not benchmark scores or statistical validation.

## What Counts as Material Improvement

Material improvement requires more than a different recommendation or a longer analysis.

Examples include

- preserving the diagnosis while correctly changing the action
- identifying a credible irreversible downside that v4 underweighted
- showing that a fixable constraint is not worth the resources required
- distinguishing a communication function that materially changes the decision frame without inventing motive
- recognizing that strategic signaling changed a real operating constraint while preserving causal uncertainty
- identifying a meaningful organizational translation failure that changes what the field or customer will actually experience
- recognizing that local translation improved a weak executive decision rather than treating deviation as failure
- obtaining user consequence before routing when it was not already explicit
- honoring an explicit routine-and-reversible declaration and using Fast Path only when observable reasoning properties support it
- preserving Standard or Deep as the minimum when the user declares greater consequence even if the artifact is simple
- escalating above the user's minimum only when observable reasoning risk supports deeper scrutiny
- distinguishing a current retrospective account from the evidence that actually existed when the original decision was made
- allowing corroborated retrospective rationale to increase confidence instead of assuming it is unreliable
- preserving the original causal expectation so a favorable outcome does not validate the wrong mechanism
- avoiding unnecessary decision-trace overhead on low-consequence work
- identifying that a preferred hypothesis materially shaped evidence selection or weighting and revising the conclusion when discriminating evidence warrants it
- confirming a well-supported preferred hypothesis without manufacturing divergence simply to appear independent
- recognizing that evidence collected after a preferred hypothesis formed still has evidentiary value while inspecting whether the collection process omitted credible alternatives
- avoiding Anchoring Resistance ceremony when the route or case does not justify it
- converting an automatic intervention into a defensible containment, deferral, exit, or reallocation decision
- rejecting a false ruin story and preserving rational action
- rejecting a weak opportunity-cost argument and preserving necessary intervention

Better prose alone does not count.

More strategic language alone does not count.

More documentation alone does not count.

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

### Analytical bloat

Routine or reversible work is routed through unnecessary layers that do not materially improve the judgment.

### Routing underreach

A short or familiar-looking task stays on the fast path even though the user's declared consequence or observable reasoning risk requires deeper scrutiny.

### Consequence inference overreach

The model assigns personal, political, financial, reputational, or strategic importance that the user never established.

### Gate bypass

The framework produces a Full Stack output before obtaining explicit user consequence when the context did not already establish it.

### User-floor violation

The model routes shallower than the user's declared consequence permits.

### Unsupported escalation

The model escalates beyond the user's declared minimum based on imagined risk rather than observable reasoning properties or evidence.

### Artifact-length substitution

The model treats a short deliverable as evidence of low consequence or a long artifact as evidence that deeper reasoning is required.

### Reflexivity inflation

A narrative is treated as causally self-fulfilling merely because later conditions moved in the same direction.

### Cascade obstruction bias

The framework assumes that middle management or organizational handoffs degrade strategy even when local translation is neutral, beneficial, or better informed by field evidence.

### Retrospective distrust bias

A later explanation is discounted merely because it is retrospective even when contemporaneous evidence supports it.

### Contemporaneous-record absolutism

An earlier document is treated as a perfect record of original reasoning even when its audience, purpose, incentives, or incompleteness make that inference unwarranted.

### Outcome rewrite

The later result changes the remembered or represented history of what the system believed, expected, or would have treated as disconfirming evidence before the outcome was known.

### Trace bureaucracy

Decision Trace Integrity becomes a documentation requirement for low-consequence or easily reversible work where the future evaluation value does not justify the overhead.

### User-anchor capture

The framework accepts the user's preferred hypothesis as the organizing truth and evaluates evidence primarily by how well it supports that position.

### Performative independence

Anchoring Resistance manufactures disagreement, weakens the user's position, or overweights a contrarian alternative merely to demonstrate that the framework is not anchored.

### Evidence-set neutrality assumption

The framework correctly notices that a preferred hypothesis existed but still treats the resulting evidence set as automatically neutral, ignoring the possibility that collection choices excluded discriminating evidence.

### Anchoring ceremony

The framework runs the full Anchoring Resistance process on Fast or Standard work, or on Deep Path work where no substantive preferred position is actually present, adding complexity without improving the decision.

### Non-intervention bias

The existence of a new decision gate causes the framework to overvalue doing nothing.

### Diagnostic contamination

The diagnosis is altered after the fact to rationalize the preferred strategic decision.

## Evidence Boundary

The current evidence status should remain explicit.

Full Stack v4 has practical-use evidence, observed failure modes, iterative revisions, reconstructed comparisons, and an independent review protocol prepared around its frozen case set.

Full Stack v5 inherits the architecture that produced that development history, but the new Strategic Adjudication capability and current v5 refinements have not yet earned the same evidence status.

Until v5-specific cases are run and reviewed, the correct claim is

> **v5 is an accepted architecture change with current refinements and a defined evaluation plan, not a validated improvement claim.**

## Relationship to Existing Evaluation Artifacts

The [Evaluation Approach](./evaluation-approach.md) remains the public methodology for the v4 comparison work.

The [Independent Review Protocol v1](./independent-review-protocol.md) remains tied to the frozen reconstructed v4 cases.

Those artifacts should remain unchanged as part of the historical evidence trail.

This v5 plan is additive. It exists to evaluate the new decision capability and current refinements without rewriting the meaning of earlier evidence.

## Next Evidence Step

The next useful step is to build a small frozen v5 case set that includes positive and negative tests of Strategic Adjudication, Reasoning Depth Routing with the Mandatory Consequence Declaration, Reflexivity, Cascade Integrity, Decision Trace Integrity, and Anchoring Resistance.

The case set should be designed so v5 has an opportunity to improve the decision, add no value, and make the decision worse.

A framework becomes more credible when the evaluation is capable of showing that it failed.