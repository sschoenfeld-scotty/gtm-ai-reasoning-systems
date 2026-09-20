# Evidence Entry 004

## External repository review batch 01

| Field | Value |
| --- | --- |
| Evidence type | External repository review batch |
| Review date | September 20, 2026 |
| Repositories reviewed | GTMify/aigtm, dominikj111/Engram, AdieLaine/multi-agent-reasoning, rajpriyanshu148/gtm-intelligence-agent |
| Review method | Each repository analyzed separately before cross-case synthesis |
| Canonical Full Stack change | None |
| GTM Diagnostic Framework change | None |
| Public evaluation implication | Three concrete external-evidence fixtures added |

## Why this entry exists

This batch tested whether external reasoning, decision-support, or GTM-adjacent repositories could produce evidence that materially bears on the current reasoning systems.

The objective was not to find support for Full Stack v5 or GTM Diagnostic Framework v9.

Each repository was reviewed against its own implementation and documentation first. A repository-only conclusion was frozen before framework comparison or cross-case synthesis.

That sequencing reduced cross-case contamination. It did not create independent reviewers or blind replication. One investigator performed the batch, and the repositories were selected because they appeared adjacent to the questions this portfolio studies.

## Evidence boundary

The four reviews were pinned to exact upstream commits.

| Repository | Reviewed commit | Bounded finding |
| --- | --- | --- |
| [GTMify/aigtm](https://github.com/GTMify/aigtm) | [216a26ae482a4dca502361695085ebc8bf27e1b6](https://github.com/GTMify/aigtm/commit/216a26ae482a4dca502361695085ebc8bf27e1b6) | Published forecast-category subtotals did not reconcile with the deals named in those categories. |
| [dominikj111/Engram](https://github.com/dominikj111/Engram) | [9084ad0e07cf57df08da63c262a450a49b4e8651](https://github.com/dominikj111/Engram/commit/9084ad0e07cf57df08da63c262a450a49b4e8651) | Delivered Phase 2 behavior and the stated raw-input privacy boundary require clarification. Runtime privacy implications remain partly unresolved. |
| [AdieLaine/multi-agent-reasoning](https://github.com/AdieLaine/multi-agent-reasoning) | [4fa5fae1e4ae0fc1d83d44e831e5d3cd5806bda0](https://github.com/AdieLaine/multi-agent-reasoning/commit/4fa5fae1e4ae0fc1d83d44e831e5d3cd5806bda0) | A reproduced Swarm routing mismatch misattributes a critique and delivers it to the wrong refinement relationship. |
| [rajpriyanshu148/gtm-intelligence-agent](https://github.com/rajpriyanshu148/gtm-intelligence-agent) | [eb0d0161810bbfb44ac31c32bcf112e29cb628b6](https://github.com/rajpriyanshu148/gtm-intelligence-agent/commit/eb0d0161810bbfb44ac31c32bcf112e29cb628b6) | Credential-free demo data can reach decision-facing reports without preserving its synthetic status. |

The detailed reproduction packages remain private. They preserve the execution record and source state. They also retain each frozen repository-only conclusion with its verification artifacts.

## Upstream action taken

The findings were adjudicated separately.

| Repository | Upstream action | Status at publication |
| --- | --- | --- |
| aigtm | [Pull request 17](https://github.com/GTMify/aigtm/pull/17) correcting the two reproduced category subtotals | Open |
| Engram | [Issue 3](https://github.com/dominikj111/Engram/issues/3) asking for clarification of current capability labeling and the raw-input privacy boundary | Open |
| multi-agent-reasoning | [Issue 7](https://github.com/AdieLaine/multi-agent-reasoning/issues/7) documenting the reproduced critique-routing mismatch | Open |
| gtm-intelligence-agent | [Issue 1](https://github.com/rajpriyanshu148/gtm-intelligence-agent/issues/1) proposing preservation of demo provenance and persistent simulation labeling | Open |

Submission is evidence that the review produced bounded findings worth returning upstream.

It is not evidence that any maintainer has accepted the finding, accepted the proposed scope, or validated the reasoning framework used in this portfolio.

## What materially changed in the evaluation work

Three cases produced concrete test fixtures for evaluation.

The aigtm case shows why aggregate reconciliation can be insufficient. A grand total can remain correct while the category allocation that drives the decision is wrong.

The multi-agent-reasoning case shows why the presence of critique is not enough. The evaluator must preserve who produced the critique and which response it was written about.

The gtm-intelligence-agent case shows why source status has to survive transformation. Synthetic or fallback evidence should not become indistinguishable from live evidence merely because it has been converted into a score or recommendation.

Those fixtures are published separately in [External Evidence Fixtures 01](../evaluation/external-evidence-fixtures-01.md).

Engram is not converted into an executable fixture yet. The correct test depends on the maintainer's intended privacy boundary and would benefit from independent Rust execution.

## Full Stack review

The current Full Stack v5 architecture already contains public-level controls capable of reasoning about these findings.

Evidence discipline can test what a number or source actually represents.

Operator Proof can inspect whether a downstream output follows from the implementation path.

Decision Trace Integrity and evidence re-entry can preserve status when prior outputs are reused.

No case established a missing reasoning stage.

The evaluation implication is therefore stronger test coverage, not framework expansion.

No canonical Full Stack modification is proposed.

## GTM v9 review

Two cases are commercially adjacent.

The aigtm finding concerns forecast evidence and category integrity.

The gtm-intelligence-agent finding concerns source status and the difference between prospecting signals and buyer-confirmed commercial truth.

Those transfers are inferential. Neither repository is a GTM v9 field test.

No GTM v9 field hypothesis is upgraded and no canonical GTM change is proposed.

## What this does not establish

This batch does not establish that Full Stack caused the findings.

It does not establish that the reviewed repositories are broadly unreliable.

It does not estimate how common these failure modes are.

It does not show that the proposed upstream changes improve model accuracy or commercial outcomes.

It does not validate Full Stack v5 or GTM Diagnostic Framework v9.

## Evidence maturity

The batch includes reproduced document arithmetic and isolated component execution. It also includes direct source tracing. Some interpretation boundaries remain unresolved.

Those evidence levels remain separate.

The strongest technical evidence comes from the reproduced aigtm reconciliation. The multi-agent critique-routing path was also reproduced with a fake client. The gtm-intelligence-agent no-key path was executed with network access blocked.

The Engram case remains partly source-traced because the Rust binary was not independently executed.

## Current disposition

Preserve this as Evidence Entry 004.

Carry three bounded fixtures into the v5 evaluation plan.

Keep the detailed private research package private.

Re-enter the evidence if an upstream maintainer responds, an issue or pull request changes materially, or new source evidence changes the interpretation.
