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

- Validated 1,051,200 five-minute AEMO rows across five NEM regions and two years; interval-ending day semantics, official monthly MMSDM repair, duplicate/gap gates and hashes keep the time axis fail-closed
- Indexed 735 AEMO/AER report chunks; hybrid retrieval reached source-routing MRR/Recall@5 1.00/1.00 and author-curated exact-passage MRR/Recall@5 0.80/1.00, while the stronger BM25 passage MRR 0.875 is retained rather than hidden
- Eight typed tools, bounded state-machine recovery and durable traces; the 80 real-window + 20 fault-fixture suite achieved 100% task/schema/citation/logical-tool/recovery success
- A two-year rolling gate produced 1,120 out-of-time region-days: LightGBM won MAE in only 15/40 folds, but forecast-driven MILP dispatch beat the threshold rule in 39/40; the five-region mean historical proxy was AUD 84,792 versus AUD 23,279/MW-year, with a paired-fold mean-delta 95% interval of AUD 3,079.62–6,912.10
- Decision-aware release gates rejected scenario-CVaR despite a positive mean because unseen fold-tail lift was negative, and rejected Chronos-2 after only 2/5 regions improved and the moving-block economic interval crossed zero
- A pinned MiniCheck-Flan-T5-Large sentence-support gate rejected 90% of controlled counterfactuals but recalled only 45% of supported official claims (67.5% balanced accuracy), so the semantic verifier remains offline rather than being promoted on model reputation
- Alibaba Cloud SG stack with FastAPI, Elasticsearch, Redis and Prometheus; 140/140 bounded loopback checks passed with P95 1.911 s
- 111 tests plus Ruff, strict mypy, dependency audit, Prometheus validation and secret scanning pass in GitHub Actions
- Economic figures are historical spot-market proxies with a user-supplied cycling cost, excluding CAPEX, fixed O&M, network fees, FCAS and investment returns
- Repository: [`australian-energy-market-intelligence-agent`](https://github.com/larry-liyuanfan/australian-energy-market-intelligence-agent)

### 3. Climate Claim Verification RAG

Reproducible search-and-ranking laboratory for climate claim verification, separated from unsupported leaderboard claims.

- Verified Spartan build over 1,208,827 evidence passages: BM25 in 40.33 s (126.3 MB) and Qwen3-Embedding-0.6B 1,024-d vectors + FAISS FlatIP in 1,696.77 s (5.13 GB artifact, 21.54 GB MaxRSS)
- A same-dimension 4B dense-encoder resource gate reduced sampled Recall@5 from 0.950 to 0.925, tied F1/MRR, encoded about 7.1x slower and used about 5.5x the peak Torch GPU memory; the full rebuild was deliberately stopped
- HNSW retained 0.9961 Recall@5 versus FlatIP ground truth while reaching 3,060.64 in-memory batch QPS and 12.88 ms single-query P50 on the fixed 154-query/32-thread benchmark
- BM25+dense RRF lifted fixed-dev Recall@5/Evidence F1 from 0.1721/0.1168 to 0.2709/0.1785
- Balanced RRF/Qwen3-Reranker-4B fusion over 7,700 pairs reached 0.3153/0.2131; four 5,000-sample paired intervals versus RRF were positive, with P95 4.82 s/query
- HNSW+RRF remains the latency default; 4B fusion is an offline dev-selection profile, not independent-test generalisation. An 8B same-pilot gate tied F1/Recall, slightly lowered MRR and raised P95 by 60.8%, so no full 8B run was submitted. IVF-PQ failed its quality gate; no leaderboard claim is made
- Claim-grouped hard-negative InfoNCE/LoRA adaptation retained the 0.6B encoder and improved full-corpus official-dev Recall@5 from 0.2793 to 0.2970, MRR from 0.3633 to 0.3869 and F1 from 0.07253 to 0.07544; all paired intervals were positive
- Candidate-agreement and text-aware routers cut 4B calls but preserved too little of the quality gain, so neither was promoted. The old LambdaMART result was invalidated after finding injected, unretrieved positives; a candidate-supported correction is under exact-SHA evaluation, with no new LTR quality claim yet
- 46 tests plus CLI and Spartan/Slurm assets for reproducible indexing, adaptation and ablation
- Repository: [`climate-claim-verification-rag`](https://github.com/larry-liyuanfan/climate-claim-verification-rag)

### 4. Wildfire Burn-window Decision Support

Deterministic, explainable domain tools for agents operating over large spatiotemporal climate data.

- Typed prescription rules, temporal alignment, continuous-window extraction, limiting-factor attribution, and sensitivity analysis
- Xarray/Dask data pipeline with checkpointable Spartan execution assets
- Greedy, nominal, max-min and empirical lower-tail CVaR MILPs with independent objective/feasibility certificates plus HiGHS optimality-gap/bound metadata
- In a 30-seed synthetic benchmark, nominal MILP improved mean utility by 1.79% over the best greedy (95% interval 0.91%-2.77%); CVaR improved mean held-out P05 utility by 1.42% versus nominal (95% interval 0.25%-3.25%)
- Agent-facing rejection reason codes and neighbouring crew-capacity counterfactuals explain scheduling trade-offs; their deltas are not LP shadow prices, causal effects or money
- Golden fixtures and 49 tests for schemas, rule boundaries, no-lookahead alignment, checkpoint/resume and feasible schedules
- A full-year public ARCO-ERA5 screen evaluated 8,283,312 cell-hours and retained 1,391,401 weather-only necessary-condition passes; these are not burn windows or safety claims
- The private Group44 code is staged on Spartan at exact commit `8724a295` with a reusable runtime image. Results remain synthetic utility or public-reanalysis scale evidence—not dollars, realised hectares or fire-risk reduction—because `yzhang3504` still lacks read access to the located `punim1257/Group44` VicClim6 path
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
