# Kovarthanam Muthusamy

### Machine Learning Research Engineer · Industrial AI · Engineering Systems

📍 Dortmund, Germany · 🇩🇪
🎯 Open to full-time opportunities in **Machine Learning · Industrial AI · Deep Learning · Robotics**

I build **machine-learning systems for physical engineering problems**, combining deep learning, simulation data, multimodal representation learning, active learning, and LLM-based engineering automation.

My research focuses on **AI-driven engineering design and optimisation**, with current work on PCB Power Delivery Networks (PDNs), surrogate modelling, latent-space optimisation, and simulation-guided learning. My broader engineering background includes **robotic welding, mechanical design, and industrial automation**.

---

## 🔬 Research & Selected Projects

### ⚡ Deep Learning Surrogate for PCB Power Delivery Network Optimisation

**Research focus:** Multimodal generative modelling · Surrogate modelling · Active learning · Latent-space optimisation

* Developed a **PyTorch multimodal Product-of-Experts VAE** representing:

  * 52-slot PCB capacitor layouts
  * 231-bin impedance spectra
  * 64 × 64 spatial field maps
* Built the simulation-data pipeline including **simulation export, per-frequency normalisation, and split-by-design evaluation**.
* Training dataset contains **29,499 layouts and 688,477 layout-frequency records**.
* Implemented and evaluated a **residual-GP active-learning loop** for targeted surrogate refinement.
* Across 248 off-anchor cases:

  * p99 MAE improved from **9.3628 → 8.8432**
  * Equal-budget GP acquisition achieved a **2.16× top-80 residual lift** over random acquisition.
* The active-learning results demonstrate improved identification of high-error regions for surrogate refinement.
* **Inverse-design candidates remain subject to physics/simulation solver verification.**

> **Research direction:** Generative surrogate modelling → latent-space optimisation → simulation-verified engineering design.

---

### 🤖 [Multi-Agent LLM Assistant for PCB Design CAD](https://github.com/kovarthanmuthusamy/pcb-cad-llm-assistant)

**Engineering focus:** LLM agents · RAG · CAD automation · Engineering tool orchestration

* Developed a **LangChain ReAct multi-agent orchestration system** for PCB engineering workflows.
* Routes engineering requests across:

  * Domain models
  * Retrieval-augmented generation
  * Simulation tools
  * Computer-vision tools
* Implemented **ChromaDB retrieval, Sentence-BERT parameter extraction, and LoRA domain adaptation**.
* Integrated Windows-based **eCADSTAR automation and simulation workflows**.
* Documented the Windows-only execution boundary and separated proprietary engineering assets from the public repository.
* Proprietary CAD outputs, local databases, credentials, model weights, and third-party corpora are intentionally excluded.

---

### 💶 [Finance Agent](https://github.com/kovarthanmuthusamy/Finance_agent)

**Engineering focus:** Local-first AI applications · Data engineering · Forecasting · Software quality

* Developed a **local-first Streamlit financial analytics application** for Sparkasse CSV/FinTS data.
* Implemented:

  * Transaction ingestion and deduplication
  * Budget management
  * Recurrence detection
  * Probabilistic forecasting
  * Scenario analysis
  * Monte Carlo reserve-risk estimation
* Built around **SQLite, SQLAlchemy, Alembic, Pydantic, keyring, and Plotly**.
* Uses **exact integer-cent persistence** for financial calculations.
* Forecasting methods are evaluated using **rolling backtests** rather than relying on a single model.
* Verified through **57 automated tests**, Ruff, and GitHub Actions.

---

## 🧠 Technical Stack

### Machine Learning & Scientific Computing

<p align="left">
  <img src="https://skillicons.dev/icons?i=python,pytorch,opencv,numpy,pandas,matlab" />
</p>

**Python · PyTorch · CUDA · NCCL/DDP · Graph Neural Networks · VAEs · FiLM · Active Learning · NumPy · pandas**

### LLM & AI Systems

<p align="left">
  <img src="https://skillicons.dev/icons?i=python,docker,fastapi" />
</p>

**LangChain · ReAct · RAG · ChromaDB · LoRA · Sentence-BERT · Tool Orchestration · Agentic AI**

### Software Engineering & Deployment

<p align="left">
  <img src="https://skillicons.dev/icons?i=git,github,linux,docker,fastapi,pytest" />
</p>

**FastAPI · Pydantic · Docker · pytest · Ruff · GitHub Actions · Linux**

### Data & Applications

<p align="left">
  <img src="https://skillicons.dev/icons?i=sqlite,postgres,python" />
</p>

**SQLite · SQLAlchemy · Alembic · pandas · NumPy · Streamlit · Plotly**

### Engineering & Simulation

**eCADSTAR · ABB RobotStudio · SolidWorks · PCB Power Integrity · Simulation Data Pipelines · Mechanical Design · Robotic Welding**

---

## 🧪 Research Interests

```text
Machine Learning for Engineering
├── Generative Models
│   ├── Variational Autoencoders
│   ├── Multimodal Representation Learning
│   └── Latent-Space Optimisation
│
├── Engineering Surrogate Models
│   ├── Physics-informed Learning
│   ├── Simulation-based Learning
│   └── Active Learning
│
├── Industrial AI
│   ├── Engineering Agents
│   ├── RAG Systems
│   └── CAD / Simulation Automation
│
└── Intelligent Engineering Design
    ├── PCB Power Delivery Networks
    ├── Design Optimisation
    └── Simulation-verified AI
```

---

## 📊 Engineering Approach

I focus on building systems where **machine-learning performance is connected to engineering validity**.

**Simulation / Engineering Data**
↓
**Multimodal Representation Learning**
↓
**Generative / Surrogate Model**
↓
**Active Learning & Error Discovery**
↓
**Latent-Space Optimisation**
↓
**Candidate Design Generation**
↓
**Physics / Solver Verification**

The objective is not simply to build a high-performing ML model, but to develop **reproducible, testable, and engineering-grounded ML systems**.

---

## 📌 Current Focus

* 🧠 Generative AI for engineering design
* ⚡ PCB Power Delivery Network optimisation
* 🔬 Multimodal surrogate modelling
* 🎯 Active learning for simulation-efficient training
* 🧩 Latent-space optimisation
* 🤖 Agentic AI for engineering workflows
* 🏭 Industrial machine learning and automation
* 🧪 Simulation-verified AI systems

---

## 📫 Connect

<p align="left">
  <a href="https://linkedin.com/in/kovarthanam-muthusamy-4a8107253">
    <img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:kovarthanmuthusamy@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
</p>

---

<p align="center">
  <i>Building machine learning systems for real engineering problems.</i>
</p>
