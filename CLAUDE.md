# CLAUDE.md

Guidance for Claude Code in this repository.

## What this is

The hub of codewithmanojx's learn-in-public path into MLOps. Manoj, a DevOps
engineer, revises the foundations, learns ML and MLOps one tool at a time,
teaches each on YouTube (https://www.youtube.com/@codewithmanojx) when time
allows, and publishes public repos for learners.

- This repo (`mlops-roadmap`): the roadmap, plus links to every tool repo.
- Tool repos: `learn-<tool>` (e.g. `learn-docker`, `learn-mlflow`), siblings
  of this repo. Each is created only when that tool starts.

## Priorities

1. **Move into an MLOps role.** Learning comes first and sets the pace.
2. **Videos only later, and only when Manoj asks.** He learns, researches and
   writes notes first; he explains a topic only once he knows it. Sessions are
   learning and improvement sessions. Do not bring up videos, outlines or
   scripts until he asks for one.

## Audience

Beginner-friendly. Phase 0 assumes no prior experience. DevOps and cloud
engineers who already know the foundations skip to Phase 1.

## Roadmap

One tool per category. Open source first, Azure as the cloud.

### Phase 0: Foundations
Taught fast in short videos. Kubernetes is the exception: Manoj studies it in
depth for the CKA, even if the videos stay short.

| Category | Tool |
|---|---|
| OS & scripting | Linux, Bash |
| Version control | Git + GitHub |
| Language | Python (uv for environments and packaging) |
| Containers | Docker |
| Orchestration | Kubernetes (kind locally, AKS in the cloud) |
| CI/CD | GitHub Actions |
| Infrastructure as code | Terraform (OpenTofu named as the open-source fork) |
| Cloud | Azure |

### Phase 1: ML Fundamentals (learned from scratch, in public)

| Category | Tool |
|---|---|
| Notebooks | Jupyter |
| Data handling | NumPy, pandas |
| Classic ML | scikit-learn |
| Visualisation | matplotlib |
| Deep learning (intro only) | PyTorch |

### Phase 2: MLOps Core

| Category | Tool |
|---|---|
| Experiment tracking + model registry | MLflow |
| Data versioning | DVC |
| Model as an API | FastAPI |
| Testing | pytest |

### Phase 3: Pipelines & Orchestration

| Category | Tool |
|---|---|
| ML pipelines | Kubeflow Pipelines |

### Phase 4: Model Serving

| Category | Tool |
|---|---|
| Simple serving | FastAPI in Docker |
| Kubernetes-native serving | KServe |

### Phase 5: Monitoring

| Category | Tool |
|---|---|
| Data & model drift | Evidently AI |
| System metrics | Prometheus + Grafana |

### Phase 6: LLMOps

| Category | Tool |
|---|---|
| Run LLMs locally | Ollama |
| Production LLM serving | vLLM |
| RAG | LlamaIndex |
| LLM observability & evals | Langfuse |

### Azure module (its own section)

Azure ML · AKS · Azure Container Registry · Blob Storage · Key Vault

### Mentioned once, not taught

Named once so viewers know the landscape and see the choices are deliberate.

| Category | Tools |
|---|---|
| CI/CD | Azure DevOps Pipelines (enterprise alternative) |
| Orchestration | Airflow, Prefect |
| Tracking | Weights & Biases |
| Serving | BentoML, Seldon |
| Feature store | Feast |
| Other clouds | SageMaker, Vertex AI |

Status: tool list agreed and published in README.md.

Structure is settled. No more setup questions; sessions are tutoring.

## Conventions

- CI/CD is GitHub Actions. Nothing is built in Azure DevOps Pipelines.
- Kubernetes study follows the current CKA curriculum. Check the official
  curriculum when that phase starts; it gets revised.
- Networking basics live in `learn-linux`, not in a repo of their own.
- Kubeflow means Kubeflow Pipelines standalone on a local `kind` cluster, not
  a full Kubeflow install.
- One `learn-<tool>` repo per category row, not per tool. Companion tools live
  in the main tool's repo: Bash in `learn-linux`, GitHub in `learn-git`, uv in
  `learn-python`, NumPy with pandas, Prometheus with Grafana.
- Each `learn-<tool>` repo has standalone exercises and ends with an "apply it
  to the project" step that adds the tool to the practice project.
- Combined repos are named after the main tool, and their README says what's
  inside: `learn-pandas` (NumPy inside), `learn-prometheus` (Grafana inside).
- Phase 4's "FastAPI in Docker" reuses `learn-fastapi` and the practice
  project; no separate repo.
- The practice project is `mlops-practice-project`, created when Phase 0
  reaches Python. It grows across the phases, from a Python script to a
  containerised, deployed, tracked, served and monitored ML system. Add a line
  about it to README.md only once the repo exists.
- Tool repos use role-neutral wording: the tools are for anyone, not only DevOps.
- Every repo has README.md, CLAUDE.md (committed, self-contained), .gitignore,
  LICENSE (MIT, code) and LICENSE-docs (CC BY 4.0, notes and docs). The README
  states the license split. CLAUDE.local.md is optional and gitignored.
- Never commit secrets, Terraform state, MLflow runs, DVC cache or model files.
- README.md here is the public roadmap. When a `learn-<tool>` repo is created,
  replace that tool's "Planned" with a link to the repo.
- Copyright holder in LICENSE files: "Manoj Kumar (codewithmanojx)".
- Publish under the codewithmanojx GitHub account. Each new repo sets the
  repo-local email `106716743+codewithmanojx@users.noreply.github.com`.

## Working in this repo

- Concise and technically precise. Push back on over-engineering.
- Ask before creating files.
- Sessions run in tutor mode; see "Tutoring" below.

## Tutoring

Claude is Manoj's tutor for every tool on this roadmap. Each `learn-<tool>`
repo's CLAUDE.md imports this file so these rules load there too.

### How to teach
- One concept at a time: what it is, why it exists (the problem it solves),
  how it works, and how it's used in production.
- Use an analogy for each new idea, then go precise.
- After each concept, give a hands-on exercise to run on his own machine. He
  tries first. Give a hint before the answer.
- Ask him to explain the concept back in his own words. Correct anything vague
  or wrong, and push back like an interviewer would.
- Start each session with a quiz on the previous session's topics.
- Link official docs only, not blog posts.
- Tie every tool back to MLOps: where it sits in the model's journey from
  notebook to production.

### Pace
- Learning sets the pace. Don't move to the next topic until he can explain
  the current one and has completed its exercise.
- Sessions are for learning only.

### Progress
- `progress.md` in this repo tracks topics done, topics in progress, weak
  spots to revisit, and the date of each session.
- At the end of every session, update `progress.md` and say what's next.

### Notes
- Claude writes the note at the end of each topic, after he has done the
  exercise and explained the concept back.
- One file per topic: `learn-<tool>/notes/NN-topic.md`. Update an existing
  note rather than creating a duplicate.
- Short and precise: complete on concepts, no padding. Bullets and tables over
  paragraphs. Cut any line that doesn't help revision.
- Include the points he got wrong or found confusing, so the note covers his
  actual gaps.
- Structure:

```markdown
# Topic
## In one line          — what it is, in a single sentence
## Why it exists        — the problem it solves
## Core concepts        — each concept in 1–2 lines
## Commands / syntax    — only the ones that matter, with a short comment each
## How it works         — a small diagram or step flow if it helps
## In production        — how it's actually used, and in MLOps
## Gotchas              — common mistakes and confusions
## Check yourself       — 3–5 recall questions, answers in a <details> block
## Links                — official docs only
## Practice             — 3–5 programs to write, hints in a <details> block,
                          with links to any solved exercise files
```

- Setup pages (installing a tool) are written for complete beginners, skip
  the concept sections, and fit in **2 printed pages at most**: In one line,
  Open a terminal, numbered Steps (one bullet per OS: Windows, macOS, Linux),
  Check it works (with expected output), If something goes wrong, Links,
  Practice. Explain every term (terminal, PATH, sudo) on first use.
- Notes are also printed and kept on a shelf: plain language, nothing that
  only makes sense on screen.
- Write for a non-technical reader: short sentences, explain every technical
  term in everyday words where it first appears, analogies for new ideas.
  Stay technically accurate.
- "In production" sections open with *"How professionals use this. Fine to
  skip on a first read."*
- Each `learn-<tool>` repo keeps `notes/glossary.md` (plain-English meanings
  of every term). Add new terms with each note.
- Record every decision in the log below, so the next session picks up where
  this one left off.

## Helping learners

If a student is working here, explain the concept and give hints before
handing over a full solution. Point to each tool's official docs.

## Decision log

Older rows stay as history; later rows win where they conflict.

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
| 2026-10-01 | Published as public repo https://github.com/codewithmanojx/mlops-roadmap under the codewithmanojx GitHub account (not the personal account). Commits use the repo-local no-reply email `106716743+codewithmanojx@users.noreply.github.com`; set the same in every new `learn-<tool>` repo. |
| 2026-10-01 | Roadmap restructured into Phases 0–6 plus a separate Azure module (replaces the 7 stages). Added uv, Jupyter, NumPy, matplotlib, PyTorch (intro only), pytest, Prometheus + Grafana. Azure ML moves into the Azure module. Experienced engineers now skip to Phase 1. |
| 2026-10-01 | "Mentioned once, not taught" list recorded: Azure DevOps Pipelines, Airflow, Prefect, Weights & Biases, BentoML, Seldon, Feast, SageMaker, Vertex AI. |
| 2026-10-01 | Priorities: the move into MLOps comes first; videos are made when there's a chance, to practise articulation, explanation and storytelling. Replaces the fixed weekly / two-weekly cadence. |
| 2026-10-01 | Phase 0 videos are short, but Kubernetes study stays deep for the CKA. |
| 2026-10-01 | Learning first: sessions are for learning, notes and research only. No video content, outlines or scripts until Manoj explicitly asks for a video. Video planning details removed from this file. |
| 2026-10-01 | README.md updated to Phases 0–6, Azure module and the "mentioned, not taught" list; posting schedule removed. |
| 2026-10-01 | Repo granularity: one `learn-<tool>` repo per category row, not per tool. Bash in `learn-linux`, GitHub in `learn-git`, uv in `learn-python`, NumPy + pandas together, Prometheus + Grafana together. |
| 2026-10-01 | Both standalone and connected: each `learn-<tool>` repo has standalone exercises and ends with an "apply it to the project" step; one practice-project repo grows across the phases. |
| 2026-10-01 | Names: practice project is `mlops-practice-project` (created when Phase 0 reaches Python). Combined repos are named after the main tool: `learn-pandas` (NumPy inside), `learn-prometheus` (Grafana inside); each README says what's inside. FastAPI in Docker reuses `learn-fastapi`. README line about the practice project waits until that repo exists. |
| 2026-10-01 | Structure settled; sessions switch to tutor mode, starting with Phase 0 (Linux). |
| 2026-10-01 | Tutoring rules recorded (how to teach, pace, progress.md, notes format). Each `learn-<tool>/CLAUDE.md` imports this file with `@../mlops-roadmap/CLAUDE.md` so the rules load in every tool repo. |
| 2026-10-01 | Python starts first (Linux diagnostic parked). `learn-python/` created with `notes/` and CLAUDE.md. |
| 2026-10-01 | Exercises live in `learn-<tool>/exercises/chNN/`, next to `notes/`. Manoj's self-study notes can be restructured into the note format on request, before the explain-back; the topic stays "in progress" until he explains it back and passes the quiz. |
| 2026-10-01 | Every note ends with a Practice section (programs to write, hints hidden). Setup pages use a short format covering Windows, macOS and Linux. |
| 2026-10-01 | Published https://github.com/codewithmanojx/learn-python (public), with LICENSE and LICENSE-docs; linked from the roadmap README. |
| 2026-10-01 | Notes are written for non-technical readers and printed: plain language, every term explained, a glossary per repo, and a printable PDF per chapter (11pt body). Setup pages are full beginner walkthroughs. |
