<h1 align="center">Hi, I'm Kovarthanam 👋</h1>
<h3 align="center">ML Software Engineer · Agentic AI Systems</h3>

<p align="center">
I build ML systems end to end — from simulation data and deep generative models to tested APIs,
containers and CI — and LLM agents that use real engineering tools.
</p>

<p align="center">
📍 Dortmund, Germany · 🎓 Master's thesis at TU Dortmund (2026) · 💼 Open to ML / AI engineering roles
</p>

<p align="center">
  <a href="https://linkedin.com/in/kovarthanam-muthusamy-4a8107253"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:kovarthanmuthusamy@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://github.com/kovarthanmuthusamy/pdn-genai-optimization"><img src="https://img.shields.io/badge/Flagship-PDN_Design_Assistant-181717?style=for-the-badge&logo=github&logoColor=white" alt="Flagship project"></a>
</p>

---

## What I work on

- **ML systems, not just models.** Data pipelines, multi-GPU training, typed REST APIs, Docker images, CI and
  experiment tracking around the model, so that it can be run, tested and shipped by someone else.
- **Agentic AI.** LLM agents that plan, call tools and hand results back to each other, and agent workflows
  that I use to build software and research faster without giving up control over correctness.
- **Engineering domains.** Simulation-driven learning for electronics (PCB power and signal integrity), on top
  of a background in robotics and mechanical design.

## Featured projects

### 🔌 [PDN Design Assistant](https://github.com/kovarthanmuthusamy/pdn-genai-optimization) — generative AI for PCB power delivery

<a href="https://github.com/kovarthanmuthusamy/pdn-genai-optimization"><img src="https://raw.githubusercontent.com/kovarthanmuthusamy/pdn-genai-optimization/main/docs/images/assistant-design-view.png" width="760" alt="PDN design assistant: board, predicted impedance spectrum and impedance map"></a>

My master's thesis, packaged as a working product. A product-of-experts VAE learns how decoupling-capacitor
placements shape a board's impedance spectrum and spatial impedance map. A latent-space search designs
placements for a target, and a web app with the field solver in the loop checks and fixes layouts live.

- **30,000 simulated layouts** from a batched, resumable eCADSTAR pipeline (about 100 h of solver time)
- **2.9 % typical error** per frequency point of the predicted spectrum
- **≈ 25,000 layouts per second** judged by the model, against ≈ 12 s per layout in the solver
- Inverse design reaches the **smallest feasible decap budgets**; 87–98 % of its proposals pass in simulation
- FastAPI service and browser UI, multi-stage Docker images, GitHub Actions CI, MLflow tracking, 116 data-free tests

`PyTorch` `DDP` `Graph networks` `VAE` `FiLM` `FastAPI` `Docker` `GitHub Actions` `MLflow` `pytest`

### 🤖 [Multi-Agent LLM Assistant for PCB CAD](https://github.com/kovarthanmuthusamy/pcb-cad-llm-assistant) — agents that operate a real EDA tool

Team research project at TU Dortmund. An orchestrator LLM breaks a request into steps and routes each step to
a specialised agent: a fine-tuned PCB expert, a RAG agent over documents and the web, a simulation agent that
drives eCADSTAR, and a vision agent that turns circuit and result images into text for the planner.

- I owned the **LangChain ReAct orchestration**, the **RAG sub-agent** (LLM router + Chroma vector store) and the
  **eCADSTAR integration**
- **Model-agnostic** orchestrator: DeepSeek-R1 locally via Ollama, GPT-4o or Gemini 1.5 Pro
- Tools registered as typed LangChain `StructuredTool`s with Pydantic schemas; one JSON action per step
- Fine-tuned sub-agents: DeepSeek-R1-Distill-Llama-8B + LoRA (domain expert), Granite-Vision-3.2-2B, 4-bit + LoRA (vision)
- Contract tests in CI; proprietary CAD files, weights and corpora deliberately kept out of the public repo

`LangChain` `ReAct` `RAG` `ChromaDB` `Sentence-BERT` `LoRA` `Ollama` `eCADSTAR`

### 💶 [Finance Agent](https://github.com/kovarthanmuthusamy/Finance_agent) — local-first finance analytics

A privacy-first app that turns raw bank statements into budgets, cash-flow analysis and forecasts, built with
an emphasis on data integrity, reproducibility and tests.

- Ingests Sparkasse CSV exports and read-only FinTS data, with duplicate-safe imports
- SQLite + SQLAlchemy + Alembic persistence with exact integer-cent amounts; Pydantic validation; keyring for credentials
- Recurrence detection, forecasting checked with rolling backtests, scenario analysis and Monte Carlo reserve risk
- 31 tests, Ruff and GitHub Actions

`Python` `Streamlit` `SQLAlchemy` `Alembic` `Pydantic` `Plotly` `pytest`

### 🌙 Night-time Camera + LiDAR Fusion — *in progress*

Does LiDAR depth close the day–night gap of a camera detector? The same 2D detector with a distance head is
trained twice on nuScenes — on RGB only and on RGB plus projected LiDAR depth — and compared on day and night
scenes (mAP and distance error). Set up like a production project from day one: Hydra configs, Weights &
Biases, pre-commit, mypy, pytest and CI, with design decisions recorded as ADRs.

`PyTorch` `torchvision` `nuScenes` `Hydra` `W&B`

## How I build with agents

**Agents I build** — an orchestrator with tool-using sub-agents, typed tool schemas, retrieval routing, and
vision-to-text so that a text-only planner can reason over images (the PCB CAD assistant above).

**Agents I build with** — I use coding agents (Claude Code, Cursor) like a team I direct, with guard rails:

- **Evidence-first multi-agent pipeline for my thesis.** An *evidence extractor* returns only facts it can point
  at in a file → a *literature researcher* verifies every citation against its source → a *writer* with no
  repository or web access drafts from those facts only → an *adversarial reviewer* audits every number, symbol
  and claim → revision. The pipeline is scripted as a Claude Code workflow with custom sub-agents.
- **Rules the agents must follow.** Every numerical claim cites a result file; path-scoped rules, hooks
  (auto-format, session status) and custom skills keep sessions consistent.
- **I review every diff.** Agents do the typing; I make the design decisions, review each change, and keep pull
  requests small with CI on every push.

## Tech stack

| | |
|---|---|
| **ML & data** | ![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white) ![CUDA](https://img.shields.io/badge/CUDA_%2B_DDP-76B900?style=flat-square&logo=nvidia&logoColor=white) ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white) ![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white) ![pandas](https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white) ![matplotlib](https://img.shields.io/badge/matplotlib-11557C?style=flat-square) |
| **LLMs & agents** | ![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white) ![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white) ![OpenAI](https://img.shields.io/badge/OpenAI_GPT--4o-412991?style=flat-square) ![Gemini](https://img.shields.io/badge/Gemini-8E75B2?style=flat-square&logo=googlegemini&logoColor=white) ![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6446?style=flat-square) ![LoRA](https://img.shields.io/badge/LoRA_fine--tuning-555555?style=flat-square) ![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white) ![Cursor](https://img.shields.io/badge/Cursor-000000?style=flat-square&logo=cursor&logoColor=white) |
| **MLOps & serving** | ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white) ![Pydantic](https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white) ![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white) ![MLflow](https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white) ![pytest](https://img.shields.io/badge/pytest-0A9EDC?style=flat-square&logo=pytest&logoColor=white) ![Ruff](https://img.shields.io/badge/Ruff-D7FF64?style=flat-square&logo=ruff&logoColor=black) |
| **Data & apps** | ![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white) ![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square&logo=sqlalchemy&logoColor=white) ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white) ![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=flat-square&logo=plotly&logoColor=white) |
| **Engineering & tools** | ![eCADSTAR](https://img.shields.io/badge/eCADSTAR_%28Zuken%29-005BAC?style=flat-square) ![ABB RobotStudio](https://img.shields.io/badge/ABB_RobotStudio-FF000F?style=flat-square) ![SolidWorks](https://img.shields.io/badge/SolidWorks-DA291C?style=flat-square) ![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white) ![Linux](https://img.shields.io/badge/Linux_%2F_WSL2-FCC624?style=flat-square&logo=linux&logoColor=black) ![LaTeX](https://img.shields.io/badge/LaTeX-008080?style=flat-square&logo=latex&logoColor=white) ![Obsidian](https://img.shields.io/badge/Obsidian-7C3AED?style=flat-square&logo=obsidian&logoColor=white) ![Mermaid](https://img.shields.io/badge/Mermaid-FF3670?style=flat-square&logo=mermaid&logoColor=white) |

## Background

Before machine learning I worked on robotic welding, mechanical design, industrial automation and CAD-based
engineering workflows.

**Interests:** simulation-driven ML · generative models for engineering design · agentic AI for engineering
tools · MLOps for research code

---

<p align="center"><sub>ML systems · Agentic AI · Engineering simulation</sub></p>
