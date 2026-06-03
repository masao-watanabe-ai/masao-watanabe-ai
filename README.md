# AI is not prediction. It is decision.
Turn AI outputs into reproducible, controllable decisions

---

Chinoba
Intelligence as Relationship

https://chinoba.org

---

## Problem
AI systems stop in production.

Why?

Because AI produces **signals**, not **decisions**.

- Predictions are probabilistic
- Decisions are accountable
- Signals are continuous
- Decisions are discrete

👉 This gap breaks real-world systems.

---

## Solution
Decision Trace Model

👉 A system that turns signals into **traceable, controllable decisions**

---

## Core Principle

AI produces signals.  
**Only the runtime produces decisions.**

---

## Architecture

Decision Flow:

Interaction → Signal → **Decision (Runtime)** → Boundary → Human → Log

👉 All decisions are evaluated and finalized in the runtime.

---

## Decision Runtime

### decision-runtime-core  
https://github.com/masao-watanabe-ai/decision-runtime-core  

→ **Decision OS Kernel**

The runtime is the **single point of decision**:

- Evaluates signals
- Applies decision logic
- Enforces boundaries
- Invokes human gates
- Produces execution-ready outcomes
- Records full decision traces

👉 Without this layer, AI outputs remain uncontrolled signals.

---

## OSS Ecosystem

### Input / Interaction

- interaction-core-v2  
  https://github.com/masao-watanabe-ai/interaction-core-v2  
  → Input / Interaction Layer for Decision OS — converts messages and evidence into structured signals

---

👉 Runtime makes decisions. Ledger records them. View makes them understandable.

### Core (Decision System)

- decision-runtime-core  
  https://github.com/masao-watanabe-ai/decision-runtime-core  
  → **Decision OS Kernel (center of the system)**  

- decision-trace-model-v2  
  https://github.com/masao-watanabe-ai/decision-trace-model-v2  
  → **Decision protocol specification**  

- decision-trace-ledger-core-k2  
  https://github.com/masao-watanabe-ai/decision-trace-ledger-core-k2  
  → Append-only, hash-chained ledger for traceable and reproducible decisions
 
- dtm-view-core-v2  
  https://github.com/masao-watanabe-ai/dtm-view-core-v2  
  → Decision Trace Interface — visualizes and explores runtime decision traces  

---

### Execution

- multi-agent-orchestrator-core-v2  
  https://github.com/masao-watanabe-ai/multi-agent-orchestrator-core-v2  
  → Execution layer for Decision Runtime OS  

👉 Execution does NOT decide. It follows runtime decisions.

---

### Design
- Decision Trace Studio (v1)  
  https://github.com/masao-watanabe-ai/decision-trace-studio  
  → Reference / initial implementation  

- Decision Trace Studio v2  
  https://github.com/masao-watanabe-ai/decision-trace-studio-v2  
  → Design, simulate, and improve decision systems  

---

### Learning
- decision-trace-gnn-core-v2  
  https://github.com/masao-watanabe-ai/decision-trace-gnn-core-v2  
  → Learning layer of Decision OS — learns from ledgered decision traces and emits signals for the runtime

👉 GNN does NOT make decisions. Runtime remains the only decision authority.

---

### Legacy

- decision-trace-model  
  https://github.com/masao-watanabe-ai/decision-trace-model  

- interaction-core  
  https://github.com/masao-watanabe-ai/interaction-core  
  → Input / interaction layer

- decision-trace-gnn-core (v1)  
  https://github.com/masao-watanabe-ai/decision-trace-gnn-core 

- dtm-view-core  
  https://github.com/masao-watanabe-ai/dtm-view-core  
  → Legacy decision trace viewer (superseded by dtm-view-core-v2) 

- Decision-Trace-Ledger-Core (v1)  
  https://github.com/masao-watanabe-ai/Decision-Trace-Ledger-Core  
  → Initial standalone ledger implementation (superseded by k2)

- multi-agent-orchestrator-core (v1)  
  https://github.com/masao-watanabe-ai/multi-agent-orchestrator-core  

---

## Demo
👉 https://manufacturing-demo-local.vercel.app/  
👉 https://multi-agent-demo-nine.vercel.app/

---

## Quick Start
👉 Starter Kit (v2 – Runtime-connected)  
https://github.com/masao-watanabe-ai/light-dtm-starter-kit-cs-v2  

👉 Starter Kit (v1 – Standalone / local decision)  
https://github.com/masao-watanabe-ai/light-dtm-starter-kit-cs  

---

## Why this matters

Most AI systems fail not because of model quality,  
but because **decisions are not designed**.

- No clear responsibility
- No reproducibility
- No auditability
- No boundary control

DTM solves this by making decisions:

- Explicit  
- Structured  
- Reproducible  
- Governed  

---

## From AI to Decision Systems

Traditional AI:
Data → Model → Prediction → ??? → Human

DTM:
Interaction → Signal → Runtime → Decision → Execution → Log

---

## Learn More

### 📘 Books

These ideas have been compiled into the following books.

#### 🇯🇵 Japanese Editions

**Decision Trace Model 実践導入ガイド**
— 製造・医療・リテール・マルチエージェントで学ぶAI意思決定システム —
Decision Trace Model（DTM）の実践的なケーススタディや導入方法をまとめました。

Available on Kindle
👉 https://amzn.to/4o5oyXT

**Trust Infrastructure AI時代の信用基盤**
— Trace・Reputation・Coordinationが支える次世代社会 —
AI時代の信用基盤（Trust Infrastructure）を解説しました。

Available on Kindle
👉 https://amzn.to/3RJgQHa

**AI is not prediction. It is decision.**
— Decision Trace Model Practical Guide —
A practical guide for designing AI as a decision system.

Available on Kindle
👉 https://amzn.to/4twsoui

**Intelligence Field — AI from “Intelligence” to “Relationship”**
Exploring intelligence as relationships between AI, humans, organizations, and society.

Available on Kindle
👉 https://amzn.to/4uN51hl

**What Kind of Mathematical Worldview Is AI Built Upon?**
— From Finite Rules to Generative Models —

Available on Kindle
👉 https://amzn.to/4frireb

**Intelligence Field Economics**
— Chinōba Keizai —
*Trust, Knowledge and Coordination in the AI Era*

Available on Kindle
👉 https://amzn.to/49A4JC8


#### 🇺🇸 English Editions

**Decision Trace Model Practical Implementation Guide**
— A Practical Guide to Connecting AI-Powered Judgment to Real-World Organizational Implementation —
A practical implementation guide for applying Decision Trace Model (DTM) to manufacturing, healthcare, retail, and multi-agent systems.

Available on Kindle
👉 https://amzn.to/4x5zNUo

**The Trust Infrastructure in the Age of AI**
— How Trace, Reputation, and Coordination Power the Next Generation Society —
This book explains the concept of Trust Infrastructure and explores how trust, reputation, verification, and coordination form the foundation of society in the AI era.

Available on Kindle
👉 https://amzn.to/4dNGtiE

**AI is not prediction. It is decision.**
— Decision Trace Model Practical Guide —
A practical guide for designing AI as a decision system.

Available on Kindle
👉 https://www.amazon.com/dp/B0GX2XWJJG

**Intelligence Field — Intelligence as Relationship**
A new perspective on AI, relational intelligence, and social intelligence fields.

Available on Kindle
👉 https://www.amazon.com/dp/B0H1GM1M75

**What Kind of Mathematical Worldview Is AI Built Upon?**
— From Finite Rules to Generative Models —

Available on Kindle
👉 https://amzn.to/3PcGpzs

**Intelligence Field Economics**
— Chinōba Keizai —
*Trust, Knowledge and Coordination in the AI Era*

Available on Kindle
👉 https://amzn.to/49HvoNp

---

### 📖 Blog  
Deep dive into Decision Trace Model, architecture, and real-world use cases  
👉 https://deus-ex-machina-ism.com  

---

### 💼 LinkedIn  
Insights, discussions, and latest updates  
👉 https://www.linkedin.com/in/masao-watanabe-ai  

---
