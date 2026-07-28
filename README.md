<!-- ===== THEME-AWARE HERO BANNER ===== -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/therealruthvik/therealruthvik/main/dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/therealruthvik/therealruthvik/main/light.svg">
  <img alt="Ruthvik Garlapati" src="https://raw.githubusercontent.com/therealruthvik/therealruthvik/main/light.svg">
</picture>

<!-- ===== GITHUB STATS ===== -->

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com/?user=therealruthvik&hide_border=true&background=0A101F&stroke=38BDF8&ring=A78BFA&fire=10B981&currStreakLabel=38BDF8&sideLabels=94A3B8&currStreakNum=F8FAFC&sideNums=F8FAFC&dates=64748B&titleColor=38BDF8&card_width=1180" />
  <img width="100%" src="https://streak-stats.demolab.com/?user=therealruthvik&hide_border=true&background=FFFFFF&stroke=0284C7&ring=7C3AED&fire=059669&currStreakLabel=0284C7&sideLabels=475569&currStreakNum=0F172A&sideNums=0F172A&dates=94A3B8&titleColor=0284C7&card_width=1180" alt="Ruthvik's streak" />
</picture>

<br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=therealruthvik&show_icons=true&count_private=true&include_all_commits=true&hide_rank=true&hide_border=true&title_color=38BDF8&icon_color=A78BFA&text_color=94A3B8&bg_color=0A101F&card_width=500" />
  <img width="49%" src="https://github-readme-stats.vercel.app/api?username=therealruthvik&show_icons=true&count_private=true&include_all_commits=true&hide_rank=true&hide_border=true&title_color=0284C7&icon_color=7C3AED&text_color=0F172A&bg_color=FFFFFF&card_width=500" alt="Ruthvik's GitHub stats" />
</picture>
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=therealruthvik&layout=compact&langs_count=8&hide_border=true&title_color=38BDF8&text_color=94A3B8&bg_color=0A101F&card_width=500" />
  <img width="49%" src="https://github-readme-stats.vercel.app/api/top-langs/?username=therealruthvik&layout=compact&langs_count=8&hide_border=true&title_color=0284C7&text_color=0F172A&bg_color=FFFFFF&card_width=500" alt="Top languages" />
</picture>

</div>

<!-- ===== CONTRIBUTION SNAKE ===== -->

<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/therealruthvik/therealruthvik/output/snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/therealruthvik/therealruthvik/output/snake-light.svg" />
  <img alt="Snake eating my contributions" src="https://raw.githubusercontent.com/therealruthvik/therealruthvik/output/snake-light.svg" />
</picture>

</div>

<br/>
<div align="center">
<img width="100%" src="https://raw.githubusercontent.com/therealruthvik/therealruthvik/projects/projects.svg" alt="Projects" />
</div>

<!-- ===== SOCIAL BADGES ===== -->
<br/>
<div align="center">

<a href="https://www.linkedin.com/in/ruthvikg31/">
  <img src="https://img.shields.io/badge/LinkedIn-0A101F?style=for-the-badge&logo=linkedin&logoColor=38BDF8&labelColor=0A101F" alt="LinkedIn" />
</a>
&nbsp;&nbsp;
<a href="https://github.com/therealruthvik">
  <img src="https://img.shields.io/badge/GitHub-0A101F?style=for-the-badge&logo=github&logoColor=white&labelColor=0A101F" alt="GitHub" />
</a>
&nbsp;&nbsp;
<a href="https://leetcode.com/ruthvikg31/">
  <img src="https://img.shields.io/badge/LeetCode-0A101F?style=for-the-badge&logo=leetcode&logoColor=10B981&labelColor=0A101F" alt="LeetCode" />
</a>
&nbsp;&nbsp;
<a href="mailto:ruthvik.garla@gmail.com">
  <img src="https://img.shields.io/badge/Email-0A101F?style=for-the-badge&logo=gmail&logoColor=A78BFA&labelColor=0A101F" alt="Email" />
</a>

</div>

<!-- =================================== -->

---

## About

I build reliability-minded AI/ML infrastructure: Kubernetes platforms for GPU workloads, durable orchestration systems, GitOps delivery paths, and policy controls that make production changes observable and reversible. My work sits at the intersection of AI serving, SRE, distributed systems durability, and Kubernetes governance, with a bias toward systems that keep operating through failed workers, bad rollouts, SLO breaches, and unsafe deploys.

Currently, I am a Software Engineer (external consultant) at **Nestle**, shipping ArgoCD-driven release pipelines on AKS. Previously, I worked as a DevOps Engineer Intern at **SAP** and as a Graduate Teaching Assistant for Cloud Computing at **Northeastern University**.

## Skills Matrix

| Area | Production Tools & Systems |
| --- | --- |
| **Kubernetes & Cloud** | Kubernetes, AKS, EKS, k3s/k3d, kind, Helm, Terraform, Docker, Linux, Tailscale, Calico |
| **AI/ML Infrastructure** | vLLM, NVIDIA Triton, Modal GPUs, NVIDIA NIM, NeMo Guardrails, MLflow, MinIO, HuggingFace Transformers |
| **SRE & Observability** | Prometheus, Grafana, AlertManager, OpenTelemetry, DCGM Exporter, Locust, SLO burn-rate alerts |
| **GitOps & Policy** | ArgoCD, Kyverno, Cosign, Sigstore/Rekor, NGINX Ingress canaries, GitHub Actions |
| **Durable Systems** | Temporal workflows, saga compensation, worker crash recovery, audit logs, approval gates |
| **Languages** | Go, Python, JavaScript/TypeScript, Java, C/C++, Shell |

---

## Featured Systems

### Durable Orchestration & Safety-Critical Pipelines

#### [temporalops](https://github.com/therealruthvik/temporalops) - Self-Healing Kubernetes Canary Orchestrator

Progressive deploy/rollback controller built as a durable Temporal workflow over real Kubernetes APIs.

- **Core design:** Runs a canary release through Kyverno policy dry-run, canary scale-up, health bake, replica-ratio traffic shift, human approval, and promotion. Multi-service releases fan out as child workflows and write append-only audit events tagged by workflow, run, actor, and timestamp.
- **Fault tolerance / SRE focus:** Uses hand-written LIFO saga compensation for rollback on health failure, traffic-shift failure, rejection, or approval timeout. Worker crash tests prove the workflow resumes from the last completed step without duplicating side effects, while Temporal SDK metrics feed Prometheus and Grafana.
- **Stack:** `Go` | `Temporal SDK` | `Kubernetes client-go` | `Kyverno` | `Prometheus` | `Grafana` | `SQLite` | `kind`

#### [perception-sentinel](https://github.com/therealruthvik/perception-sentinel) - Fault-Tolerant AV Perception Pipeline

Safety-critical autonomous-vehicle perception demo with GPU inference, chaos injection, SLO monitoring, and LLM fallback.

- **Core design:** Replays synthetic CARLA data into YOLOv8n running at 20 Hz on Modal T4 GPUs, streams detections over WebSockets, and routes degraded states into a local fallback/control plane.
- **Fault tolerance / SRE focus:** A custom watchdog tracks rolling p99 latency against a 40 ms SLO and triggers fallback after three consecutive breaches. The chaos proxy injects blackouts, frame drops, corrupt frames, and p99 inflation; fallback uses NVIDIA NIM with NeMo Guardrails before handing control to a rate-limited FastAPI arbiter.
- **Stack:** `Python` | `FastAPI` | `Modal T4 GPU` | `YOLOv8n` | `NVIDIA NIM` | `NeMo Guardrails` | `Prometheus` | `Grafana` | `Docker`

### Kubernetes Governance & GitOps

#### [kyvernoproject](https://github.com/therealruthvik/kyvernoproject) - Kubernetes Policy Suite

Cluster-wide Kyverno admission controls for security, compliance, and operational guardrails.

- **Core design:** Organizes policies into validate, mutate, generate, and image-verify domains. Validation blocks privileged containers, host namespaces, missing resource limits, and unapproved registries; mutation injects labels, security contexts, and image pull policies; generation creates default NetworkPolicies and ResourceQuotas.
- **Fault tolerance / SRE focus:** Moves safety checks to admission time so bad workloads fail before storage. Kyverno CLI tests validate pass/fail resources offline, while policy reports give cluster operators a post-admission compliance surface.
- **Stack:** `Kyverno` | `Kubernetes YAML` | `Cosign` | `Sigstore/Rekor` | `Helm` | `Shell`

#### [hybrid-gpu-infra](https://github.com/therealruthvik/hybrid-gpu-infra) - Hybrid GPU Kubernetes Cluster

Two-node Kubernetes architecture spanning an AWS control plane and Lambda Labs A10 GPU worker over a private Tailscale mesh.

- **Core design:** Runs kubeadm Kubernetes with an AWS t2.micro control plane and Lambda Labs A10 GPU node, connected through WireGuard-backed Tailscale networking. The cluster hosts vLLM Mistral-7B-AWQ inference, ArgoCD, Kyverno, Prometheus, Grafana, GPU Operator components, and DCGM metrics.
- **Fault tolerance / SRE focus:** Separates control-plane and GPU-worker responsibilities with taints, labels, and VPN-only inter-node traffic. GitOps owns workload drift correction, Kyverno enforces policy, and GPU telemetry is scraped continuously for platform health.
- **Stack:** `Kubernetes` | `kubeadm` | `AWS EC2` | `Lambda Labs A10` | `Tailscale` | `vLLM` | `ArgoCD` | `Kyverno` | `Prometheus` | `Grafana`

#### [mlops-llm-pipeline](https://github.com/therealruthvik/mlops-llm-pipeline) - GitOps LLM Delivery Pipeline

End-to-end MLOps pipeline for model training, artifact storage, containerization, canary deploys, and live monitoring.

- **Core design:** Trains and promotes a DistilGPT2 model through MLflow and MinIO, builds a FastAPI inference server, packages it with Helm, and lets ArgoCD reconcile the release into a kind cluster.
- **Fault tolerance / SRE focus:** Uses NGINX Ingress canary routing to shift from 10 percent to full rollout only after validation. Prometheus and Grafana expose serving metrics so rollout decisions are tied to measured behavior, not blind deploy success.
- **Stack:** `Python` | `FastAPI` | `Transformers` | `MLflow` | `MinIO` | `Docker` | `Helm` | `ArgoCD` | `NGINX Ingress` | `Prometheus`

### Infrastructure Performance & Reliability Tooling

#### [riskdiff](https://github.com/therealruthvik/riskdiff) - Offline Pre-Commit Risk Scanner

Deterministic guardrail for risky git diffs, designed to catch AI-code failure patterns before review.

- **Core design:** Scans staged or branch-based git diffs locally, scores heuristic signals, and emits text, JSON, SARIF, or Markdown reports with specific one-line remediation advice.
- **Fault tolerance / SRE focus:** Runs with no network, telemetry, backend, account, or LLM dependency, making it safe for private codebases. Threshold-based exits support pre-commit hooks and GitHub Actions, while baselines allow teams to grandfather existing findings without losing enforcement on new risk.
- **Stack:** `JavaScript` | `Node.js >= 18` | `Git CLI` | `SARIF` | `GitHub Actions` | zero npm runtime dependencies

#### [sentinalflow](https://github.com/therealruthvik/sentinalflow) - Multi-Tenant SLO Observability Platform

Local, production-shaped observability stack for tenant metrics, streaming aggregation, alerting, and rollback automation.

- **Core design:** Streams tenant metrics and logs through Redpanda, aggregates one-minute SLO windows in Spark Structured Streaming, writes Parquet to LocalStack S3, and bridges SLO aggregates into Prometheus.
- **Fault tolerance / SRE focus:** Models error-rate, latency, and fast-burn alerts with AlertManager, then connects critical SLO breaches to an ArgoCD rollback webhook. ApplicationSets manage tenant namespaces, RBAC, NetworkPolicies, and HPAs with GitOps self-healing.
- **Stack:** `Python` | `Redpanda/Kafka` | `Spark Structured Streaming` | `LocalStack` | `Terraform` | `k3d` | `Prometheus` | `AlertManager` | `Grafana` | `ArgoCD`

#### [inference-platform](https://github.com/therealruthvik/inference-platform) - vLLM vs NVIDIA Triton Benchmark Platform

GPU inference benchmarking environment comparing throughput, latency, and autoscaling behavior across serving engines.

- **Core design:** Runs vLLM and NVIDIA Triton side-by-side on a Lambda Labs A10 VM with TinyLlama-1.1B, using k3s, PVC-backed model caches, Prometheus scraping, and Locust load generation.
- **Fault tolerance / SRE focus:** KEDA ScaledObjects autoscale each engine from one to five replicas based on queue depth, pending requests, p99 latency, and average queue wait. Grafana dashboards and load-test artifacts make performance regressions visible.
- **Stack:** `k3s` | `vLLM` | `NVIDIA Triton 23.10` | `KEDA` | `Prometheus` | `Grafana` | `Locust` | `TinyLlama` | `Lambda Labs A10`

#### [dgxclone](https://github.com/therealruthvik/dgxclone) - Self-Hosted GPU Job Platform

Run:AI-style GPU workload portal for submitting containerized jobs, streaming logs, and monitoring GPU utilization on Kubernetes.

- **Core design:** Next.js UI talks to a FastAPI backend, queues work in Redis/RQ, and launches Kubernetes Jobs on GPU nodes. The backend streams live job logs over SSE while DCGM Exporter feeds GPU metrics into Prometheus and Grafana.
- **Fault tolerance / SRE focus:** Separates request handling, queue state, and job execution so submitted workloads survive frontend/API restarts. Helm deployment, ingress routing, and GPU visibility checks make the platform reproducible on a fresh NVIDIA VM.
- **Stack:** `Next.js 14` | `FastAPI` | `Redis` | `RQ` | `Kubernetes Jobs` | `Helm` | `NVIDIA Device Plugin` | `DCGM Exporter` | `Prometheus` | `Grafana`

---

## Certifications & Education

| Certification | Issuer | Verification |
| --- | --- | --- |
| Certified Kubernetes Administrator (CKA) | CNCF / Linux Foundation | [Credential](https://www.credly.com/badges/8067d292-b8aa-4a86-ad16-5ae29a99553d) |
| Terraform Associate | HashiCorp | [Credential](https://www.credly.com/badges/fcbb30be-aed9-4bb8-9b42-15f1db4c0da1/linked_in_profile) |
| Azure Fundamentals | Microsoft | [Credential](https://learn.microsoft.com/en-in/users/ruthvikgarlapati-8692/credentials/3831ce1f37da4222) |
| AI Infrastructure & Operations Associate | NVIDIA | [Credential](https://www.credly.com/badges/56edd9a6-3553-4748-abc1-b2cde77feeae/public_url) |
| Certified System Administrator | ServiceNow | Credential available through ServiceNow certification profile |

| Education | Program | Location |
| --- | --- | --- |
| [Northeastern University](https://www.northeastern.edu/) | M.S. in Information Systems, GPA 3.9 | Boston, MA |
| [Jawaharlal Nehru Technological University](https://jntuh.ac.in/) | B.Tech in Computer Science | Hyderabad, India |
