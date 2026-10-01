# MLOps Roadmap

A beginner-friendly path from your first Linux command to running ML models
and LLMs in production, one tool at a time.

I'm Manoj, a DevOps engineer working toward MLOps, and I'm learning in public.
The ops side I know from experience; the ML side I'm learning from scratch.
Notes and code for each tool go in their own repo, and some topics get videos
on [YouTube](https://www.youtube.com/@codewithmanojx).

## Where to start

- **New to all of this?** Start at Phase 0.
- **Already working in DevOps or cloud?** Skip to Phase 1.

## What MLOps is

MLOps applies DevOps practices to machine learning. The difference: an ML
system depends on code, data *and* a trained model, and the model gets worse
as real-world data changes. So the lifecycle is a loop:

```
data → train → track → package → deploy → monitor → retrain
```

## The roadmap

One tool per category. Open source first, Azure as the cloud. Each row links
to its repo once that topic starts.

### Phase 0: Foundations

| Category | Tool | Repo |
|---|---|---|
| OS & scripting | Linux, Bash (plus networking basics) | Planned |
| Version control | Git + GitHub | Planned |
| Language | Python (uv for environments and packaging) | Planned |
| Containers | Docker | Planned |
| Orchestration | Kubernetes (kind locally, AKS in the cloud) | Planned |
| CI/CD | GitHub Actions | Planned |
| Infrastructure as code | Terraform | Planned |
| Cloud | Azure | Planned |

### Phase 1: ML Fundamentals

| Category | Tool | Repo |
|---|---|---|
| Notebooks | Jupyter | Planned |
| Data handling | NumPy, pandas | Planned |
| Classic ML | scikit-learn | Planned |
| Visualisation | matplotlib | Planned |
| Deep learning (intro only) | PyTorch | Planned |

### Phase 2: MLOps Core

| Category | Tool | Repo |
|---|---|---|
| Experiment tracking + model registry | MLflow | Planned |
| Data versioning | DVC | Planned |
| Model as an API | FastAPI | Planned |
| Testing | pytest | Planned |

### Phase 3: Pipelines & Orchestration

| Category | Tool | Repo |
|---|---|---|
| ML pipelines | Kubeflow Pipelines | Planned |

### Phase 4: Model Serving

| Category | Tool | Repo |
|---|---|---|
| Simple serving | FastAPI in Docker | Planned |
| Kubernetes-native serving | KServe | Planned |

### Phase 5: Monitoring

| Category | Tool | Repo |
|---|---|---|
| Data & model drift | Evidently AI | Planned |
| System metrics | Prometheus + Grafana | Planned |

### Phase 6: LLMOps

| Category | Tool | Repo |
|---|---|---|
| Run LLMs locally | Ollama | Planned |
| Production LLM serving | vLLM | Planned |
| RAG | LlamaIndex | Planned |
| LLM observability & evals | Langfuse | Planned |

### Azure module

Where it all runs in the cloud, covered as its own section:
Azure ML · AKS · Azure Container Registry · Blob Storage · Key Vault

## Notes on tool choices

- **CI/CD:** GitHub Actions is free for public repos and lives next to the
  code.
- **Infrastructure as code:** Terraform is the industry default. Its license
  is no longer open source; [OpenTofu](https://opentofu.org) is the
  open-source fork, created from Terraform 1.5.
- **Kubernetes** goes deeper than the other foundations, aligned with the CKA
  exam.
- **Kubeflow** means Kubeflow Pipelines on a local `kind` cluster, not a full
  Kubeflow install.
- **PyTorch** is an introduction only: enough to understand and operate deep
  learning models, not to research them.

## Mentioned, not taught

Good tools, deliberately left out so each category gets one tool covered
properly. The concepts carry over.

| Category | Tools |
|---|---|
| CI/CD | Azure DevOps Pipelines |
| Orchestration | Airflow, Prefect |
| Experiment tracking | Weights & Biases |
| Serving | BentoML, Seldon |
| Feature store | Feast |
| Other clouds | SageMaker, Vertex AI |

## How to use the repos

Each `learn-<tool>` repo stands on its own: clone only the one you need. New
repos appear as I reach each topic, so there are no dates.

## License

- Code: [MIT](LICENSE)
- Notes and docs: [CC BY 4.0](LICENSE-docs)
