# Evidence Center: A Reference Architecture for Evidence Preservation and Provenance

*A domain-neutral reference architecture for preserving reasoning
outcomes without interpreting their internal semantics*

> Work in progress \| September 2026\
> Reference architecture, not a validated implementation or canonical
> Full Stack component

## Status and Source Boundary

The Evidence Center is an independent research direction for preserving
evidence and reasoning outcomes across systems, models, workflows, and
human review.

This document defines architectural concepts and boundaries. It does not
prescribe an implementation schema, API contract, storage engine,
serialization format, event platform, deployment topology, user
interface, or replacement for domain-specific reasoning.

The schemas in this document are **conceptual schemas**. They make
architectural distinctions explicit. They are not database tables,
production payload definitions, or component specifications.

Full Stack v5 appears only as a mapping case. The Evidence Center is not
derived from Full Stack v5, does not modify it, and does not require
knowledge of its internal reasoning semantics.

## The Problem

Reasoning systems can preserve conclusions while losing the state that
produced them.

A later artifact may overwrite an earlier one. A copied artifact may
lose its source identity. A model-generated revision may become
indistinguishable from a human revision. A relationship between two
outcomes may be reconstructed from prose or naming conventions rather
than explicitly preserved.

This creates a gap between having evidence and being able to answer
basic provenance questions:

-   What exactly existed at a particular point in time?
-   Was that exact content later changed?
-   Who or what produced or captured it?
-   What external system or identifier referred to it?
-   Which later state followed it?
-   Who asserted that two preserved states were related?
-   Can a later interpretation be added without rewriting the earlier
    record?

The Evidence Center addresses that gap.

> **Its purpose is to preserve evidence states, identities, actor
> provenance, and externally declared relationships without deciding
> what the evidence means.**

## Architectural Position

The Evidence Center sits at the provenance boundary between
evidence-producing environments and evidence-consuming systems.

``` mermaid
flowchart LR
    P[Human / LLM / System] --> C[Capture]
    C --> E[Evidence Center]
    E --> R[Reasoning Systems]
    E --> V[Review / Reconstruction]
    R -->|new outcomes or relationships| E
```

Evidence-producing systems remain responsible for producing content.

Reasoning systems remain responsible for interpretation, diagnosis,
confidence, adjudication, and action.

The Evidence Center is responsible for preserving what was produced, its
identity and provenance, and externally asserted connections between
preserved outcomes.

This boundary is intentional.

A reasoning artifact may internally contain observations, hypotheses,
alternatives, diagnoses, decisions, recommendations, or any other
domain-specific structure. The Evidence Center does not need to
decompose or understand that structure in order to preserve the
artifact.

## Core Design Principles

### 1. Preserve before interpreting

Capture should not require the Evidence Center to understand a domain's
reasoning model.

An artifact can be preserved as an opaque payload even when its internal
semantics are unknown to the provenance layer.

### 2. Preserved payloads are immutable

Once a payload is captured as a preserved state, its exact content is
not edited in place.

If the content changes, the changed content becomes another package.

### 3. Package identity is not content identity

A captured package and its exact payload are different identities.

The same exact payload may be captured more than once in different
contexts or at different times. Those captures may have different
package identities while sharing the same content digest.

### 4. External identity remains externally owned

GitHub IDs, decision IDs, requirement IDs, repository paths, case IDs,
message IDs, or identifiers from another reasoning system remain
identities of those external systems.

The Evidence Center preserves and resolves those references. It does not
redefine their semantics.

### 5. Actor provenance is captured, not inferred

Where available, the producer or capturing actor should be recorded when
the package is created.

A later reviewer should not need to inspect writing style or ask another
model to guess whether a state was produced by a human, LLM, or system.

Unknown actor provenance remains unknown.

### 6. Relationships exist outside packages

A relationship does not belong to either connected package.

It is an independently attributable assertion connecting references or
preserved states.

This allows relationships to be added later without modifying either
original payload.

### 7. Relationship semantics remain externally owned

The Evidence Center does not require a universal vocabulary such as
`SUPPORTS`, `CHALLENGES`, `REVISES`, or `IMPLEMENTS`.

A domain system may use those terms through externally supplied
qualifiers.

The Evidence Center preserves, indexes, and returns those qualifiers
without deciding what they mean.

### 8. History is additive

New evidence, correction, disagreement, reinterpretation, or
adjudication should be represented through additional packages and
relationships rather than silent rewriting of prior states.

## Minimal Conceptual Model

The minimum reference architecture contains two primary records and
several identity/provenance concepts carried by them.

``` text
Outcome Package
├── Package Identity
├── Content Identity
├── Actor Provenance
├── Reference ID Set
├── Capture Metadata
└── Immutable Payload

Relationship
├── Relationship Identity
├── Endpoints
├── Direction
├── Actor Provenance
├── Reference ID Set
└── Qualifier Field Set
```

This is a conceptual model, not a required storage layout.

An implementation may represent these concepts in a file, library,
database, graph store, embedded module, or independent service.

## Outcome Package

An Outcome Package preserves one captured state without requiring the
Evidence Center to interpret its payload.

A conceptual representation is:

``` yaml
package:
  package_id: "EP-<capture-oriented-id>"
  captured_at: "<timestamp>"

  content_id:
    algorithm: "sha256"
    digest: "<digest>"

  actor:
    type: "human | llm | system | unknown"
    ref: "<external-or-local-actor-reference>"

  reference_ids:
    - namespace: "<external-system>"
      type: "<externally-defined-type>"
      value: "<external-id>"

  capture:
    source: "<source-reference>"
    method: "<capture-method>"

  payload: "<exact preserved content>"
```

The fields illustrate concepts that should remain distinguishable. They
do not prescribe field names or serialization.

### Package Identity

`package_id` identifies the capture event or preserved package.

Two packages may contain identical payload bytes while representing
different captures.

### Content Identity

`content_id` identifies the exact preserved content.

A cryptographic digest such as SHA-256 can answer a narrow but important
question:

> Is this exact payload the same content that was previously preserved?

The digest does not establish truth, authority, authorship, or
correctness.

### Actor Provenance

The package records who or what produced or supplied the captured state
when that information is available.

At minimum, a system may distinguish broad actor types such as:

``` text
human
llm
system
unknown
```

More specific actor identities remain externally defined.

For example:

``` text
PKG-A [Human]
   ↓
PKG-B [LLM]
   ↓
PKG-C [Human]
```

This sequence can be reconstructed from package provenance without
interpreting any of the three payloads.

Actor provenance records an attributable source claim or observed
capture fact. It should not be silently inferred when unavailable.

### Reference ID Set

A package may have multiple external identities.

For example, one preserved artifact could be known as:

``` text
github:pull_request:13
github:path:evidence/2026-09-14-open-ended-collaboration.md
full-stack:evidence-entry:001
```

Those identifiers may refer to the same preserved package without
becoming Evidence Center-native semantics.

A Reference ID Set allows external systems to continue using their own
identifiers while the Evidence Center provides a common resolution
boundary.

### Immutable Payload

The payload is the content that was actually preserved.

The default principle is:

> **Preserve the submitted outcome without parsing, summarizing,
> restructuring, or semantically rewriting it.**

A payload may contain rich internal structure. That structure remains
the responsibility of the producing system.

If a transformation such as summarization, translation, redaction,
extraction, or normalization produces materially different content, the
result should be preserved as another package rather than replacing the
original payload.

## Relationship

A Relationship is a first-class record outside the connected packages.

Conceptually:

``` yaml
relationship:
  relationship_id: "REL-<id>"
  created_at: "<timestamp>"

  actor:
    type: "human | llm | system | unknown"
    ref: "<actor-reference>"

  endpoints:
    - ref:
        namespace: "<external-system>"
        value: "<id-a>"
    - ref:
        namespace: "<external-system>"
        value: "<id-b>"

  direction: "directed | undirected | bidirectional"

  reference_ids:
    - namespace: "<external-system>"
      value: "<relationship-reference>"

  qualifier:
    namespace: "<external-domain>"
    fields:
      type: "<externally-defined-value>"
      stage: "<externally-defined-value>"
      scope: "<externally-defined-value>"
```

Again, this is a conceptual schema.

### Why Relationship is outside Package

Suppose Package A and Package B already exist.

A later reasoning system may determine that B challenges A. Another
system may describe the same connection differently. A human reviewer
may later add another relationship.

None of those assertions requires either original package to be
modified.

``` text
Package A              Package B
    \                      /
     \                    /
      └── Relationship ──┘
              │
          Qualifier
```

The relationship therefore has its own identity, provenance, time, and
externally supplied semantics.

### Direction is structural; meaning is external

Direction supports traversal.

For example, an implementation may need to move from A to B, from B to
A, or across an undirected connection.

Direction does not by itself define semantic roles.

The meaning of the connection belongs to the external qualifier.

### Qualifier

A qualifier is an externally defined, queryable field set.

For example, Full Stack could choose to assert:

``` yaml
qualifier:
  namespace: "full-stack"
  fields:
    type: "CHALLENGES"
    stage: "diagnosis"
    scope: "causal"
```

`CHALLENGES`, `diagnosis`, and `causal` are not Evidence Center
vocabulary.

The Evidence Center only needs to preserve that an external actor or
system asserted those fields.

This allows domain semantics to remain at the edge while still
supporting filtering, grouping, traversal, and reconstruction.

## Core Invariants

An implementation consistent with this reference architecture should
preserve the following invariants.

**Immutable state.** A preserved payload does not change in place.

**New content, new package.** A materially changed payload is captured
separately.

**Separate identities.** Package identity, content identity, external
identity, and actor identity are not interchangeable.

**External ownership.** External identifiers and qualifier semantics
remain owned by their originating systems.

**Explicit relationships.** Material connections are recorded rather
than inferred from filenames, folders, timestamps, or prose.

**Attributable assertions.** A relationship records who or what asserted
it when that information is available.

**No semantic invention.** The Evidence Center does not invent missing
relationships or domain meanings.

**No provenance completion by guess.** Unknown source, actor, timestamp,
or reference data remains unknown unless a separately attributable
process derives it.

**Additive history.** Later evidence can alter current interpretation
without silently rewriting earlier preserved states.

## Generic Operations

The reference architecture implies several generic operations without
prescribing their implementation.

### Capture

Preserve a payload together with package identity, content identity,
actor provenance, external references, and capture metadata.

### Resolve

Given a package ID, content identity, or external reference, locate the
corresponding preserved package or packages.

### Relate

Record an externally asserted relationship between resolvable endpoints.

### Filter

Select packages or relationships using provenance metadata, references,
actor information, or qualifier fields.

### Trace

Traverse explicit relationships without requiring the Evidence Center to
interpret their domain meaning.

A domain consumer may interpret a trace as a decision chain, requirement
trace, evidence chain, authorization chain, or another domain-specific
view.

### Matrix

Project packages and relationships across selected dimensions.

The dimensions may come from reference IDs, actor provenance,
timestamps, or externally supplied qualifier fields.

The Evidence Center does not need to understand those dimensions
semantically in order to group or expose them.

## Mapping Case: Full Stack v5 and PR #13

Full Stack v5 provides a useful boundary test because it already has its
own reasoning semantics.

The question is not whether Evidence Center can reproduce Full Stack's
reasoning model.

The question is:

> **Can a domain-neutral provenance architecture preserve a Full Stack
> evidence artifact and its later evolution without understanding or
> rewriting Full Stack semantics?**

PR #13, **"Add contemporaneous evidence entry for open-ended
collaboration,"** provides a concrete case.

The evidence entry deliberately preserves a pre-outcome reasoning state
before the external contribution is available for review. Internally,
the Markdown distinguishes Observation, Inference, Working Hypothesis,
Competing Explanations, strengthening and weakening evidence, and
Current Decision.

Evidence Center does not need to decompose those sections.

The entire Evidence Entry 001 can be preserved as one Outcome Package:

``` text
PR #13 / Evidence Entry 001
            │
            ▼
┌──────────────────────────────┐
│ Outcome Package              │
│                              │
│ Package ID                   │
│ Captured At                  │
│ Actor Provenance             │
│ Content SHA                  │
│ Reference ID Set             │
│ Original Markdown Payload    │
└──────────────────────────────┘
```

A conceptual mapping is:

  -----------------------------------------------------------------------
  PR #13 element                      Evidence Center concept
  ----------------------------------- -----------------------------------
  Entire Evidence Entry 001           Outcome Package

  Exact Markdown                      Immutable Payload

  Exact-content fingerprint           Content Identity

  Capture at the original point in    Package / capture identity
  time                                

  Producer identity                   Actor Provenance

  GitHub PR #13                       External Reference ID

  Repository path                     External Reference ID

  Evidence Entry 001                  External Reference ID

  Later reasoning artifact            New Outcome Package

  Full Stack's interpretation of how  External Relationship + Qualifier
  the states relate                   
  -----------------------------------------------------------------------

This mapping is intentionally asymmetric.

Full Stack owns the meaning of `Observation`, `Inference`,
`Working Hypothesis`, `Diagnosis`, `Adjudication`, or any other
reasoning category.

Evidence Center only preserves the artifact containing those semantics
and the provenance needed to reconstruct its history.

If later evidence changes Scott's interpretation, the earlier package
remains unchanged:

``` text
PKG-A
Pre-contribution state
T0
SHA-A
        │
        │ externally asserted relationship
        ▼
PKG-B
Post-contribution state
T1
SHA-B
```

Full Stack may describe that relationship as strengthening, weakening,
challenging, revising, superseding, or something else.

Evidence Center does not choose the term.

This directly supports the principle expressed by PR #13:

> Later evidence should be able to change the model without rewriting
> what was believed before that evidence arrived.

The mapping therefore tests architectural sufficiency without making
Evidence Center a Full Stack component.

## Why Actor Provenance Matters for Reasoning Systems

Reasoning workflows increasingly combine human, LLM, and
system-generated states.

Without capture-time provenance, a later reviewer may know that content
changed but not whether the change was made by a human, model, or
automated process.

With package-level actor provenance:

``` text
T0  PKG-A  Human
T1  PKG-B  LLM
T2  PKG-C  LLM
T3  PKG-D  Human
```

the production path is inspectable without semantic analysis of the
payload.

This does not establish whether an actor was authorized to make the
change or whether the resulting content was correct.

Those are separate questions.

## Human Review and Disagreement

The Evidence Center does not require human review for every package or
relationship.

A reasoning system may operate autonomously and escalate only when its
own rules identify material disagreement, unresolved conflict,
insufficient confidence, or another review condition.

For example:

``` text
Model / System
      │
      ▼
  Outcome A
      │
      ▼
  Outcome B
      │
      ▼
External evaluation
   /          \
continue     dispute
                │
                ▼
          Human adjudication
                │
                ▼
           Outcome C
```

The Evidence Center preserves A, B, C, and externally asserted
relationships between them.

It does not decide when escalation is required.

This keeps human adjudication an exception-driven reasoning concern
rather than a mandatory provenance workflow.

## Trust Boundary

Preservation does not establish truth.

A content digest can demonstrate that bytes remain unchanged without
proving that the bytes were correct.

Actor provenance can record that an artifact was attributed to a human,
LLM, or system without proving that the actor was authorized or
trustworthy.

An external relationship can be preserved without the Evidence Center
endorsing its substantive validity.

Implementations may therefore add authentication, authorization, role
controls, operation logging, audit, retention policy, or certification
where required.

Those mechanisms are compatible with this architecture but are not part
of the minimal provenance kernel defined here.

## Failure Modes

Several failure modes help clarify the architectural boundary.

### Mutable-history collapse

A current artifact overwrites an earlier state, preventing
reconstruction of what existed at the earlier point.

### Identifier conflation

Package identity, content digest, external identity, and storage
location are treated as interchangeable.

### Actor ambiguity

Human, LLM, and system-produced states become indistinguishable.

### Relationship inference

A material connection is reconstructed from filenames, folder structure,
timestamps, or prose instead of being explicitly asserted.

### Semantic overreach

The provenance layer begins deciding whether an artifact is true,
relevant, sufficient, causal, or decision-worthy.

### Universal-ontology expansion

Domain-specific relationship types accumulate in the Evidence Center
core until the provenance architecture becomes coupled to one reasoning
system.

### False completeness

Missing provenance is filled with inferred values that appear
authoritative.

### Integrity without provenance

A digest confirms that content is unchanged, but the system cannot show
where the content came from, who supplied it, or how it was referenced.

## Evaluation Questions

The reference architecture remains a research proposal.

Useful evaluation questions include:

-   Can an exact historical payload be reconstructed?
-   Can package identity be distinguished from content identity?
-   Can the same content be captured in different provenance contexts
    without identity collision?
-   Can external identifiers be preserved without redefining them?
-   Can human, LLM, system, and unknown producers remain
    distinguishable?
-   Can a later relationship be added without modifying either connected
    package?
-   Can domain-specific relationship semantics remain outside the
    provenance core?
-   Can a reasoning system reconstruct an evidence path using only
    explicit references and relationships?
-   Can later evidence alter interpretation without rewriting prior
    states?
-   Can the same primitives preserve artifacts from materially different
    domains?
-   Can the architecture remain useful without becoming operationally
    burdensome?

The PR #13 mapping is one structural test. It is not validation of the
architecture.

## Open Questions

Several questions remain intentionally unresolved.

### Package granularity

What should count as one preserved outcome: an entire document, a
reasoning run, a message, a claim, or another domain-defined unit?

The reference architecture does not require one universal answer.

### Relationship granularity

Should relationships normally connect packages, external references,
content states, or other addressable objects?

Different implementations may require different levels of precision.

### Actor identity

How much actor identity is necessary beyond broad type distinctions such
as human, LLM, system, and unknown?

### Provenance depth

How far should a system recursively preserve dependencies such as
prompts, retrieved sources, model versions, tool calls, configurations,
and upstream evidence?

### Privacy and retention

How should immutable historical preservation coexist with deletion
requirements, privacy constraints, source revocation, and contractual
retention limits?

### Cost proportionality

Which outcomes require exact payload preservation, and when is bounded
metadata or an external content reference sufficient?

These are implementation and research questions rather than reasons to
expand the minimal kernel prematurely.

## What the Evidence Center Is Not

The Evidence Center is not:

-   a truth engine
-   a reasoning framework
-   a fact-checker
-   a universal knowledge graph
-   a mandatory human-review workflow
-   a model-evaluation framework
-   a document-management system by definition
-   an observability platform by definition
-   a replacement for domain judgment
-   proof that preserved evidence is correct
-   proof that a decision was justified

It preserves the record required for those questions to be investigated
elsewhere.

## Implementation Neutrality

The concepts in this reference architecture do not imply component
boundaries.

A system may embed them directly inside an existing reasoning
architecture.

They may be implemented as reusable components or a library.

They may also be operated as an independent provenance service shared by
multiple reasoning systems.

``` text
Reference Architecture
        │
        ▼
Conceptual Primitives
        │
        ├── Embedded implementation
        ├── Reusable component / library
        └── Independent provenance service
```

The architecture defines **what must remain distinguishable**, not how
many components must exist.

## Current Position

The Evidence Center is best described as a **domain-neutral reference
architecture for preserving immutable outcome states, content identity,
external identities, actor provenance, and externally declared
relationships across reasoning workflows**.

Its central boundary is simple:

> **The Evidence Center preserves what existed, who or what produced it,
> how external systems identify it, and how external systems say
> preserved states are connected. It does not decide what the evidence
> means.**

Full Stack v5 is one plausible producer and consumer of these records.
It remains a separate reasoning architecture.

Whether a reasoning system adopts these primitives directly, maps
existing constructs onto them, embeds them as reusable components, or
interoperates with an independent provenance layer is intentionally left
open.
