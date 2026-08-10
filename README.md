# Kovarthanam Muthusamy

**Machine Learning Research Engineer | Engineering Systems**  
Dortmund, Germany | Open to full-time Machine Learning, Industrial ML, Deep Learning, and Robotics roles

I build machine-learning systems for physical engineering problems, from simulation-data pipelines and multimodal graph models to active-learning evaluation, retrieval-augmented engineering assistants, and tested inference applications. My work combines TU Dortmund research in PCB power integrity with earlier industrial experience in robotic welding and mechanical design.

## Selected work

### Deep-learning surrogate for PCB power-delivery-network optimisation

- Implemented a PyTorch multimodal Product-of-Experts VAE for 52-slot PCB layouts, 231-bin impedance spectra, and 64 x 64 spatial field maps.
- Built simulation export, per-frequency normalisation, and split-by-design training across **29,499 layouts and 688,477 layout-frequency records**.
- Evaluated a residual-GP active-learning loop using eCADSTAR labels: off-anchor p99 MAE improved from **9.3628 to 8.8432** across 248 cases, while equal-budget GP acquisition produced a **2.16x top-80 residual lift** over random.
- These results demonstrate improved surrogate error discovery and refinement; final inverse-design candidates still require solver verification.

### [Multi-Agent LLM Assistant for PCB Design CAD](https://github.com/kovarthanmuthusamy/pcb-cad-llm-assistant)

- Built a LangChain ReAct orchestrator that routes engineering requests across domain-model, RAG, simulation, and vision tools.
- Implemented ChromaDB retrieval, Sentence-BERT parameter extraction, LoRA domain adaptation, and Windows eCADSTAR automation.
- Integrated an eCADSTAR simulation interface and documented its Windows-only execution boundary; proprietary CAD outputs, local databases, credentials, model weights, and third-party corpora are intentionally excluded from the public repository.

### [Finance Agent](https://github.com/kovarthanmuthusamy/Finance_agent)

- Built a local-first Streamlit application for Sparkasse CSV/FinTS ingestion, transaction deduplication, budgeting, recurrence detection, and probabilistic forecasting.
- Uses SQLite, SQLAlchemy, Alembic, Pydantic, keyring, Plotly, and exact integer-cent persistence.
- Verified through **57 automated tests**, Ruff, and GitHub Actions; forecasting compares candidate methods through rolling backtests and reports scenario and Monte Carlo reserve risk.

## Technical focus

- **Machine learning:** Python, PyTorch, CUDA, NCCL/DDP, graph neural networks, VAEs, FiLM, active learning
- **LLM systems:** LangChain, ReAct, RAG, ChromaDB, LoRA, Sentence-BERT, tool orchestration
- **Deployment and quality:** FastAPI, Pydantic, Docker, pytest, Ruff, GitHub Actions
- **Data and applications:** SQLite, SQLAlchemy, Alembic, pandas, NumPy, Streamlit, Plotly
- **Engineering tools:** eCADSTAR, ABB RobotStudio, SolidWorks, Git, Linux, Obsidian

## Contact

- [LinkedIn](https://linkedin.com/in/kovarthanam-muthusamy-4a8107253)
- [Email](mailto:kovarthanmuthusamy@gmail.com)
