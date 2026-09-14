# Evolution of the Reasoning System

*The design decisions that moved Full Stack from prompt-level improvement toward an explicit reasoning architecture and strategic decision gate*

**Status**  
Work in progress. This history includes only changes supported by the currently available source documents. It does not reconstruct undocumented intermediate versions.

## Why This History Matters

The point of version history is not to show that a prompt was edited many times.

It is to show when a recurring reasoning failure produced a meaningful change in the architecture.

The development pattern has been

**Observed failure → reasoning challenge → reusable lesson → architectural change → later retest**

## Design Evolution

| Stage | Reasoning problem | Architectural response | Why it mattered |
| --- | --- | --- | --- |
| **Initial problem** | AI could produce fluent output before the diagnosis deserved confidence | Introduce deliberate reasoning friction before writing | Shifted the objective from faster output to more inspectable judgment |
| **v3** | Surface agreement and first-order explanations were too easy to accept | Add hidden-assumption analysis, a human-systems view, and early consequence modeling | Moved the system beyond response generation toward diagnosis |
| **v4** | The framework needed clearer evidence discipline and stronger self-challenge | Make evidence separation, competing explanations, prognosis, pressure testing, confidence, and revision more explicit | Turned a collection of useful reasoning moves into a more coherent architecture |
| **v4 refinement** | A governing constraint could explain what blocked an outcome without explaining why the same condition kept recurring | Add optional system-dynamics reasoning, stakeholder perspective triangulation, and an experienced-operator delta inside pressure testing | Extended diagnosis from a static blocker toward recurring system behavior while preserving evidence and attribution discipline |
| **v4 refinement** | The written sequence did not make it explicit enough that material real-world responses and outcomes should be allowed to reopen the diagnosis | Make external evidence recursively re-enter at Source Truth, reinforce outcome-attribution discipline, and distinguish compliance from commitment | Turned an implicitly recursive system into an explicitly closed-loop reasoning process without adding another architectural layer |
| **v5** | A diagnosis could be correct and the resulting intervention could still be strategically wrong | Add Communication Function when material and Strategic Adjudication between prognosis and intervention | Separated diagnostic correctness from whether action is survivable and worth scarce resources |
| **v5 refinement** | The framework could still over-process simple work, miss cases where narrative changes operating reality, or treat organizational layers as static stakeholder states rather than translation channels | Add Reasoning Depth Routing, Reflexivity inside System Dynamics, and Cascade Integrity inside Operator Proof | Made existing v5 functions more deterministic without changing the governing reasoning spine |
| **v5 refinement** | A later explanation of a prior decision could be mistaken for evidence of the reasoning that actually produced the choice | Add Decision Trace Integrity across evidence discipline, Human Pattern 1, recursive evidence re-entry, and consequence-based trace preservation | Separated retrospective rationale from contemporaneous decision evidence without turning cognitive-bias labels into new peer lenses |
| **Current evaluation direction** | Existing v4 evidence does not validate the new v5 strategic-decision capability or later v5 refinements | Expand the v5-specific evaluation plan while preserving v4 evidence as v4 evidence | Keeps version claims and evidence claims aligned |
| **Separate research direction** | Behavioral observations can still become unsupported stories about motive | Explore longitudinal behavioral inference with attribution discipline | Extends evidence discipline across time without treating motive as fact |

## What Materially Changed in v4

Several v4 changes were substantive rather than cosmetic.

### Evidence became a first-class constraint

The framework became more explicit about keeping what is known separate from what is inferred.

This matters because fluent language can otherwise make uncertain reasoning appear settled.

### Competing explanations became part of the architecture

The system became more deliberate about keeping credible alternatives open before accepting a diagnosis.

This reduced the risk that the first plausible explanation would become the default story.

### Prognosis became explicit

The framework separated diagnosis of the current state from the likely consequences of leaving that condition unchanged or intervening against the wrong issue.

That created a clearer bridge between diagnosis and recommendation.

### The first answer became something to challenge

The architecture moved beyond polishing a plausible response and toward deliberately testing whether the reasoning could survive credible pushback.

### Confidence and framework revision became more inspectable

v4 distinguished confidence in the reasoning from confidence created by polished output.

It also added more explicit discipline for deciding whether a lesson belongs only to one case or should influence the framework itself.

## Later v4 Refinements

Later reviews exposed narrower gaps inside the existing v4 architecture. These changes deepened existing reasoning functions without changing the framework's purpose enough to justify a new major version.

### System dynamics became an optional extension of causal diagnosis

Causal diagnosis could identify the governing constraint but still stop too early when the real question was why that condition repeatedly regenerated.

The framework learned to distinguish between a condition that blocks an outcome and a feedback structure that may keep recreating that condition.

The refinement remains conditional. A single example does not justify a system-level claim.

### Perspective triangulation strengthened competing explanations

For multi-stakeholder problems, the framework can compare how the same condition appears from different operating positions.

The purpose is not to invent personas or motives. It is to expose differences in evidence, incentives, constraints, and consequences that may generate competing explanations.

### Operator proof gained an experienced-operator delta

Pressure testing began asking whether an experienced operator would notice practical evidence, ownership, measurability, handoffs, incentives, or execution constraints that a more abstract analysis might miss.

Experience is not treated as proof. The distinction matters only when the reasoning can show what is different and what evidence supports it.

### Recursive evidence re-entry made the system explicitly closed loop

A later comparative review largely validated the existing Full Stack architecture but exposed an implementation ambiguity.

The system already had evidence revision, competing explanations, operator proof, confidence calibration, and iterative learning. What the written sequence did not make explicit enough was what should happen after an output or intervention encountered reality.

The refinement made the intended behavior deterministic.

When a material external response or outcome appears, it re-enters at Source Truth and Evidence Discipline. Only the downstream reasoning materially affected by the new evidence is reopened.

The earlier diagnosis is neither protected nor automatically discarded.

A positive result can strengthen confidence without proving that the intervention alone caused the outcome. A negative result can weaken confidence without proving that the diagnosis was wrong.

> **Reality must retain the right to change the model.**

### Compliance is not commitment

The False Equivalence logic was sharpened with a distinction that generalizes across sales, management, organizational change, and AI adoption.

Visible compliance can create the appearance of progress without proving ownership, judgment, internalization, or durable behavior change.

This remained a v4 refinement rather than a new architectural layer.

## Why v5 Crossed the Version Threshold

The v5 change addresses a different class of failure.

Full Stack v4 could correctly identify what was true, what condition governed an outcome, what trajectory followed, and what intervention was most likely to change that trajectory.

The remaining assumption was subtle.

Once the governing constraint was diagnosed, the architecture still tended to proceed toward fixing it.

That is not always the right executive decision.

A diagnosed constraint may be strategically unimportant relative to a better use of scarce resources. An apparently attractive intervention may expose the business to credible irreversible downside. A public statement may be misread as a literal operating directive when its function is broader or different.

The important v5 distinction became

> **A correctly diagnosed problem does not automatically deserve intervention.**

That changed the reasoning path rather than merely sharpening an existing step.

## The v5 Architecture Change

Full Stack v5 preserves the diagnostic architecture of v4 and adds two connected changes.

### Communication Function when material

Before diagnosing an apparent operating claim, the system can ask whether the communication may serve more than one function and whether that distinction would materially change the diagnosis.

The purpose is to prevent category error, not to infer hidden motive.

Unverified intent remains a hypothesis. A communication can serve multiple audiences. Strategic signaling does not erase operational consequences.

### Strategic Adjudication between prognosis and intervention

This is the major architectural addition.

Strategic Adjudication asks whether acting on the diagnosis is strategically warranted before Full Stack commits to intervention.

It contains two connected tests.

**Ruin and Irreversibility** asks whether expected upside is being purchased with credible material downside that is difficult or impossible to reverse.

**Strategic Worth** asks whether removing the governing constraint creates enough strategic value to justify the scarce resources and opportunity cost required.

The result may still be intervention. It may also be deliberate non-intervention, containment, deferral, simplification, work-around, exit, or reallocation.

The important change is that v5 can preserve the diagnosis while changing the decision.

## Current v5 Refinements

Later review exposed narrower gaps inside v5. These changes are meaningful, but they do not create a new major architecture or a new numbered minor release.

### Reasoning Depth Routing

The framework was designed to use conditional lenses, but the execution sequence still risked making simple work inherit too much analytical weight.

The refinement adds an explicit entry-routing decision based on decision consequence, reversibility, ambiguity, stakeholder complexity, and strategic tradeoff rather than output length.

Low-stakes, reversible work can remain on a fast path. More ambiguous work uses the standard v5 execution path. High-stakes or difficult-to-reverse work can escalate to the deeper Operating Manual.

The governing principle is

> **Reasoning depth should be proportional to decision consequence, not output length.**

A short comment can still deserve deep reasoning. A long artifact can still be low risk.

### Reflexivity became explicit inside System Dynamics

Communication Function already distinguished what a statement may be doing. System Dynamics already looked for reinforcing feedback loops.

The missing connection was reflexivity.

A strategic signal can alter capital availability, talent flows, customer confidence, partner or competitor behavior, employee commitment, market expectations, or resource allocation. Those changes can then alter the feasibility of the original claim.

The refinement makes that causal loop inspectable without treating narrative influence as automatic proof of causality.

### Cascade Integrity became explicit inside Operator Proof

Perspective Triangulation compared stakeholder views. Operator Proof already considered handoffs and incentives.

The missing question was how strategic intent changes as it travels through the organization.

Cascade Integrity examines translation across executive intent, functional interpretation, management incentives, process design, frontline behavior, and customer experience.

The guardrail matters. Middle management is not assumed to be the source of distortion. Local translation can weaken, delay, redirect, improve, or correctly adapt an executive decision in light of field evidence.

The relevant test is translation variance, not automatic obstruction.

### Decision Trace Integrity strengthened evidence and revision

A later human-reasoning review exposed a different epistemic risk.

A person can give a sincere, coherent explanation of a prior choice without that explanation necessarily being a reliable record of the reasoning that produced the choice at the time.

The framework therefore needed to distinguish **retrospective rationale** from **contemporaneous decision evidence**.

Decision Trace Integrity treats a later explanation as evidence of the person's current account. It does not automatically promote that account into verified evidence of original causation.

When the original decision matters, Full Stack can compare the later account with contemporaneous evidence such as the alternatives available, information known at the time, stated assumptions, observable behavior, forecasts, communications, and conditions that were expected to change the decision.

When a current decision is consequential enough to justify it, the framework preserves a compact decision trace so later evaluation does not depend only on memory after the outcome is known.

The refinement also strengthens Recursive Evidence Re-entry.

Reality should be allowed to change the diagnosis, confidence, prognosis, or decision. It should not silently rewrite what the system believed before the new evidence arrived.

> **Reality should be able to change the model without rewriting what the model believed before reality arrived.**

The guardrail is equally important.

Decision Trace Integrity does not assume retrospective explanation is false. It does not assume contemporaneous documentation is complete or neutral. Communication Function still applies to records that may themselves have been written for an audience. The framework compares evidence rather than automatically privileging memory or documentation.

### Why these changes remain v5

These refinements do not alter Full Stack's governing purpose or insert another peer layer into the reasoning spine.

Reasoning Depth Routing sits inside Pre-diagnosis. Reflexivity sits inside System Dynamics. Cascade Integrity sits inside Operator Proof. Decision Trace Integrity operates across Evidence Discipline, Human Pattern 1, Recursive Evidence Re-entry, and consequence-based routing for prospective trace preservation.

That makes the existing architecture more deterministic without changing the reason v5 exists.

The version decision is therefore deliberate.

These are **Full Stack v5 refinements**, not v5.1 and not v6.

## What v5 Did Not Change

The new version does not replace the Logic Lens concept or the core Full Stack thesis.

The following principles remain intact.

- Better decisions come from better diagnosis.
- Evidence and interpretation remain separate.
- Competing explanations remain necessary when material.
- Motive and intent remain hypotheses unless supported.
- Causal diagnosis remains distinct from chronology.
- System Dynamics remains conditional.
- Prognosis remains probabilistic.
- Operator Proof remains grounded in operating reality.
- Recursive Evidence Re-entry remains active.
- Outcomes remain evidence about a diagnosis rather than automatic proof of causality.
- Retrospective explanation remains evidence rather than automatic proof of original reasoning.
- Human judgment retains responsibility for the conclusion.

The GTM Diagnostic Framework v8 is not modified by this change.

The Behavioral Inference Engine remains a separate work-in-progress research direction.

## Rejected Alternatives

The v5 design review rejected several ways of adding the new reasoning.

Three independent mandatory lenses were rejected because the architecture should not become a heavier checklist.

Strategic Intent inside the Evidence Ladder was rejected because epistemic classification and communication function answer different questions.

Opportunity Cost inside Causal Diagnosis was rejected because diagnosis should identify what governs the outcome while Strategic Worth decides whether changing that condition deserves resources.

A non-zero severe-risk probability as an automatic veto was rejected because consequential decisions almost always contain some theoretical severe-risk path. The relevant standard is credible and material irreversible downside.

Importing the separate Five Lens Decision Review architecture was rejected. Full Stack v5 does not adopt its independent-lens or Chairman structure.

The later refinement review also rejected adding Reflexivity, Cascade Integrity, and Fast-Path Routing as three new peer stages. Doing so would have increased checklist weight without changing the underlying architecture. Each belongs inside the existing function it sharpens.

The Decision Trace review rejected adding a dedicated **Choice Blindness** lens or a catalog of cognitive biases. The psychological observation exposed the failure mode, but the reusable architecture problem is broader. Retrospective rationale should be treated according to its evidence status, and consequential decisions should preserve enough contemporaneous state to make later comparison possible.

## Evidence and Evaluation Boundary

Existing Full Stack v4 evidence remains evidence about v4.

It must not be silently relabeled as v5 validation.

The broader development history still matters. Repeated practical use, observed reasoning failures, framework revision, later retesting, and reconstructed comparisons show that the system has been exercised and changed in response to evidence.

But the new v5 Strategic Adjudication capability and the current v5 refinements require their own evaluation.

The [Full Stack v5 Evaluation Plan](../evaluation/full-stack-v5-evaluation-plan.md) is designed to test cases where

- the diagnosis is correct but intervention is strategically inferior to non-intervention
- an optimization has attractive expected upside but credible irreversible downside
- a constraint can be fixed but another use of scarce resources has greater strategic value
- a communication is misdiagnosed because its function is misunderstood
- a strategic signal changes the resources or behavior that determine whether the claim can become true
- an apparent reflexive loop is actually coincidence or post hoc storytelling
- strategic intent mutates materially as it passes through organizational handoffs
- local translation improves rather than degrades an executive decision
- a low-stakes task is over-processed by the full architecture
- a seemingly simple task is routed too shallowly even though the decision consequence is material
- a retrospective explanation conflicts with contemporaneous decision evidence
- a retrospective explanation is well supported and should not trigger manufactured skepticism
- a contemporaneous record was itself strategic communication rather than a neutral record of decision reasoning
- a good outcome occurred through a mechanism different from the one originally expected
- decision-trace requirements create unnecessary bureaucracy on low-consequence work
- ruin reasoning creates a false positive and causes unnecessary paralysis
- opportunity-cost reasoning becomes an excuse to avoid necessary work

No v5 performance result is claimed until those tests are actually run and reviewed.

## Two-Part Implementation

Full Stack continues to operate through two private components.

| Component | Role |
| --- | --- |
| **Operating Manual** | Deeper reasoning for complex or high-stakes work |
| **Execution Prompt** | Faster application of the same underlying discipline, with entry routing that can remain fast, use the standard path, or escalate to deeper reasoning |

The two components implement the same v5 architecture at different levels of depth.

## Current State

Full Stack v5 is the active canonical version for new work.

Full Stack v4 remains preserved as historical canonical source material and as a public architecture artifact.

The v5 Operating Manual and Execution Prompt are complete and aligned with the current v5 architecture, including Reasoning Depth Routing, Reflexivity, Cascade Integrity, and Decision Trace Integrity.

The next Full Stack work is evaluation of the v5 decision capability and current refinements rather than version expansion.

## Version Discipline

Full Stack v5 supersedes v4 for new work.

v4 and v3 remain historical source material.

Minor wording, voice, example, execution-routing, or nested reasoning refinements should update v5 rather than create a new numbered release.

Reasoning Depth Routing, Reflexivity, Cascade Integrity, and Decision Trace Integrity are current v5 refinements. They do not create v5.1 or v6.

A future major version should require another meaningful change in purpose, architecture, or reasoning capability.

## Related Public Documents

- [Full Stack v5 Public Architecture](./full-stack-v5-public-architecture.md)
- [Full Stack v4 Public Architecture](./full-stack-v4-public-architecture.md)
- [Building Friction Into AI](../docs/building-friction-into-ai.md)
- [What I Mean by a Logic Lens](../docs/what-is-a-logic-lens.md)
- [Full Stack v5 Evaluation Plan](../evaluation/full-stack-v5-evaluation-plan.md)
