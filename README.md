# AI is not prediction. It is decision.
Turn AI outputs into reproducible, controllable decisions

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

- interaction-core  
  https://github.com/masao-watanabe-ai/interaction-core  
  → Input / interaction layer

---

### Core (Decision System)

- decision-runtime-core  
  https://github.com/masao-watanabe-ai/decision-runtime-core  
  → **Decision OS Kernel (center of the system)**  

- decision-trace-model  
  https://github.com/masao-watanabe-ai/decision-trace-model  
  → Conceptual model of decisions  

- Decision Trace Ledger  
  https://github.com/masao-watanabe-ai/Decision-Trace-Ledger-Core  
  → Stores decision traces (audit / replay / governance)  

- dtm-view-core  
  https://github.com/masao-watanabe-ai/dtm-view-core  
  → Visualizes decisions and traces  

---

### Execution

- multi-agent-orchestrator-core  
  https://github.com/masao-watanabe-ai/multi-agent-orchestrator-core  
  → Executes actions based on finalized decisions  

👉 Execution does NOT decide. It follows decisions.

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
- decision-trace-gnn-core  
  https://github.com/masao-watanabe-ai/decision-trace-gnn-core  
  → Learn decision structures from traceable decision data using Graph Neural Networks

---

## Demo
👉 https://manufacturing-demo-local.vercel.app/  
👉 https://multi-agent-demo-nine.vercel.app/

---

## Quick Start
👉 Starter Kit  
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

### 📘 Book  
This concept has been compiled into a practical guide.

"AI is not prediction. It is decision."  
— Decision Trace Model Practical Guide —

Available now on Kindle  
English edition coming soon  

👉 https://amzn.to/3Oso8Od

---

### 📖 Blog  
Deep dive into Decision Trace Model, architecture, and real-world use cases  
👉 https://deus-ex-machina-ism.com  

---

### 💼 LinkedIn  
Insights, discussions, and latest updates  
👉 https://www.linkedin.com/in/masao-watanabe-ai  

---
