<div align="center">
  <h1>Ruthvik Garlapati</h1>
  <p><b>Software Engineer (AI/ML Infra & Kubernetes SRE)</b></p>
  <p>📍 Seattle, WA &nbsp;•&nbsp; ☸️ CKA-Certified &nbsp;•&nbsp; ✉️ <a href="mailto:ruthvik.garla@gmail.com">ruthvik.garla@gmail.com</a></p>
  <p>
    <a href="https://www.linkedin.com/in/ruthvikg31/"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
    <a href="https://github.com/therealruthvik"><img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub"></a>
    <a href="https://leetcode.com/ruthvikg31/"><img src="https://img.shields.io/badge/LeetCode-FFA116?style=flat-square&logo=leetcode&logoColor=black" alt="LeetCode"></a>
  </p>
</div>

---

### 💫 About Me

I build and operate **AI/ML infrastructure on Kubernetes** — GPU clusters, LLM inference platforms, and the GitOps pipelines that ship them. I treat infrastructure and operations as software engineering problems, focusing on **distributed systems durability**, **safety policies**, and **automated observability**.

Currently, I am a Software Engineer (external consultant) at **Nestle**, shipping ArgoCD-driven release pipelines on AKS. Previously, I was a DevOps Engineer Intern at **SAP** and a Graduate TA for Cloud Computing at **Northeastern University**.

---

### 🛠️ Technical Stack

| Category | Technologies |
| :--- | :--- |
| **Cloud & Orchestration** | Kubernetes (CKA), Go (`client-go`), Temporal, Terraform, Helm, Docker, AKS, EKS, GCP, Linux Systems |
| **AI/ML & Serving Infra** | vLLM, NVIDIA Triton, NVIDIA GPU Operator, DCGM Exporter, Modal, NVIDIA NIM, MLflow, MinIO |
| **SRE, GitOps & Security**| Prometheus, Grafana, OpenTelemetry, Kyverno, ArgoCD, Cosign, NGINX Ingress, ServiceNow |
| **Languages** | Go, Python, JavaScript/TypeScript, Java, C/C++, Shell |

---

## 🚀 Featured Projects

### ⚙️ Durable Orchestration & Safety-Critical Pipelines

#### 🔗 [temporalops](https://github.com/therealruthvik/temporalops) — Self-Healing Canary Release Orchestrator
*A progressive canary deployer and rollback manager running as a durable Temporal workflow.*
- **Core Design:** Implements dry-run policy gating via Kyverno, replica scaling, bake stages, traffic splitting, and human approval gates.
- **Fault Tolerance:** Uses a hand-written LIFO Saga compensation pattern for automatic rollbacks on telemetry failures or gate timeouts. Worker crashes mid-deploy resume from the last completed stage with no duplicate side effects.
- **Stack:** `Go` • `Temporal SDK` • `Kubernetes API (client-go)` • `Kyverno` • `Prometheus` • `SQLite`

#### 🛡️ [perception-sentinel](https://github.com/therealruthvik/perception-sentinel) — Fault-Tolerant AV Perception Pipeline
*Real-time autonomous vehicle perception stream with LLM-augmented fallback mechanisms and production-grade SLO tracking.*
- **Core Design:** YOLOv8n object detection running at 20 Hz on Modal GPUs, automatically failing over to Nemotron-550B (via NVIDIA NIM) with NeMo Guardrails upon watchdog alert.
- **SRE Focus:** Features an in-path chaos proxy for fault injection, rolling p99 latency watchdog metrics, and full Prometheus/Grafana dashboarding for SLO compliance.
- **Stack:** `Python` • `Modal (T4 GPU)` • `NVIDIA NIM` • `NeMo Guardrails` • `Prometheus` • `Docker`

#### 🤖 [k8s-ai-agent](https://github.com/therealruthvik/k8s-ai-agent) — Natural Language to kubectl Interpreter
*Interactive CLI agent translating plain English requests into dry-run validated Kubernetes YAML manifests.*
- **Core Design:** Multi-step prompt builder with safety dry-runs, topological sort for resource creation (e.g. namespaces before deployments), and risk score checks using Claude.
- **Stack:** `Python` • `Anthropic Claude API` • `kubectl` • `Docker`

---

### ☸️ Kubernetes Governance, Security & GitOps

#### 🛡️ [kyvernoproject](https://github.com/therealruthvik/kyvernoproject) — Cluster Security & Governance Policies
*Production-grade Kubernetes admission control rules for cluster-wide enforcement of security and operational compliance.*
- **Core Design:** Implements validation (blocking privileged containers, host namespaces, and unapproved registries), mutation (default resource injects), and Cosign signature verification.
- **Validation:** Automated test-harness using `kyverno` CLI validating resource pass/fail metrics.
- **Stack:** `Kyverno Policies (YAML)` • `Cosign` • `Helm` • `Shell`

#### 🔄 [mlops-llm-pipeline](https://github.com/therealruthvik/mlops-llm-pipeline) — End-to-End GitOps for LLM Inference
*Continuous delivery pipeline implementing automated canary releases and traffic splitting for FastAPI inference servers.*
- **Core Design:** MLflow experiment tracking with MinIO backend, Helm-packaged app, ArgoCD deployment, and NGINX Ingress canary routing (10% to 100% rollout) triggered by performance metrics.
- **Stack:** `ArgoCD` • `Helm` • `FastAPI` • `MLflow` • `MinIO` • `NGINX Ingress` • `Prometheus`

---

### 📊 Infrastructure Performance & Tooling

#### 🔍 [riskdiff](https://github.com/therealruthvik/riskdiff) — Pre-Commit Git Diff Risk Scanner
*A lightning-fast, zero-dependency, local pre-commit hook targeting AI-generated code pattern smells.*
- **Core Design:** Scrapes staged git diffs to calculate risk scores based on heuristics (undocumented calls, swallowed exceptions, secret leakage, missing tests).
- **User Experience:** Fully offline, outputs reports in JSON, SARIF, or Markdown, recommending specific code-level corrections.
- **Stack:** `JavaScript` • `Node.js` • `Git CLI` (Zero npm dependencies)

#### ⚡ [inference-platform](https://github.com/therealruthvik/inference-platform) — Triton vs vLLM Serving Benchmarks
*Side-by-side performance benchmarking framework comparing LLM inference engines on Lambda Labs A10 GPUs.*
- **Core Design:** Serves TinyLlama-1.1B through both vLLM and NVIDIA Triton, using KEDA to autoscale deployments based on Prometheus queue-depth telemetry under load from Locust.
- **Stack:** `Kubernetes` • `vLLM` • `NVIDIA Triton` • `KEDA` • `Prometheus` • `Locust` • `Grafana`

#### 🖥️ [dgxclone](https://github.com/therealruthvik/dgxclone) — Multi-Tenant GPU Workload Scheduler
*Self-hosted job runner scheduling containerized ML workloads across a private GPU cluster (Run:AI style).*
- **Core Design:** Next.js UI submitting tasks to a FastAPI backend, executing Kubernetes Jobs via Redis/RQ queue worker, with live Server-Sent Events (SSE) logs.
- **Stack:** `Next.js` • `FastAPI` • `Redis / RQ` • `NVIDIA Device Plugin` • `DCGM Exporter`

---

## 📜 Certifications & Education

### Certifications
- ☸️ **Certified Kubernetes Administrator (CKA)** — [Verify Badge](https://www.credly.com/badges/8067d292-b8aa-4a86-ad16-5ae29a99553d)
- 🔧 **HashiCorp Certified: Terraform Associate** — [Verify Badge](https://www.credly.com/badges/fcbb30be-aed9-4bb8-9b42-15f1db4c0da1/linked_in_profile)
- ☁️ **Microsoft Certified: Azure Fundamentals** — [Verify Badge](https://learn.microsoft.com/en-in/users/ruthvikgarlapati-8692/credentials/3831ce1f37da4222)
- 🛠️ **ServiceNow Certified System Administrator**
- 🎯 **NVIDIA Certified Associate: AI Infrastructure & Operations** — [Verify Badge](https://www.credly.com/badges/56edd9a6-3553-4748-abc1-b2cde77feeae/public_url)

### Education
- **Northeastern University** — M.S. in Information Systems (GPA: 3.9) &nbsp;•&nbsp; *Boston, MA*
- **Jawaharlal Nehru Technological University** — B.Tech in Computer Science &nbsp;•&nbsp; *Hyderabad, India*
