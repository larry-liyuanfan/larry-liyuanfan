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
- Citation verification, trace inspection, cost/policy guards, and a 100-task deterministic Agent contract suite
- Isolated FastAPI + Elasticsearch + Redis + Prometheus stack on Alibaba Cloud SG; deidentified loopback fixture sustained 470.1 QPS at concurrency 10 with P95 42.30 ms, while Redis reduced HTTP P50 by 82.8% (infrastructure evidence, not a public SLA or relevance score)
- Repository: [`australian-housing-intelligence-agent`](https://github.com/larry-liyuanfan/australian-housing-intelligence-agent)

### 3. Climate Claim Verification RAG

Reproducible search-and-ranking laboratory for climate claim verification, separated from unsupported leaderboard claims.

- Verified Spartan build over 1,208,827 evidence passages: BM25 in 40.33 s (126.3 MB) and Qwen3-Embedding-0.6B 1,024-d vectors + FAISS FlatIP in 1,696.77 s (5.13 GB artifact, 21.54 GB MaxRSS)
- BM25 and dense ANN recall, reciprocal-rank fusion, LambdaMART features, hard-negative mining, and cross-encoder reranking adapters
- Evidence selection, calibrated claim classification, and selective abstention
- Retrieval, end-to-end, latency, index-size, and paired-bootstrap evaluation
- CLI and Spartan/Slurm assets for full-data indexing and controlled ablation studies
- HNSW/IVF-PQ and fixed-dev LTR effects remain pending; no unverified relevance lift or leaderboard rank is claimed
- Repository: [`climate-claim-verification-rag`](https://github.com/larry-liyuanfan/climate-claim-verification-rag)

### 4. Wildfire Burn-window Decision Support

Deterministic, explainable domain tools for agents operating over large spatiotemporal climate data.

- Typed prescription rules, temporal alignment, continuous-window extraction, limiting-factor attribution, and sensitivity analysis
- Xarray/Dask data pipeline with checkpointable Spartan execution assets
- Greedy, nominal MILP, and max-min robust MILP scheduling with an independent feasibility checker
- In a 30-seed synthetic benchmark, nominal MILP improved mean utility by 1.79% over the best greedy baseline (bootstrap mean 95% interval 0.91%-2.77%); robust scheduling reduced mobilisation-penalty units by 2.55% (synthetic operational proxies, not dollars or realised fire-risk reduction)
- Golden fixtures and 35 tests for tool schemas, rule boundaries, and feasible schedules
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
