# AI is not prediction. It is decision.
Turn AI outputs into reproducible, controllable decisions

---

## Problem
Why AI systems stop in production.  
AI systems produce signals, but not decisions.

---

## Solution
Decision Trace Model

---

## Demo
👉 https://manufacturing-demo-local.vercel.app/  
👉 https://multi-agent-demo-nine.vercel.app/

---

## Architecture

Decision Flow:  
Interaction → Signal → **Decision (Runtime)** → Boundary → Human → Log

👉 All decisions are evaluated and finalized in **decision-runtime-core**

---

## OSS Ecosystem

### Input / Interaction
- interaction-core  
  https://github.com/masao-watanabe-ai/interaction-core  
  → Input / interaction layer for decision systems

---

### Core (Decision Layer)

- decision-trace-model  
  https://github.com/masao-watanabe-ai/decision-trace-model  
  → Conceptual model for structuring decisions

- decision-runtime-core  
  https://github.com/masao-watanabe-ai/decision-runtime-core  
  → **Decision OS Kernel**  
  → The single point where signals are evaluated and decisions are finalized

- Decision Trace Ledger  
  https://github.com/masao-watanabe-ai/Decision-Trace-Ledger-Core  
  → Stores decision traces for auditability and reproducibility

- dtm-view-core  
  https://github.com/masao-watanabe-ai/dtm-view-core  
  → Visualizes decision structures and traces

---

### Execution
- multi-agent-orchestrator-core  
  https://github.com/masao-watanabe-ai/multi-agent-orchestrator-core  
  → Executes actions based on finalized decisions

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

## Quick Start
👉 Starter Kit  
https://github.com/masao-watanabe-ai/light-dtm-starter-kit-cs

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
