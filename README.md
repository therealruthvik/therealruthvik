# Hi, I'm Ruthvik 👋

I build and operate **AI/ML infrastructure on Kubernetes** — GPU clusters, LLM inference platforms, and the GitOps pipelines that ship them. Currently a Software Engineer at Nestle (external consultant) shipping ArgoCD-driven release pipelines on AKS. Previously DevOps Engineer Intern at SAP and Graduate TA for Cloud Computing at Northeastern.

📍 Seattle, WA &nbsp;•&nbsp; 🎯 Site Reliability Engineering, with a focus on AI/ML workloads &nbsp;•&nbsp; ☸ CKA-certified

---

## What I work on

I treat operations as a software problem. Most of what I build sits at the intersection of three things: **distributed systems on Kubernetes**, **GPU/LLM serving stacks**, and **the observability + automation that keeps them up**.

If you're curious what that looks like in practice, the projects below are the best window in.

---

## Featured projects

### 🚀 [inference-platform](https://github.com/therealruthvik/inference-platform) — vLLM vs Triton, side by side
Benchmarking platform that runs **vLLM** and **NVIDIA Triton Inference Server** on the same Lambda Labs A10 GPU VM, both serving TinyLlama-1.1B. **KEDA** autoscales each engine (1–5 replicas) based on Prometheus queue-depth metrics. Locust drives load. Compares throughput, latency, and autoscaling behavior between the two.
> `k3s` `vLLM` `Triton` `KEDA` `Prometheus` `Grafana` `Locust`

### ☁️ [gpu-k8s-lab](https://github.com/therealruthvik/gpu-k8s-lab) — Terraform-provisioned GPU clusters on AWS
Two-phase GPU Kubernetes lab: **Phase 1** is bare GPU access on k3s on a single spot EC2 instance; **Phase 2** is managed EKS running **Llama-3.1-8B via vLLM** with full observability (NVIDIA GPU Operator, DCGM exporter, Prometheus, Grafana). Spot pricing keeps it ~$0.16–$0.29/hr.
> `Terraform` `AWS` `EKS` `vLLM` `Llama-3.1-8B` `DCGM` `Prometheus`

### 🔁 [mlops-llm-pipeline](https://github.com/therealruthvik/mlops-llm-pipeline) — End-to-end GitOps for LLM inference
Production-style MLOps pipeline covering the full model lifecycle: **MLflow** experiment tracking with MinIO artifact storage, FastAPI/Docker inference server, Helm packaging, **ArgoCD** GitOps deploys, **NGINX Ingress canary** traffic splitting (10% → full rollout), and Prometheus + Grafana observability.
> `MLflow` `ArgoCD` `Helm` `NGINX` `FastAPI` `Canary deploys`

### 🖥️ [dgxclone](https://github.com/therealruthvik/dgxclone) — Self-hosted GPU job scheduler (RUN:ai-style)
Submit Docker-based AI workloads to a GPU cluster, stream live logs via SSE, and watch GPU utilization in Grafana. Next.js frontend, FastAPI backend, Redis-backed RQ worker that creates Kubernetes Jobs for GPU pods. Packaged as a single Helm chart.
> `k3s` `FastAPI` `Next.js` `Redis/RQ` `NVIDIA device plugin` `DCGM` `SSE` `Helm`

### 📚 [sre-runbook-generator](https://github.com/therealruthvik/sre-runbook-generator) — RAG over postmortems
LLM-powered runbook generator that turns Prometheus alerts into structured runbooks. Alertmanager → API Gateway → AWS Lambda. Uses **ChromaDB + sentence-transformers** for local retrieval over past postmortems (zero embedding API cost), and the Anthropic Claude API for generation. Optional ServiceNow ticket creation.
> `Claude API` `ChromaDB` `RAG` `AWS Lambda` `Prometheus` `ServiceNow`

### ☸ [k8s-ai-agent](https://github.com/therealruthvik/k8s-ai-agent) — Plain English → kubectl
CLI agent that translates natural-language requests into kubectl commands and YAML manifests. Full CRUD for every major Kubernetes resource (Deployments, Services, Ingress, RBAC, CRDs). Per-step **confirm/refine loop**, prerequisite ordering, dry-run mode, and per-step risk scoring before execution.
> `Claude API` `kubectl` `Python` `Interactive REPL`

### 🧪 [neural-inference-server](https://github.com/therealruthvik/neural-inference-server) — Pure-Python inference over JSON/HTTP
Bazel-managed two-layer dense network (ReLU → softmax) exposed over JSON/HTTP, with a **proto-defined service contract** that mirrors gRPC stub interfaces for drop-in replacement. Includes a typed client SDK and latency benchmark target. Companion C++ matrix-ops library (matmul/ReLU/softmax) is the planned CUDA acceleration path.
> `Bazel` `Protocol Buffers` `Python` `C++ kernels`

---

## Stack I work with

**Distributed systems & cloud:** Kubernetes (CKA), AWS (EKS, EC2, Lambda), Azure (AKS, ACR), GCP, Terraform, Helm
**AI/ML infra:** vLLM, Triton Inference Server, KEDA, NVIDIA DCGM, MLflow, GPU workload orchestration on k8s
**Reliability & observability:** Prometheus, Grafana, OpenTelemetry, ELK, SumoLogic, ServiceNow, ArgoCD, Istio, Velero, Kyverno
**Languages:** Python, Java, C/C++, Node.js (and a couple of Go and Rust repos here while I learn)
**Linux & systems:** Linux administration, container runtime debugging, Bazel hermetic builds, NGINX, Docker

---

## Certifications

- ☸ **Certified Kubernetes Administrator (CKA)** — [credential](https://www.credly.com/badges/8067d292-b8aa-4a86-ad16-5ae29a99553d)
- 🔧 **HashiCorp Terraform Associate** — [credential](https://www.credly.com/badges/fcbb30be-aed9-4bb8-9b42-15f1db4c0da1/linked_in_profile)
- ☁️ **Microsoft Azure Fundamentals** — [credential](https://learn.microsoft.com/en-in/users/ruthvikgarlapati-8692/credentials/3831ce1f37da4222)
- 🛠️ **ServiceNow Administrator**
- 🎯 **NVIDIA Certified Associate — AI Infrastructure & Operations (NCA-AIIO)** — *in progress*

---

## Education

**Northeastern University** — M.S., Information Systems &nbsp;•&nbsp; GPA 3.9 &nbsp;•&nbsp; Boston, MA &nbsp;•&nbsp; May 2024
*Coursework:* Advanced Cloud Computing, Network Structures & Cloud Computing, Data Structures and Algorithms

**Jawaharlal Nehru Technological University** — B.Tech, Computer Science &nbsp;•&nbsp; Hyderabad, India
*Coursework:* Database Management, Operating Systems, Software Engineering

---

## Let's connect

📫 [ruthvik.garla@gmail.com](mailto:ruthvik.garla@gmail.com) &nbsp;•&nbsp; 💼 [LinkedIn](https://www.linkedin.com/in/ruthvikg31/) &nbsp;•&nbsp; 🧮 [LeetCode](https://leetcode.com/ruthvikg31/)

If you're building AI/ML infrastructure or hiring for an SRE role on a team that does — I'd love to talk.
