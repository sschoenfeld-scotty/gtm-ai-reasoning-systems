# What I Mean by a "Logic Lens"

*A plain-English explanation using Full Stack v5.1 as the example*

When I use the term **logic lens**, I mean a predefined way of examining a problem before AI produces an answer. It doesn’t just tell AI what to write. It tells AI what to inspect, what to challenge, what evidence to trust, and what the conclusion needs to survive before it is delivered.

> **A prompt mostly defines the output. A logic lens defines the reasoning path that should produce the output.**

## Why I Use Logic Lenses

Without a lens, AI can move from a prompt to a fluent answer too quickly. It can accept the premise, smooth over ambiguity, or turn an assumption into a confident-sounding conclusion.

A logic lens deliberately interrupts that jump. It creates a repeatable discipline for establishing what is actually known before the model recommends, explains, writes, or acts.

## How a Logic Lens Can Be Specialized

A logic lens does not have to be defined by an industry.

Some reasoning problems are better organized around an operating domain or recurring decision environment that appears across many industries.

Go-to-market is one example. The [GTM Diagnostic Framework v9](../architecture/gtm-diagnostic-framework-v9-public-architecture.md) is specialized around the commercial system rather than around one market. Its value does not come only from knowing more GTM terminology or facts. It makes recurring dependencies inside the revenue system explicit and requires the diagnosis to change when those dependencies change.

That distinction matters because specialization should improve the reasoning, not simply add more subject matter.

Industry context can still affect what evidence matters, what constraints apply, and what decisions are available. Organization-specific experience can add another layer of context. Neither automatically requires a separate logic lens.

A distinct specialized lens becomes more defensible when the recurring decision environment requires important relationships, evidence standards, or failure modes to be made explicit so they are applied more reliably.

The useful boundary is therefore not automatically the industry.

It is the reasoning environment the lens must handle well.

## Full Stack v5.1 Is One Logic Lens

Full Stack v5.1 is designed to improve diagnosis before writing or action. Its core idea remains simple.

**Better decisions come from better diagnosis.**

Before producing the final output, it asks the model to work through questions like these.

- What is actually known, and what is being inferred?
- What else could explain the same observable facts?
- What condition is really governing the outcome?
- When communication purpose matters, what function may the statement actually be serving?
- What is most likely to happen if nothing changes or the wrong thing changes?
- Could the proposed action create credible downside that is difficult or impossible to reverse?
- Even if the diagnosis is correct, is the problem worth solving relative to other uses of scarce resources?
- What evidence would weaken the conclusion, change the prognosis, or change the decision?
- When experience creates a strong prior, would more diagnostic evidence improve the decision enough to justify the delay required to obtain it?

One important change introduced in v5 is the distinction between diagnosis and action. v5.1 adds Compressed Diagnosis, which governs when a strong prior can reduce additional diagnostic expansion without bypassing diagnosis.

Current v5.1 invocation uses Deep Path and maximum Full Stack execution by default. Fast Path and Standard Path remain defined but dormant. Maximum execution means the complete architecture is considered at the deepest available reasoning level and continues only while another increment of reasoning or evidence can materially improve the judgment.

> **A correct diagnosis is necessary for a good decision. It does not make every diagnosed problem worth solving.**

## The Two Parts of Full Stack v5.1

| | Operating Manual | Execution Prompt |
| --- | --- | --- |
| **Plain English** | The playbook | The game-day call sheet |
| **Role** | Defines the governing reasoning architecture for the current maximum-execution path | Acts as the execution control surface that applies the matched architecture to a specific task |
| **Best Use** | Governing architecture for Full Stack reasoning | Day-to-day execution without changing the reasoning tier |

## What the Lens Is Supposed to Change

The goal isn’t to make AI sound smarter. It’s to make the reasoning more disciplined.

A useful logic lens should reduce reflexive agreement, make uncertainty visible, pressure-test the first explanation, and produce an answer that is more grounded in the actual problem.

Full Stack v5.1 extends that discipline by asking whether the diagnosis is right, whether acting on it is strategically warranted, and whether more diagnostic work has enough expected decision value to justify its cost or delay.

The stopping rule is not a fixed number of questions or challenge passes. The lens keeps going while another increment can materially improve or weaken the conclusion, change confidence, favor a credible alternative, change the decision boundary, or change what should be done.

> **The writing is the output. The logic lens is the thinking discipline behind it.**
