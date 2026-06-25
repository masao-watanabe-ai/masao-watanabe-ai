# Chinoba
**Intelligence as Relationship**

An open research ecosystem exploring the infrastructure for Human–AI Coordination.

[chinoba.org](https://chinoba.org)

---

## What is Chinoba

Chinoba is an open research ecosystem built on a single idea:
**intelligence is not a property of a model — it emerges in relationship.**

That idea is the foundation. Everything else is built on top of it, across
three layers:

| Layer | What it is |
|---|---|
| **Philosophy** | *Intelligence as Relationship* — the worldview |
| **Research Streams** | The **Decision Stream** (Trust → Knowledge → Decision) and the **Coordination Stream** (Governance → Coordination → Society) |
| **Implementation** | An open-source architecture that puts the research into practice |

The research is not a collection of separate projects. It is two streams
built on one philosophy — one that produces accountable decisions, the other
that coordinates humans and AI around them.

---

## Intelligence as Relationship

We usually ask how *intelligent* a model is — as if intelligence were
something a system possesses on its own.

Chinoba starts from a different premise: **intelligence is relational.**
It does not live inside a model. It emerges in the relationships between
AI, humans, organizations, and society — in how they trust each other,
share what they know, decide, and act together.

This reframes the engineering problem. If intelligence is relational, then
building better AI is not only about better models. It is about building the
**infrastructure of the relationship** — the trust, the knowledge, the
accountable decisions, and the coordination that let humans and AI act
together in the open.

→ Read the worldview in depth: [`docs/philosophy/`](docs/philosophy/)

> Relationships are not enough on their own. At some point, intelligence
> must *act*. And action raises a harder question —
> **is AI prediction, or is it decision?**

---

## Research Streams

Modern AI research has focused on the **model** — making it larger, faster,
more capable. Chinoba focuses on something else: the **infrastructure that
lets those models take part in human society.**

That infrastructure has two complementary goals:

- **producing accountable decisions**, and
- **coordinating humans and AI around those decisions.**

So Chinoba is pursued as two complementary research streams — both growing
from the same philosophy, *Intelligence as Relationship*. One asks how a
single accountable decision is *produced*; the other asks how many humans
and AI *coordinate* around it.

---

### Decision Stream
*How signals become accountable decisions.*

AI systems emit **signals** — probabilistic, continuous, unaccountable. This
stream is about turning those signals into decisions we can own. Each stage
prepares the signal for the one after it.

**1 · Trust Infrastructure**
Trust enables reliable relationships. Before anything can be acted on, there
must be a way to establish, trace, and verify trust between AI, people, and
organizations.
→ [`docs/themes/trust-infrastructure.md`](docs/themes/trust-infrastructure.md)

**2 · Knowledge Infrastructure**
Knowledge enables meaningful signals. Structured, reliable knowledge is what
gives a raw signal context and significance.
→ [`docs/themes/knowledge-infrastructure.md`](docs/themes/knowledge-infrastructure.md)

> Together, trust and knowledge make signals **decision-ready.**

**3 · Decision Trace Model**
Decision-ready signals still are not decisions. The Decision Trace Model is
the transformation at the center of Chinoba:

> ## Signal → Decision

AI produces the signal. Only the runtime produces the decision — discrete,
traceable, and owned — and carries it through to accountable action.

> ### AI is not prediction. It is decision.

→ [`docs/themes/decision-trace-model.md`](docs/themes/decision-trace-model.md)

---

Accountable decisions are not the destination. They are what a society
coordinates around.

---

### Coordination Stream
*How humans and AI coordinate around those decisions.*

A single good decision is not enough. Decisions must be bounded, scaled, and
woven into how many agents and people act together.

**4 · Governance**
Accountable decisions need limits — boundaries, human authority, and the
right to say no. Governance defines who is responsible for what.
→ [`docs/themes/governance.md`](docs/themes/governance.md)

**5 · Multi-Agent Coordination**
Real systems are many agents acting at once. This stage carries shared
decisions across them without losing accountability.
→ [`docs/themes/multi-agent-coordination.md`](docs/themes/multi-agent-coordination.md)

**6 · Runtime Society**
Runtime Society integrates everything above — trust, knowledge, decisions,
governance, and coordination — into humans and AI coordinating in the open,
in real time. It is not a later version of any one theme; it is where they
meet.
→ [`docs/themes/runtime-society.md`](docs/themes/runtime-society.md)

---

## Open-Source Architecture

The research above explains what Chinoba explores. This section shows how
those ideas are implemented through an open-source architecture — organized
into five layers.

Each layer notes which research stream it primarily serves. Most of it
implements the **Decision Stream**: producing, executing, and improving
accountable decisions.

---

### Interaction
*Supports both streams.*

Turns raw messages and evidence into structured signals the rest of the
system can reason over — the entry point for everything downstream.

- **interaction-core-v2** — input / interaction layer; converts messages and
  evidence into structured signals
  https://github.com/masao-watanabe-ai/interaction-core-v2

---

### Core / Decision Runtime
*Primarily implements the Decision Stream.*

The runtime is the **single point of decision**. It evaluates signals,
applies decision logic, enforces boundaries, invokes human gates, produces
execution-ready outcomes, and records a full, replayable trace of every
decision.

> The runtime is the only decision authority. Every other layer produces
> signals, follows decisions, or makes them understandable — none of them
> decide.

- **decision-runtime-core** — the Decision OS kernel; the center of the system
  https://github.com/masao-watanabe-ai/decision-runtime-core
- **decision-trace-model-v2** — the decision protocol specification
  https://github.com/masao-watanabe-ai/decision-trace-model-v2
- **decision-trace-ledger-core-k2** — append-only, hash-chained ledger for
  traceable, reproducible decisions
  https://github.com/masao-watanabe-ai/decision-trace-ledger-core-k2
- **dtm-view-core-v2** — decision-trace interface; visualizes and explores
  runtime decision traces
  https://github.com/masao-watanabe-ai/dtm-view-core-v2

---

### Execution
*Executes runtime decisions in the real world.*

Carries finalized runtime decisions out into action — through agents, APIs,
workflows, tools, and external systems. Execution does not decide; it
faithfully enacts decisions the runtime has already made.

- **multi-agent-orchestrator-core-v2** — execution layer for the Decision
  Runtime; enacts finalized decisions across agents, tools, and systems
  https://github.com/masao-watanabe-ai/multi-agent-orchestrator-core-v2

---

### Learning
*Improves future runtime decisions.*

Learns from the ledgered history of past decisions and emits better signals
back to the runtime. It learns; it never decides.

- **decision-trace-gnn-core-v2** — learning layer; learns from ledgered
  decision traces and emits signals for the runtime
  https://github.com/masao-watanabe-ai/decision-trace-gnn-core-v2

---

### Design
*Supports both streams by modeling and simulating systems.*

Where decision and coordination systems are designed, simulated, and improved
before and after they run.

- **decision-trace-studio-v2** — design, simulate, and improve decision systems
  https://github.com/masao-watanabe-ai/decision-trace-studio-v2

---

> **Where is the Coordination Stream?**
> Coordination is not a single layer. It is a higher-level research problem —
> Governance, Multi-Agent Coordination, and Runtime Society — that emerges
> from the *behavior* of systems built on top of these layers. The
> implementation here produces accountable decisions; coordination is what
> societies of humans and AI do with them.

---

<details>
<summary>Earlier / superseded repositories</summary>

These predate the current architecture and remain available for reference:

- **decision-trace-model** — original DTM
  https://github.com/masao-watanabe-ai/decision-trace-model
- **interaction-core** — original interaction layer (→ interaction-core-v2)
  https://github.com/masao-watanabe-ai/interaction-core
- **decision-trace-gnn-core** — v1 learning layer (→ decision-trace-gnn-core-v2)
  https://github.com/masao-watanabe-ai/decision-trace-gnn-core
- **dtm-view-core** — v1 trace viewer (→ dtm-view-core-v2)
  https://github.com/masao-watanabe-ai/dtm-view-core
- **Decision-Trace-Ledger-Core** — standalone ledger (→ ledger-core-k2)
  https://github.com/masao-watanabe-ai/Decision-Trace-Ledger-Core
- **multi-agent-orchestrator-core** — v1 orchestrator
  https://github.com/masao-watanabe-ai/multi-agent-orchestrator-core
- **decision-trace-studio** — v1 / reference studio
  https://github.com/masao-watanabe-ai/decision-trace-studio

</details>

→ Full architecture and decision flow: [`docs/architecture/`](docs/architecture/)

---

## Architecture

One flow, end to end. AI proposes; the runtime decides and records the
decision; humans stay in the loop; execution carries it out.

```
   Interaction
        ↓
     Signal
        ↓
 Decision (Runtime)
        ↓
    Boundary
        ↓
     Human
        ↓
   ┌────┴─────┐
Execution    Log
           (decision trace)
```

The runtime records the **decision trace as part of the decision** — not as a
final step after execution. Once a decision is finalized through its
boundaries and human gate, the runtime both records it and dispatches it for
execution. Execution may then succeed or fail; the decision and its trace
already exist, independently of the outcome.

Four principles explain the whole picture:

- **Trust enables reliable relationships.**
- **Knowledge enables decision-ready signals.**
- **The runtime transforms signals into accountable decisions — and records
  the trace as it decides.**
- **Execution realizes decisions — coordination emerges from the systems built
  on top of them.**

→ Full architecture and decision flow: [`docs/architecture/`](docs/architecture/)

---

## Demos

See the runtime make and trace decisions in real scenarios.

- **Manufacturing** — decision-making and tracing on a production line
  https://manufacturing-demo-local.vercel.app/
- **Multi-Agent** — many agents acting under shared runtime decisions
  https://multi-agent-demo-nine.vercel.app/

→ More demos and walkthroughs: [`docs/demos/`](docs/demos/)

---

## Quick Start

Clone a starter kit, run it, and watch a decision become a trace.

- **Starter Kit v2 — runtime-connected** *(recommended)*
  Connected to the Decision Runtime; the full signal → decision → trace flow.
  https://github.com/masao-watanabe-ai/light-dtm-starter-kit-cs-v2
- **Starter Kit v1 — standalone**
  Local, self-contained decision logic with no runtime dependency.
  https://github.com/masao-watanabe-ai/light-dtm-starter-kit-cs

---

## Books

The ideas behind Chinoba are developed in depth across a series of books, in
both Japanese and English. Two starting points:

- **Intelligence Field — Intelligence as Relationship** — the philosophy
  https://www.amazon.com/dp/B0H1GM1M75
- **AI is not prediction. It is decision.** — the Decision Trace Model in practice
  https://www.amazon.com/dp/B0GX2XWJJG

→ Full bibliography (JP & EN): [`docs/books/`](https://chinoba.org/library/)

---

## Vision

Chinoba is not a collection of repositories. It is an evolving research
ecosystem with a single aim: to build the infrastructure for Human–AI
Coordination — trust, knowledge, accountable decisions, and the coordination
that lets humans and AI act together in the open.

The destination is not better models.  
It is better relationships.

Between humans.  
Between AI.  
Between organizations.  
Between society.

> ### From Intelligence, to Relationship, to Society.

---

## Explore Chinoba

- **Website** — [chinoba.org](https://chinoba.org)
- **Research Blog** — [deus-ex-machina-ism.com](https://deus-ex-machina-ism.com)
- **Books** — [full bibliography](https://chinoba.org/library/)
- **YouTube** — [Chinoba Research Archive](https://www.youtube.com/@masawata-f2f)
- **LinkedIn** — [masao-watanabe-ai](https://www.linkedin.com/in/masao-watanabe-ai)

---

**Chinoba** · *Intelligence as Relationship*
