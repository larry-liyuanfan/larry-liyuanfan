# Liyuan Fan

Master of Data Science at the University of Melbourne, focused on **Multimodal Search, RAG and Agentic AI Applications**.

I build evidence-grounded AI systems that connect multimodal understanding, multi-stage retrieval, tool-using agents, and deterministic domain services.

## Featured Projects

### 1. Trip — Multimodal Search and Travel Planning

Flagship OTA application that turns travel images, reviews, and user constraints into structured information, searchable candidates, and travel-planning inputs.

- VLM-based image understanding and schema-constrained extraction
- Visual, keyword, and hybrid retrieval with Milvus-backed serving
- Versioned prompts, evaluation datasets, failure analysis, and experiment tracking
- FastAPI, Docker, vLLM/Model Studio, Alibaba Cloud, and Spartan GPU workflows
- Repository: [`Trip_Project`](https://github.com/larry-liyuanfan/Trip_Project)

### 2. Australian Housing Intelligence Agent

Agentic-search system built on a university team project's housing-discussion and official-evidence datasets. The public extension focuses on my implementation of safe tool use, evidence retrieval, and evaluation.

- Typed tools and an explicit state machine for planning, execution, retries, loop detection, and empty-result recovery
- Separate social-discussion and official-evidence retrieval with filters, hybrid search, fusion, and reranking adapters
- Citation verification, trace inspection, cost/policy guards, and task-level Agent evaluation
- FastAPI, Elasticsearch, Redis, Docker Compose, and Alibaba Cloud deployment assets
- Repository: [`australian-housing-intelligence-agent`](https://github.com/larry-liyuanfan/australian-housing-intelligence-agent)

### 3. Climate Claim Verification RAG

Reproducible search-and-ranking laboratory for climate claim verification, separated from unsupported leaderboard claims.

- BM25 and dense ANN recall, reciprocal-rank fusion, learning-to-rank features, and cross-encoder reranking adapters
- Hard-negative mining, evidence selection, calibrated claim classification, and selective abstention
- Retrieval, end-to-end, latency, index-size, and paired-bootstrap evaluation
- CLI and Spartan/Slurm assets for full-data indexing and controlled ablation studies
- Repository: [`climate-claim-verification-rag`](https://github.com/larry-liyuanfan/climate-claim-verification-rag)

### 4. Wildfire Burn-window Decision Support

Deterministic, explainable domain tools for agents operating over large spatiotemporal climate data.

- Typed prescription rules, temporal alignment, continuous-window extraction, limiting-factor attribution, and sensitivity analysis
- Xarray/Dask data pipeline with checkpointable Spartan execution assets
- Constraint-aware scheduling with deterministic baselines and an optional MILP solver
- Golden fixtures and invariant tests for tool schemas, rule boundaries, and feasible schedules
- Repository: [`wildfire-burn-window-decision-support`](https://github.com/larry-liyuanfan/wildfire-burn-window-decision-support)

### 5. Fulfillment Optimization Decision Support

Reproducible decision-optimization pipeline for order-wave release and workforce scheduling.

- Gurobi mixed-integer programming, exact baselines, scenario experiments, and solver validation
- Repository: [`fulfillment-optimization-decision-support`](https://github.com/larry-liyuanfan/fulfillment-optimization-decision-support)
- Demo: [`GitHub Pages`](https://larry-liyuanfan.github.io/fulfillment-optimization-decision-support/)

## Technical Focus

- Multimodal AI: VLM inference, image-text alignment, structured extraction, evaluation datasets
- Search and RAG: BM25, dense ANN, hybrid retrieval, fusion, learning-to-rank, reranking, retrieval evaluation
- Agentic AI: typed tool calling, explicit state machines, evidence verification, traces, failure recovery, Agent Eval
- Systems: Python, FastAPI, Elasticsearch, Redis, Milvus, Docker, Slurm, Xarray, Dask

## Contact

- Email: liyuan.fan.2@student.unimelb.edu.au
- LinkedIn: pending
