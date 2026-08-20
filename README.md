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

### 2. Australian Energy Market Intelligence Agent

Agentic decision-support system over official Australian National Electricity Market data: market retrieval, official-evidence search, price-risk forecasting, constrained battery dispatch, economic sensitivity and auditable answers.

- Validated 525,600 five-minute AEMO rows across five NEM regions and repaired one incomplete daily archive only from official monthly MMSDM data
- Indexed 735 AEMO/AER report chunks; hybrid+rerank reached source-routing MRR 0.967 and Recall@5 1.00 on a 20-query benchmark (BM25 MRR 0.892)
- Eight typed tools, bounded state-machine recovery and durable traces; the 80 real-window + 20 fault-fixture suite achieved 100% task/schema/citation/logical-tool/recovery success
- Four seasonal folds across five regions produced 560 out-of-time region-days. At 0/25/50/100 AUD per discharged MWh, the five-region mean annualised operating-margin proxy was AUD 76.6k/53.2k/41.0k/24.2k per MW-year; all five regional P05 values were negative at 50 AUD/MWh
- Alibaba Cloud SG stack with FastAPI, Elasticsearch, Redis and Prometheus; 140/140 bounded loopback checks passed with P95 1.911 s
- Economic figures are historical spot-market proxies with a user-supplied cycling cost, excluding CAPEX, fixed O&M, network fees, FCAS and investment returns
- Repository: [`australian-energy-market-intelligence-agent`](https://github.com/larry-liyuanfan/australian-energy-market-intelligence-agent)

### 3. Climate Claim Verification RAG

Reproducible search-and-ranking laboratory for climate claim verification, separated from unsupported leaderboard claims.

- Verified Spartan build over 1,208,827 evidence passages: BM25 in 40.33 s (126.3 MB) and Qwen3-Embedding-0.6B 1,024-d vectors + FAISS FlatIP in 1,696.77 s (5.13 GB artifact, 21.54 GB MaxRSS)
- HNSW retained 0.9961 Recall@5 versus FlatIP ground truth while reaching 3,060.64 in-memory batch QPS and 12.88 ms single-query P50 on the fixed 154-query/32-thread benchmark
- BM25+dense RRF lifted fixed-dev Recall@5/Evidence F1 from 0.1721/0.1168 to 0.2709/0.1785
- Balanced RRF/Qwen3-Reranker-4B fusion over 7,700 pairs reached 0.3153/0.2131; four 5,000-sample paired intervals versus RRF were positive, with P95 4.82 s/query
- HNSW+RRF remains the latency default; 4B fusion is an offline dev-selection profile, not independent-test generalisation. IVF-PQ and LambdaMART failed the quality gate; no leaderboard claim is made
- 28 tests plus CLI and Spartan/Slurm assets for reproducible indexing and ablation
- Repository: [`climate-claim-verification-rag`](https://github.com/larry-liyuanfan/climate-claim-verification-rag)

### 4. Wildfire Burn-window Decision Support

Deterministic, explainable domain tools for agents operating over large spatiotemporal climate data.

- Typed prescription rules, temporal alignment, continuous-window extraction, limiting-factor attribution, and sensitivity analysis
- Xarray/Dask data pipeline with checkpointable Spartan execution assets
- Greedy, nominal, max-min and empirical lower-tail CVaR MILPs with independent feasibility checks
- In a 30-seed synthetic benchmark, nominal MILP improved mean utility by 1.79% over the best greedy (95% interval 0.91%-2.77%); CVaR improved mean held-out P05 utility by 1.42% versus nominal (95% interval 0.25%-3.25%)
- Agent-facing rejection reason codes and neighbouring crew-capacity counterfactuals explain scheduling trade-offs; their deltas are not LP shadow prices, causal effects or money
- Golden fixtures and 38 tests for schemas, rule boundaries, no-lookahead alignment and feasible schedules
- Results are synthetic utility evidence, not dollars, realised hectares or fire-risk reduction; real VicClim6 processing remains blocked on authorised Mediaflux access
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
