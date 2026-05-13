# Liyuan Fan

Master of Data Science at the University of Melbourne, focused on LLM applications, RAG, agentic analytics, and data-driven decision support.

I work on systems that turn messy domain data into searchable evidence, interpretable signals, and decision-ready outputs.

## Featured Projects

### Climate Claim Verification RAG

Built a multi-stage fact-checking pipeline for climate science claims, covering claim-evidence retrieval and four-way claim classification.

- Method: Bi-Encoder retrieval, Cross-Encoder reranking, Transformer / open-source LLM verification, hard negative sampling
- Evaluation: public evaluation rank 5; H-mean 0.35, Evidence Retrieval F-score 0.26, Claim Classification Accuracy 0.57
- Repository: [`climate-claim-verification-rag`](https://github.com/larry-liyuanfan/climate-claim-verification-rag)

### Movie Review Intelligence Dashboard

Built a privacy-safe movie-review analytics project that converts semi-structured review data into movie-level aggregate features, LLM-ready evidence documents, and a static portfolio dashboard.

- Method: public-release data audit, feature aggregation, sentiment-signal summarization, TF-IDF retrieval, prompt-ready recommendation context
- Result: packaged 246 movie-level records and 246 retrieval documents without raw comments, usernames, profile URLs, or crawler artifacts
- Demo: [`GitHub Pages`](https://larry-liyuanfan.github.io/movie-review-intelligence-dashboard/)
- Repository: [`movie-review-intelligence-dashboard`](https://github.com/larry-liyuanfan/movie-review-intelligence-dashboard)

### Fulfillment Optimization Decision Support

Built a full decision-optimization pipeline for e-commerce order-wave release and workforce scheduling, from baseline data generation to integrated MIP modeling, scenario experiments, and solver reproducibility audit.

- Method: Gurobi mixed-integer programming, sequential exact benchmark, scenario simulation, validation checks, replication study
- Result: reduced labor cost by 2.58%-13.55% across four scenarios; integrated model was cheaper in 39/40 replicated instances with zero late orders
- Demo: [`GitHub Pages`](https://larry-liyuanfan.github.io/fulfillment-optimization-decision-support/)
- Repository: [`fulfillment-optimization-decision-support`](https://github.com/larry-liyuanfan/fulfillment-optimization-decision-support)

### Geospatial Burn-window Demo

Public synthetic-data demo derived from a confidential prescribed-burn decision-support project. The original research repository remains private; this demo only shows the transferable technical workflow.

- Method: toy gridded climate variables, rule-based suitability masks, limiting-factor analysis, threshold sensitivity analysis
- Skills: Xarray/Dask-style geospatial data processing, NetCDF-style data modeling, interpretable decision-support outputs
- Repository: [`geospatial-burn-window-demo`](https://github.com/larry-liyuanfan/geospatial-burn-window-demo)

### HPC Social Language Count

Sanitized data-engineering portfolio project for parallel language counting over social-media-style NDJSON records on an HPC cluster.

- Method: MPI map-reduce style counting, SLURM batch jobs, runtime comparison across node/core configurations
- Skills: distributed data processing, semi-structured text parsing, scalable aggregation, performance evaluation
- Repository: [`hpc-social-language-count`](https://github.com/larry-liyuanfan/hpc-social-language-count)

### Housing Safety Agent Analytics

Built a housing safety analytics prototype with ReAct-style data exploration and sentiment analysis. The public portfolio repository is pending because the source project is hosted on a private university GitLab.

- Method: ReAct agent workflow, BERT/VADER sentiment signals, Elasticsearch retrieval, serverless data collection
- Status: documentation will be published after source export and sanitization

## Technical Focus

- LLM / NLP: RAG, ReAct Agent, retrieval evaluation, prompt-ready context generation, BGE-M3, Bi-Encoder, Cross-Encoder, BERT
- Data Science: statistical machine learning, sentiment signals, A/B testing, time-series analysis
- Data Engineering: Python, SQL, Pandas, PySpark, Xarray, Dask, Elasticsearch, NetCDF
- Optimization: MIP modeling, Gurobi, solver validation, decision support, reproducibility diagnostics
- Tools: Docker, Git, Fission Serverless, Claude Code, Copilot

## Contact

- Email: liyuan.fan.2@student.unimelb.edu.au
- LinkedIn: pending