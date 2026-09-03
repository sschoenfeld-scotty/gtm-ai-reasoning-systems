# Building Friction Into AI

*How I’m using AI to build a repeatable reasoning system for GTM judgment*

> Work in progress | August 2026

**The most useful thing I’ve built with AI isn’t a prompt. It’s friction.**

## Why I started

Most AI workflows optimize for faster output. I started from a different problem. In GTM, speed is not leverage if the diagnosis is wrong. AI can accept a premise, over-weight a vivid event, or turn a plausible explanation into more certainty than the evidence deserves.

The risk is not just bad writing. It is bad intervention. The visible issue can be a downstream symptom rather than the governing constraint. If that distinction is missed, AI can make the wrong action faster, cleaner, and more convincing.

## What I’m building

I call the core approach a **logic lens**. A prompt mostly defines the output. A logic lens defines how the problem should be examined before the output is trusted.

The current implementation is **Full Stack v4**, a reusable reasoning architecture designed to separate observation from inference and keep alternative explanations open. It also asks what evidence would weaken the current conclusion before that conclusion becomes a recommendation.

### The two-part system

| Component | Plain English | Role |
| --- | --- | --- |
| **Operating Manual** | The playbook | Defines the deep reasoning architecture, evidence discipline, and the conditions that should force the system to challenge its own diagnosis. |
| **Execution Prompt** | The game-day call sheet | Applies the same reasoning quickly to daily LinkedIn work and executive GTM analysis. |

Today, that discipline is encoded in working prompts and source documents, but the asset is not a single prompt. It is a repeatable reasoning system that can be applied across different problems and revised when the evidence changes.

## Where the idea is going

The next layer is a **Behavioral Inference Engine**. This is not a finished product. It is the design direction.

The goal is for AI to maintain a longitudinal view of behavior without silently converting an observation into motive. Assumed intention stays a hypothesis, and competing explanations stay open until the evidence meaningfully favors one.

A current design problem is model revision. A vivid outlier may reveal something important, but it can also distort the broader pattern. The engine needs a disciplined way to decide which is happening.

## How I’m using AI to build it

AI is not just receiving instructions. It is also the design partner and test environment. I run real GTM situations and public writing through the system, then inspect where the reasoning fails or overreaches. If the lesson is reusable, I codify it into the lens and test it again against a different case.

**Live case → Initial diagnosis → Challenge it → Codify lesson → Re-test → Use in live work**

That loop is the point. AI is both the tool and part of the experiment. The system is being shaped through repeated use, with each revision expected to survive a new case rather than merely improve the last answer.

## Build journey and current state

| Stage | What changed |
| --- | --- |
| **1 · Problem** | AI was fluent but too willing to accept the premise. The first design goal was deliberate reasoning friction before writing. |
| **2 · v3** | The framework moved beyond surface agreement. It added hidden-assumption analysis and a human-systems view, then began playing likely consequences forward. |
| **3 · v4** | The architecture became explicit around evidence discipline and structured self-challenge. The system was designed to make uncertainty visible before a recommendation was trusted. |
| **4 · Two-part system** | The work split into an Operating Manual for deep reasoning and an Execution Prompt for daily application. A separate plain-English guide made the logic-lens concept easier to explain without AI jargon. |
| **5 · Now** | Full Stack v4 is being used in live GTM thought leadership and executive work. The next layer is focused on attribution discipline and longitudinal behavioral inference. |

## Current state

Full Stack v4 is functional and already used in live work. The Operating Manual and Execution Prompt now operate as a matched system, with a plain-English guide explaining the concept.

The framework has moved beyond one-off prompting into reusable reasoning architecture. The evidence today is repeated practical use and iterative testing, not a formal benchmark. The Behavioral Inference Engine remains a work in progress.

## Work left

The next work is to formalize how the system handles attribution and assumed intention. It also needs a model-update rule for deciding when an outlier should change the pattern rather than be treated as noise.

A later evaluation layer should test diagnostic quality over time, not just whether the writing improves.

## What this showcases about how I use AI

I am not using AI to outsource commercial judgment. I am using it to make the judgment process more inspectable and harder to fool.

AI helps me expose assumptions and pressure-test causal logic, while I retain responsibility for the conclusion. The learning from one case is then carried forward and challenged against the next.

Whether the visible output is public writing or executive GTM work, the asset being built is the reasoning discipline underneath it.

**The advantage isn’t getting to the first answer faster. It’s knowing when the first answer shouldn’t be trusted.**
