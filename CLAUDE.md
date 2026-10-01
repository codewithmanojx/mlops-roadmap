# CLAUDE.md

Guidance for Claude Code in this repository.

## What this is

The hub of codewithmanojx's learn-in-public path into MLOps. Manoj, a DevOps
engineer, revises the foundations, learns ML and MLOps one tool at a time,
teaches each on YouTube (https://www.youtube.com/@codewithmanojx), and
publishes one public repo per tool.

- This repo (`mlops-roadmap`): the roadmap, plus links to every tool repo.
- Tool repos: `learn-<tool>` (e.g. `learn-docker`, `learn-mlflow`), one per
  tool, siblings of this repo. Each is created only when that tool starts.

## Audience

Beginner-friendly. Stage 1 assumes no prior experience. DevOps and cloud
engineers who already know the foundations skip to Stage 2.

## Roadmap

| Stage | Tools |
|---|---|
| 1. Foundations | Linux (with Bash and networking basics), Git, Python, Docker, Kubernetes, GitHub Actions, Azure basics, Terraform |
| 2. ML foundations | pandas, scikit-learn |
| 3. Core MLOps | MLflow, DVC, FastAPI |
| 4. Cloud ML | Azure ML |
| 5. ML on Kubernetes | Kubeflow Pipelines, KServe |
| 6. Monitoring | Evidently AI |
| 7. LLMOps | Ollama, vLLM, LlamaIndex, Langfuse |

Status: tool list and order agreed; public roadmap in README.md. Video 1
talk track drafted in conversation, not saved. Open: whether one project runs
through the whole series or each tool repo stands alone.

## Conventions

- One tool per category. Open source first; exceptions are in the decision log.
- Azure is the cloud. Azure ML gets its own section.
- CI/CD is GitHub Actions. Azure DevOps Pipelines is mentioned once as the
  enterprise alternative; nothing is built in it.
- Kubernetes goes deep, structured around the current CKA curriculum. Check
  the official curriculum when that stage starts; it gets revised.
- Networking basics live in `learn-linux`, not in a repo of their own.
- Kubeflow means Kubeflow Pipelines standalone on a local `kind` cluster, not
  a full Kubeflow install.
- Tool repos use role-neutral wording: the tools are for anyone, not only DevOps.
- Every repo has README.md, CLAUDE.md (committed, self-contained), .gitignore,
  LICENSE (MIT, code) and LICENSE-docs (CC BY 4.0, notes and docs). The README
  states the license split. CLAUDE.local.md is optional and gitignored.
- Never commit secrets, Terraform state, MLflow runs, DVC cache or model files.
- README.md here is the public roadmap. When a `learn-<tool>` repo is created,
  replace that tool's "Planned" with a link to the repo.
- Copyright holder in LICENSE files: "Manoj Kumar (codewithmanojx)".

## Working in this repo

- Concise and technically precise. Push back on over-engineering.
- Ask before creating files.
- Record every decision in the log below, so the next session picks up where
  this one left off.

## Helping learners

If a student is working here, explain the concept and give hints before
handing over a full solution. Point to each tool's official docs.

## Publishing

- Weekly while the foundation videos are short. One every two weeks once the
  ML stages start, since those are learned from scratch.
- Batch-record 2–3 videos before publishing the first.
- Video 1: MLOps roadmap explainer, ~12–15 min, screen share + webcam, raw
  with simple cuts.

## Decision log

| Date | Decision |
|---|---|
| 2026-10-01 | Goal: become an MLOps engineer, learning in public. Hub `mlops-roadmap`; tool repos `learn-<tool>`, all directly in the workspace root. |
| 2026-10-01 | Licenses: MIT for code (LICENSE), CC BY 4.0 for notes and docs (LICENSE-docs). |
| 2026-10-01 | Beginner-friendly: foundations are taught as short videos; experienced engineers skip to Stage 2. |
| 2026-10-01 | Open source first, Azure as the cloud, one tool per category. |
| 2026-10-01 | Python sits in Stage 1, so one Python app can run through Docker and later become the FastAPI model server. |
| 2026-10-01 | CI/CD: GitHub Actions. Free for public repos and lives next to the code. |
| 2026-10-01 | Exception to open source first: Terraform (Business Source License) over OpenTofu. Terraform is the industry default and the tool Manoj is certified in. The README names OpenTofu as the open-source fork. |
| 2026-10-01 | Kubernetes goes deep and is aligned to the CKA. |
| 2026-10-01 | Each `learn-<tool>` repo is created only when that tool starts. |
| 2026-10-01 | No memory.md or rules/ directory. Claude's auto memory stays on the author's machine and never reaches students; shared context lives in CLAUDE.md. |
| 2026-10-01 | Cadence: weekly during Stage 1, every two weeks from Stage 2. Batch-record 2–3 videos before publishing. |
| 2026-10-01 | Repos are siblings in the workspace root, never nested. The hub links to tool repos by URL in its README; no git submodules. |
| 2026-10-01 | README.md (public roadmap), LICENSE (MIT) and LICENSE-docs (official CC BY 4.0 legal code) created. |
