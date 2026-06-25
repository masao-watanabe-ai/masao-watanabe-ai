# Architecture

The full decision flow and the open-source layers that implement it.

```
Interaction → Signal → Decision (Runtime) → Boundary → Human → ┬ Execution
                                                               └ Log (decision trace)
```

Layers: **Interaction · Core / Decision Runtime · Execution · Learning ·
Design.** The runtime is the only decision authority; the trace is recorded
as part of the decision, independent of execution outcomes.

> Detailed documentation is in progress.

← Back to the [Chinoba overview](../../README.md)
