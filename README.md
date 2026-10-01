# MLOps Roadmap

A beginner-friendly path from your first Linux command to running ML models
and LLMs in production, one tool at a time.

I'm Manoj, a DevOps engineer working toward MLOps, and I'm learning in public.
I teach the ops side from experience; the ML side I'm learning alongside you.
Every tool gets videos on [YouTube](https://www.youtube.com/@codewithmanojx)
and its own repo with notes and code.

## Where to start

- **New to all of this?** Start at Stage 1.
- **Already working in DevOps or cloud?** Skip to Stage 2.

## What MLOps is

MLOps applies DevOps practices to machine learning. The difference: an ML
system depends on code, data *and* a trained model, and the model gets worse
as real-world data changes. So the lifecycle is a loop:

```
data → train → track → package → deploy → monitor → retrain
```

## The roadmap

One tool per category. Each tool links to its repo once that stage starts.

### Stage 1: Foundations

| Tool | Why it's here | Repo |
|---|---|---|
| Linux | Every server, container and cluster runs on it. Includes Bash and networking basics. | Planned |
| Git | Code, infrastructure and pipelines are all versioned. | Planned |
| Python | The language of ML and of most MLOps tools. | Planned |
| Docker | Packages an app and its dependencies, models included, so it runs the same everywhere. | Planned |
| Kubernetes | Runs containers at scale. Kubeflow and KServe run on top of it. | Planned |
| GitHub Actions | Automates testing, building and deploying. | Planned |
| Azure basics | Where everything runs: subscriptions, resource groups, identity, storage, ACR, AKS. | Planned |
| Terraform | Builds that Azure setup as code. | Planned |

### Stage 2: ML foundations

| Tool | Why it's here | Repo |
|---|---|---|
| pandas | Load, clean and explore data. | Planned |
| scikit-learn | Train and evaluate classic models: enough ML to understand what you're operating. | Planned |

### Stage 3: Core MLOps

| Tool | Why it's here | Repo |
|---|---|---|
| MLflow | Track experiments and register model versions. | Planned |
| DVC | Version datasets and models alongside Git. | Planned |
| FastAPI | Put a model behind an HTTP API. | Planned |

### Stage 4: Cloud ML

| Tool | Why it's here | Repo |
|---|---|---|
| Azure ML | The managed, all-in-one version of Stage 3 on Azure. | Planned |

### Stage 5: ML on Kubernetes

| Tool | Why it's here | Repo |
|---|---|---|
| Kubeflow Pipelines | Turn the ML steps into a repeatable pipeline on Kubernetes. | Planned |
| KServe | Serve models on Kubernetes with autoscaling. | Planned |

### Stage 6: Monitoring

| Tool | Why it's here | Repo |
|---|---|---|
| Evidently AI | Detect data drift and quality drops, which tells you when to retrain. | Planned |

### Stage 7: LLMOps

| Tool | Why it's here | Repo |
|---|---|---|
| Ollama | Run open models locally. | Planned |
| vLLM | Serve LLMs in production. | Planned |
| LlamaIndex | Connect an LLM to your own data (RAG). | Planned |
| Langfuse | Trace, evaluate and track the cost of LLM calls. | Planned |

## Notes on tool choices

- **CI/CD:** GitHub Actions is free for public repos and lives next to the
  code. Azure DevOps Pipelines is the common enterprise alternative; the
  concepts carry over.
- **Infrastructure as code:** Terraform is the industry default. Its license
  is no longer open source; [OpenTofu](https://opentofu.org) is the
  open-source fork, created from Terraform 1.5.
- **Kubernetes** goes deeper than the other tools, aligned with the CKA exam.
- **Kubeflow** means Kubeflow Pipelines on a local `kind` cluster, not a full
  Kubeflow install.

## Not on this roadmap, on purpose

Feature stores, training deep learning models, multiple clouds, and
alternatives to each tool. One tool per category, covered properly.

## How the series works

- Each `learn-<tool>` repo stands on its own: clone only the one you need.
- Videos come out weekly during Stage 1 and every two weeks from Stage 2.
  No dates promised.

## License

- Code: [MIT](LICENSE)
- Notes and docs: [CC BY 4.0](LICENSE-docs)
