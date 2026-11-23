![cover](cover.png)

<h1 align="center">Kovarthanam Muthusamy</h1>
<h3 align="center">AI/ML Software Engineer — I solve companies' AI problems</h3>

<p align="center">
I help companies put AI to work — not as demos, but as software that runs in production. Most teams I work
with have the same problem: data and ideas for AI, but no reliable way to turn them into a system customers
can use. I build that bridge — from first prototype to a product running in production.
</p>

<p align="center">
📍 Dortmund, Germany · 🎓 M.Sc. Automation and Robotics, TU Dortmund (2027) · ✉️ kovarthanmuthusamy@gmail.com
</p>

<p align="center">
  <a href="https://linkedin.com/in/kovarthanam-muthusamy-4a8107253"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:kovarthanmuthusamy@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"></a>
  <a href="https://github.com/kovarthanmuthusamy/Generative-AI-System-Engineering-Analysis"><img src="https://img.shields.io/badge/Flagship-Generative_AI_System-181717?style=for-the-badge&logo=github&logoColor=white" alt="Flagship project"></a>
</p>

---

## What I solve for companies

- **LLM applications and agents that handle real tasks end to end.** Multi-agent assistants with an
  orchestrator, RAG, LoRA fine-tuning and typed, validated tool calling — built to work in the real world,
  not just in a notebook.
- **RAG systems — retrieval, grounding and evaluation, not just a chatbot.** Document search and domain
  knowledge your team can trust, with evaluation so you know what it gets right and what it doesn't.
- **Model inference and deployment.** APIs, Docker, CI/CD and cloud infrastructure, so a model becomes a
  tested, reproducible service instead of a script on someone's laptop.
- **MLOps that keeps systems reliable.** Pipelines, monitoring and retraining, so the system you ship keeps
  working after it ships.
- **Engineering domains.** Simulation-driven learning for electronics (PCB power and signal integrity), on
  top of a background in robotics and mechanical design.

## Proof, not promises

- **IEEE paper** on generative AI for engineering design (2026 Kleinheubach Conference).
- **End-to-end generative AI platform** shipped as production software — predicts a board's power behaviour
  in milliseconds instead of a 12-second simulation.
- **Self-healing Kubernetes agent** that diagnosed a live failure and proposed the fix in **37 s for $0.04**.

If your team has an AI problem worth solving, let's talk.

## Featured projects

### 🔌 [Generative AI System for Engineering Analysis](https://github.com/kovarthanmuthusamy/Generative-AI-System-Engineering-Analysis) — AI for circuit-board power design

<a href="https://github.com/kovarthanmuthusamy/Generative-AI-System-Engineering-Analysis"><img src="https://raw.githubusercontent.com/kovarthanmuthusamy/Generative-AI-System-Engineering-Analysis/main/docs/images/assistant-design-view.png" width="760" alt="Generative AI System for Engineering Analysis: board, predicted impedance spectrum and impedance map"></a>

An AI model that predicts how a board's power supply behaves in milliseconds instead of a
12-second simulation, plus a web app that suggests better designs. Published at the [2026 Kleinheubach Conference (IEEE)](https://doi.org/10.23919/IEEECONF72572.2026.11743273).

- Trained on **30,000 simulated layouts**; typical error **2.9 %**
- Checks **≈ 25,000 layouts per second** vs ≈ 12 s per layout in the simulator
- Finds designs with the fewest components; **87–98 %** of proposals pass a real simulation
- Web app + API, Docker, CI, MLflow, 116 automated tests
- Model inference built for Azure ML (managed online endpoint, CPU)

`PyTorch` `DDP` `VAE` `FastAPI` `Docker` `GitHub Actions` `MLflow` `Azure ML`

### 🤖 [AI Assistant System for ECAD Software](https://github.com/kovarthanmuthusamy/AI-assistant-system-for-ECAD-software)

Team project (8 people). Answers circuit-design questions, runs simulations from plain English and explains
the results. I built the agent logic and most of the backend.

- A coordinating agent routes each request to the right specialist: expert model, document search or simulation
- Runs on local or cloud models (DeepSeek-R1, GPT-4o, Gemini) without code changes
- Fine-tuned an 8B open-source model (LoRA) as the domain expert
- Plain English → checked simulation settings; 130 automated tests

`LangChain` `RAG` `ChromaDB` `LoRA` `Ollama` `Pydantic`

### 🚗 [Camera + LiDAR Perception Service](https://github.com/kovarthanmuthusamy/sensor-fusion)

Spots cars and people and tells how far away they are, from a camera and LiDAR.

- LiDAR cuts the distance error **8.1 % → 4.3 %**, at night **10.9 % → 3.6 %**
- Answers in **≈ 0.1 s on a CPU**, about 10 requests per second
- Production-ready API: health checks, monitoring, logging, overload protection, secure container
- 372 tests (95 % coverage); built with Claude Code, every change reviewed

`PyTorch` `ONNX Runtime` `FastAPI` `Docker` `Prometheus` `Claude Code`

### 🗺️ SLAM and Localization using TurtleBot — coursework lab, TU Dortmund

Coursework lab at TU Dortmund. Built SLAM and localization for a TurtleBot — the robot maps its environment and localizes itself within it, so it can navigate autonomously.

- SLAM: the TurtleBot builds a map of its environment while tracking its own position in it
- Developed and tested in Gazebo, visualized in RViz; motion planning with MoveIt

`ROS 2` `Python` `MoveIt` `Gazebo` `RViz`

### 💶 [Finance Agent](https://github.com/kovarthanmuthusamy/finance-agent) — private budgeting and forecasts

Turns bank statements into budgets and cash-flow forecasts. All data stays on the user's computer.

- Imports Sparkasse exports and skips duplicates automatically
- Forecasts 14–90 days ahead and shows the risk of running low on money
- SQLite with versioned schema changes and exact cent amounts; 31 tests in CI

`Python` `Streamlit` `SQLAlchemy` `Alembic` `pytest`

### 🩺 [KubeMedic](https://github.com/kovarthanmuthusamy/kubmedic) — AI agent that fixes broken cloud apps

Finds why a Kubernetes app broke and proposes the fix as a pull request for a human to approve.

- **Live demo (Nov 2026):** diagnosed a bad image tag (ImagePullBackOff) in a live cluster and proposed
  the fix in **37 s for $0.04** — [demo report](https://github.com/kovarthanmuthusamy/kubmedic/blob/main/evals/results/2026-11-21-frontend-bad-image-tag/KubMedic-Demo-Report.pdf)
- Built with LangGraph (triage → investigate → plan), MCP tools and Langfuse traces
- Safe by design: the agent can only read; every fix needs human approval
- Platform: local Kubernetes cluster and local AI models on two GPUs, set up reproducibly

`Kubernetes` `Ollama` `LangGraph` `MCP` `ArgoCD`

## Publications

- N. G. Shoaee, **K. Muthusamy**, W. John, R. Brüning and J. Götze, "[A Variational Autoencoder Framework for PCB Power Delivery Network Design](https://doi.org/10.23919/IEEECONF72572.2026.11743273)," *2026 Kleinheubach Conference*, Miltenberg, Germany, 2026, pp. 1–4. IEEE.
  A generative AI model that designs PCB power networks meeting a target impedance with as few capacitors as possible, without slow EM simulations.

## How I build with agents

- **I use coding agents (Claude Code, Cursor) like a team I direct:** they write code, I make the design decisions and review every change.
- **Guard rails:** every number cites a result file, CI runs on every push, and pull requests stay small.

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

<p align="center"><sub>AI/ML systems · Agentic AI · MLOps — built to solve your problem, not to sit in a notebook</sub></p>
