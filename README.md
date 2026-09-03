# AI Reasoning Systems for GTM Judgment

*How I am using AI to make executive and GTM reasoning more inspectable, evidence-disciplined, and harder to fool.*

## What This Repository Is

This repository documents a body of work focused on one question.

**How can AI help improve judgment without allowing speed, fluency, or confidence to outrun the evidence?**

I am an enterprise GTM executive, not a software developer. The work here is not a prompt library or a software codebase. It is a public portfolio of reasoning architectures, design principles, experiments, and practical applications developed through repeated use.

The point is not the tooling.

The point is the reasoning discipline underneath it.

## Why It Exists

Most AI workflows optimize for faster output.

In GTM and executive work, speed is not leverage if the diagnosis is wrong. AI can accept the premise too quickly, over-weight a vivid event, smooth over ambiguity, or turn a plausible explanation into more certainty than the evidence deserves.

That creates a larger risk than bad writing.

It can create bad intervention.

A visible issue may be a downstream symptom rather than the condition governing the outcome. A polished answer can make a weak diagnosis more persuasive rather than more accurate.

The core thesis behind this work is simple.

> **Better decisions come from better diagnosis.**

And the operating principle is equally important.

> **The advantage isn’t getting to the first answer faster. It’s knowing when the first answer shouldn’t be trusted.**

## The Core Idea

I use the term **logic lens** to describe a predefined way of examining a problem before AI produces an answer.

A prompt mostly defines the output.

A logic lens defines the reasoning path that should produce the output.

The current implementation is **Full Stack v4**, a reusable reasoning architecture designed to create deliberate friction before a conclusion is trusted.

```mermaid
flowchart LR
    A[Source Truth] --> B[Evidence Discipline]
    B --> C[Competing Explanations]
    C --> D[Causal Diagnosis]
    D --> E[Prognosis]
    E --> F[Pressure Testing]
    F --> G[Confidence and Revision]
    G --> H[Output]
```

The purpose is not to make every answer follow the same visible structure.

The purpose is to make the reasoning behind different answers more disciplined.

## Start Here

| Document | What it shows |
| --- | --- |
| [Building Friction Into AI](docs/building-friction-into-ai.md) | Why the work started, how the reasoning system is being built, and what remains unresolved |
| [What I Mean by a Logic Lens](docs/what-is-a-logic-lens.md) | A plain-English explanation of the core concept |
| [Full Stack v4 Public Architecture](architecture/full-stack-v4-public-architecture.md) | The high-level architecture behind the current reasoning system |
| [Evolution of the Reasoning System](architecture/evolution.md) | The design decisions that materially changed the system |

If you only read one document, start with **Building Friction Into AI**.

If you want the architecture, go directly to **Full Stack v4 Public Architecture**.

## How the Work Is Developed

The development loop is practical rather than theoretical.

```mermaid
flowchart LR
    A[Live Case] --> B[Initial Diagnosis]
    B --> C[Challenge It]
    C --> D[Codify Reusable Lesson]
    D --> E[Re-test on Another Case]
    E --> F[Use in Live Work]
    F --> A
```

AI serves two roles in that process.

It is the tool being guided by the reasoning system, and it is part of the environment used to expose where the reasoning system fails or overreaches.

A lesson is more useful when it survives a different case rather than merely improving the answer that revealed the weakness.

## Current Evidence and Limits

Full Stack v4 is functional and already used in live GTM thought leadership and executive work.

The evidence today is repeated practical use and iterative testing.

That is not the same as formal validation.

The current work can show observed failure modes, framework revisions, later retesting, and changes in how the system approaches diagnosis. It does not yet include a formal benchmark demonstrating that the architecture consistently improves reasoning quality.

A future evaluation layer should test diagnostic quality over time rather than relying only on whether the final writing improves.

A separate behavioral inference research direction is also still work in progress and will be documented publicly only when the underlying design is mature enough to support a dedicated artifact.

## Public Architecture and Private Implementation

This repository is intended to make the work inspectable without publishing the complete implementation.

The public material explains the problem, architecture, design principles, evolution, applications, and limits of the work.

The private material retains the detailed operating instructions, execution logic, internal tests, decision rules, and other implementation-level methods used to run the system.

That boundary is deliberate.

Credibility should come from showing that a real system exists, how it evolved, what failure modes it addresses, and where its limits remain.

It does not require publishing every instruction needed to replicate it.

See [Rights and Reuse](RIGHTS.md) for the repository's reuse terms.

## What Is Next

Planned additions include

- an evaluation approach focused on reasoning quality
- a public GTM diagnostic application note
- a Behavioral Inference Engine design note when the design is sufficiently mature
- reconstructed and anonymized examples showing how a reasoning intervention changed the diagnosis, confidence, recommendation, or decision

These will be added only when the underlying material is strong enough to support the claim the artifact is intended to prove.

## About Scott Schoenfeld

I am an enterprise GTM executive who has spent my career operating in complex technology markets.

I use AI as a reasoning and decision-support tool, not as a substitute for commercial judgment.

This repository makes that approach inspectable. It shows how I am developing, testing, challenging, and revising systems intended to improve diagnosis before action.

The work is practical, versioned, and still evolving.
