## Ruthvik Garlapati

I build infrastructure for systems that have to keep running when something
breaks — Kubernetes platforms, GPU inference serving, and the observability and
rollback machinery around them.

Most of what's here is me taking an idea that usually needs a whole platform
team, and finding out how far one person can get.

### Projects

**[temporalops](https://github.com/therealruthvik/temporalops)** — Self-healing
Kubernetes canary orchestrator. Rollouts run as a durable Temporal workflow, so
a rollback survives the controller dying mid-deploy. *Go, Temporal, Kubernetes.*

**[inference-platform](https://github.com/therealruthvik/inference-platform)** —
Benchmarks vLLM against NVIDIA Triton on the same hardware, with autoscaling
driven by real queue depth instead of CPU. *vLLM, Triton, KEDA.*

**[perception-sentinel](https://github.com/therealruthvik/perception-sentinel)**
— Autonomous-vehicle perception pipeline built to be broken: chaos injection on
the GPU path, LLM fallback when inference degrades. *Python, FastAPI, Modal.*

**[sentinalflow](https://github.com/therealruthvik/sentinalflow)** — Multi-tenant
SLO observability. Streams metrics through Kafka and Spark, and trips a rollback
when an error budget burns too fast. *Kafka, Spark, Prometheus.*

**[riskdiff](https://github.com/therealruthvik/riskdiff)** — Pre-commit scanner
that flags risky diffs before a human reviews them. Runs fully offline, outputs
SARIF. *Node.js, CLI.*

More in [my repositories](https://github.com/therealruthvik?tab=repositories).

### Elsewhere

[LinkedIn](https://www.linkedin.com/in/ruthvikg31/) ·
[LeetCode](https://leetcode.com/ruthvikg31/) ·
[Email](mailto:ruthvik.garla@gmail.com)
