# Kovarthanam Muthusamy

**Machine Learning Research Engineer | Industrial AI | Engineering Systems**

Dortmund, Germany · Open to full-time opportunities in **Applied Machine Learning, Industrial AI, Deep Learning, Engineering Simulation, and Robotics**

I develop **machine-learning methods and software systems for engineering applications**, with a focus on simulation-driven learning, surrogate modelling, multimodal representation learning, optimisation, and intelligent engineering automation.

My current research at **TU Dortmund University** focuses on generative and surrogate modelling for **PCB Power Delivery Network (PDN) design optimisation**, combining simulation data, deep learning, active learning, and latent-space optimisation.

My engineering background additionally includes **robotic welding, mechanical design, industrial automation, and CAD-based engineering workflows**.

---

## Research & Engineering Projects

### PCB Power Delivery Network Optimisation

**Applied Machine Learning · Surrogate Modelling · Generative AI · Active Learning · Engineering Simulation**

Research project focused on developing a learning-based framework for simulation-efficient optimisation of PCB Power Delivery Networks.

* Developed a **PyTorch-based multimodal Product-of-Experts Variational Autoencoder (PoE-VAE)** for joint representation of:

  * 52-slot PCB capacitor layouts
  * 231-bin impedance spectra
  * 64 × 64 spatial field maps
* Designed simulation-data processing pipelines covering **simulation export, frequency-wise normalisation, dataset construction, and split-by-design evaluation**.
* Built the training dataset from **29,499 PCB layouts and 688,477 layout-frequency records**.
* Developed an **active-learning framework based on residual Gaussian Processes (GPs)** to identify high-error regions for targeted surrogate refinement.
* Evaluated the approach on **248 off-anchor cases**:

  * p99 MAE: **9.3628 → 8.8432**
  * **2.16× top-80 residual lift** compared with random acquisition at equal acquisition budget.
* The methodology targets **simulation-efficient engineering optimisation** by combining learned surrogate representations with targeted data acquisition.
* Generated inverse-design candidates are subsequently subject to **physics-based solver verification**.

**Key methods:** PyTorch · VAE · Multimodal Learning · Surrogate Modelling · Gaussian Processes · Active Learning · Latent-Space Optimisation · Power Integrity Simulation

---

### [Multi-Agent LLM Assistant for PCB CAD](https://github.com/kovarthanmuthusamy/pcb-cad-llm-assistant)

**Engineering AI · CAD Automation · Retrieval-Augmented Generation · Tool Integration**

Team research project at TU Dortmund: a framework that connects language models with PCB engineering tools and domain-specific information sources. I owned the LangChain orchestration, the RAG sub-agent, and the integration with eCADSTAR (Zuken's PCB design suite).

* Implemented a **LangChain ReAct orchestration layer** for routing engineering tasks across domain models, retrieval, simulation, and vision components.
* Developed retrieval pipelines using **ChromaDB and Sentence-BERT-based semantic representations**.
* Applied **LoRA-based domain adaptation** for engineering-specific language-model workflows.
* Integrated Windows-based **eCADSTAR automation and simulation interfaces**.
* Designed explicit interfaces between LLM reasoning, engineering tools, and simulation workflows.
* Documented system boundaries and reproducibility constraints for proprietary engineering software.
* Proprietary CAD outputs, credentials, local databases, model weights, and third-party corpora are intentionally excluded from the public repository.

**Key technologies:** Python · LangChain · RAG · ChromaDB · Sentence-BERT · LoRA · eCADSTAR · CAD Automation

---

### [Finance Agent](https://github.com/kovarthanmuthusamy/Finance_agent)

**Software Engineering · Data Engineering · Forecasting · Quality Assurance**

A local-first financial data application designed with an emphasis on **data integrity, reproducibility, automated testing, and maintainable software architecture**.

* Developed ingestion pipelines for Sparkasse CSV/FinTS transaction data.
* Implemented transaction deduplication, budgeting, recurrence detection, and financial forecasting.
* Built the persistence layer using **SQLite, SQLAlchemy, and Alembic**.
* Used **Pydantic** for structured validation and **keyring** for credential handling.
* Implemented exact **integer-cent persistence** for financial calculations.
* Evaluated forecasting approaches through **rolling backtests**.
* Added scenario analysis and Monte Carlo-based reserve-risk estimation.
* Maintained automated quality checks using **31 tests, Ruff, and GitHub Actions**.

**Key technologies:** Python · SQLite · SQLAlchemy · Alembic · Pydantic · Streamlit · Plotly · pytest · Ruff · GitHub Actions

---

## Technical Expertise

### Machine Learning & AI

<p align="left">
  <img src="https://skillicons.dev/icons?i=python,pytorch,numpy,pandas" />
</p>

**Python · PyTorch · CUDA · NCCL/DDP · Deep Learning · Variational Autoencoders · Graph Neural Networks · Multimodal Learning · FiLM · Active Learning · Surrogate Modelling**

### Engineering AI & LLM Systems

<p align="left">
  <img src="https://skillicons.dev/icons?i=python,docker,fastapi" />
</p>

**LangChain · ReAct · Retrieval-Augmented Generation · ChromaDB · LoRA · Sentence-BERT · Tool Integration · Engineering Automation**

### Software Engineering

<p align="left">
  <img src="https://skillicons.dev/icons?i=git,github,linux,docker,fastapi" />
</p>

**FastAPI · Pydantic · Docker · pytest · Ruff · GitHub Actions · Git · Linux · CI/CD**

### Data Engineering & Applications

<p align="left">
  <img src="https://skillicons.dev/icons?i=sqlite,python" />
</p>

**SQLite · SQLAlchemy · Alembic · pandas · NumPy · Streamlit · Plotly**

### Engineering Software

**eCADSTAR · ABB RobotStudio · SolidWorks · PCB Power Integrity · Engineering Simulation · CAD Automation · Robotic Welding · Mechanical Design**

---

## Research Interests

* **Applied Machine Learning for Engineering**
* **Industrial AI and Engineering Automation**
* **Simulation-driven Machine Learning**
* **Surrogate Modelling and Reduced-Order Learning**
* **Multimodal Representation Learning**
* **Generative Models for Engineering Design**
* **Active Learning and Data-Efficient Simulation**
* **Latent-Space Optimisation**
* **Physics-informed and Physics-constrained Learning**
* **CAD / Simulation Tool Integration**
* **Machine Learning for Electronics and Manufacturing**

---

## Engineering & Research Workflow

My work focuses on connecting **machine-learning methods with engineering simulation and validation**:

**Engineering Problem**
→ **Simulation & Experimental Data**
→ **Data Engineering & Representation Learning**
→ **Surrogate / Generative Model**
→ **Active Learning**
→ **Optimisation**
→ **Candidate Design Generation**
→ **Physics-Based Verification**

The emphasis is on developing **reproducible, testable, and engineering-valid ML systems**, rather than treating model performance as the sole objective.

---

## Professional Focus

**Applied Machine Learning · Industrial AI · Engineering Simulation · Digital Engineering · Deep Learning · Surrogate Modelling · Engineering Optimisation · Robotics · CAD Automation**

---

## Connect

<p align="left">
  <a href="https://linkedin.com/in/kovarthanam-muthusamy-4a8107253">
    <img src="https://img.shields.io/badge/LinkedIn-Professional%20Profile-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" />
  </a>
  <a href="mailto:kovarthanmuthusamy@gmail.com">
    <img src="https://img.shields.io/badge/Email-Contact-EA4335?style=for-the-badge&logo=gmail&logoColor=white" />
  </a>
</p>

---

<p align="center">
  <sub>Machine Learning · Engineering Simulation · Industrial AI</sub>
</p>
