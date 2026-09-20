# External Evidence Fixtures 01

*Concrete evaluation checks derived from external repository reviews. These fixtures test existing evaluation discipline. They are not new Full Stack stages and do not validate Full Stack v5.*

## Status

This packet contains three active fixtures and one deferred case.

The fixtures were derived from external repositories reviewed on September 20, 2026. Each source case remains bounded to its reviewed commit and verification method.

A strong result means the evaluation procedure detects the specified integrity condition.

It does not mean the reasoning framework caused the original finding or that passing the fixture improves real-world outcomes.

## Fixture 1

**Decision-category reconciliation**

**Source case**

[GTMify/aigtm](https://github.com/GTMify/aigtm) at commit [216a26ae482a4dca502361695085ebc8bf27e1b6](https://github.com/GTMify/aigtm/commit/216a26ae482a4dca502361695085ebc8bf27e1b6)

**Failure mode**

The published example's grand total was correct, but two decision categories did not reconcile with the deals named inside them.

Upside named TerraWave at $75,000 and Bridgeport at $400,000. That membership totals $475,000, not the published $195,000.

At Risk / Pull named Greenleaf at $95,000 and Apex at $120,000. That membership totals $215,000, not the published $495,000.

**Evaluation assertion**

When a decision depends on partitions, categories, cohorts, or buckets, reconciliation should occur at the decision-relevant partition level rather than only at the grand total.

**Pass condition**

The evaluator verifies that each category's members reconcile to that category before accepting a downstream diagnosis or recommendation.

**Failure condition**

The evaluator treats a correct aggregate total as sufficient even though the category allocation is internally inconsistent.

**Boundary**

This fixture does not determine whether the category definitions themselves are commercially correct.

It tests arithmetic and membership integrity only.

## Fixture 2

**Critique author and target integrity**

**Source case**

[AdieLaine/multi-agent-reasoning](https://github.com/AdieLaine/multi-agent-reasoning) at commit [4fa5fae1e4ae0fc1d83d44e831e5d3cd5806bda0](https://github.com/AdieLaine/multi-agent-reasoning/commit/4fa5fae1e4ae0fc1d83d44e831e5d3cd5806bda0)

**Failure mode**

The Swarm flow stored critique text under the critic's name. The refinement step then read that entry while labeling it as another agent's critique of the current response.

A fake-client reproduction with distinct markers showed the mismatch without requiring a live model call.

**Evaluation assertion**

A critique stage should preserve both the critique author and the response that critique was written about through the receiving prompt.

**Pass condition**

The evaluator can trace each critique from author to intended target and confirm that the receiving refinement step uses the critique written about that response.

**Failure condition**

Critique content reaches a refinement step with false authorship, the wrong target relationship, or an ambiguous mapping that cannot be independently reconstructed.

**Boundary**

This fixture tests routing integrity.

It does not establish that correctly routed critique improves answer quality.

## Fixture 3

**Source-mode continuity**

**Source case**

[rajpriyanshu148/gtm-intelligence-agent](https://github.com/rajpriyanshu148/gtm-intelligence-agent) at commit [eb0d0161810bbfb44ac31c32bcf112e29cb628b6](https://github.com/rajpriyanshu148/gtm-intelligence-agent/commit/eb0d0161810bbfb44ac31c32bcf112e29cb628b6)

**Failure mode**

With provider credentials absent and network access blocked, the application produced synthetic source content and generated a company-specific buying score with a confidence value. It also produced a purchasing window.

The downstream report named Bright Data sources without carrying an explicit demo or fallback provenance field.

**Evaluation assertion**

When evidence changes form, its source mode should remain inspectable if that status matters to the downstream judgment.

Relevant source modes can include live, synthetic, fallback, reconstructed, or mixed.

**Pass condition**

The decision-facing output preserves enough provenance to distinguish the source mode that produced the underlying evidence.

**Failure condition**

Synthetic or fallback evidence becomes indistinguishable from live evidence after transformation into a score, recommendation, summary, or other decision artifact.

**Boundary**

This fixture does not establish that synthetic data is inappropriate for demos.

It tests whether the demo status survives into the output.

## Deferred case

**Capability and privacy boundary**

**Source case**

[dominikj111/Engram](https://github.com/dominikj111/Engram) at commit [9084ad0e07cf57df08da63c262a450a49b4e8651](https://github.com/dominikj111/Engram/commit/9084ad0e07cf57df08da63c262a450a49b4e8651)

The review found a stale Phase 1 README status while Phase 2 behavior is present in the source and roadmap.

It also found that the current CLI places raw trimmed input into line-editor history before engine execution, while the project describes raw text as discarded at the tokenizer boundary.

The correct fixture depends on the intended privacy boundary.

If the guarantee concerns graph persistence only, the issue may be primarily documentation scope.

If the guarantee covers all application memory after tokenization, the implementation question is different.

The case therefore remains deferred pending maintainer clarification and independent Rust execution.

## How these fixtures should be used

These checks belong inside evaluation, not inside the canonical reasoning architecture.

They can be applied to future cases when the underlying failure mode is relevant.

They should not be forced onto unrelated cases merely because an external example exists.

A future fixture should be added only when it creates a distinct falsifiable check that existing evaluation material does not already express clearly.

## Relationship to the v5 evaluation plan

The [Full Stack v5 Evaluation Plan](./full-stack-v5-evaluation-plan.md) incorporates these fixtures as bounded evaluation assertions.

The source cases are summarized in [Evidence Entry 004](../evidence/2026-09-20-external-repository-review-batch-01.md).

No canonical framework modification follows from this packet.
