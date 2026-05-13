# Liyuan Fan

Master of Data Science at the University of Melbourne, focused on LLM applications, RAG, agentic analytics, and data-driven decision support.

I work on systems that turn messy domain data into searchable evidence, interpretable signals, and decision-ready outputs.

## Featured Projects

### Climate Claim Verification RAG

Built a multi-stage fact-checking pipeline for climate science claims, covering claim-evidence retrieval and four-way claim classification.

- Method: Bi-Encoder retrieval, Cross-Encoder reranking, Transformer / open-source LLM verification, hard negative sampling
- Evaluation: public evaluation rank 5; H-mean 0.35, Evidence Retrieval F-score 0.26, Claim Classification Accuracy 0.57
- Repository: `climate-claim-verification-rag`

### Geospatial Burn-window Demo

Public synthetic-data demo derived from a confidential prescribed-burn decision-support project. The original research repository remains private; this demo only shows the transferable technical workflow.

- Method: toy gridded climate variables, rule-based suitability masks, limiting-factor analysis, threshold sensitivity analysis
- Skills: Xarray/Dask-style geospatial data processing, NetCDF-style data modeling, interpretable decision-support outputs
- Repository: `geospatial-burn-window-demo`

### HPC Social Language Count

Sanitized data-engineering portfolio project for parallel language counting over social-media-style NDJSON records on an HPC cluster.

- Method: MPI map-reduce style counting, SLURM batch jobs, runtime comparison across node/core configurations
- Skills: distributed data processing, semi-structured text parsing, scalable aggregation, performance evaluation
- Repository: `hpc-social-language-count`

### Housing Safety Agent Analytics

Built a housing safety analytics prototype with ReAct-style data exploration and sentiment analysis. The public portfolio repository is pending because the source project is hosted on a private university GitLab.

- Method: ReAct agent workflow, BERT/VADER sentiment signals, Elasticsearch retrieval, serverless data collection
- Status: documentation will be published after source export and sanitization

## Technical Focus

- LLM / NLP: RAG, ReAct Agent, BGE-M3, Bi-Encoder, Cross-Encoder, BERT
- Data Science: statistical machine learning, retrieval evaluation, A/B testing, time-series analysis
- Data Engineering: Python, SQL, Pandas, PySpark, Xarray, Dask, Elasticsearch, NetCDF
- Tools: Docker, Git, Fission Serverless, Claude Code, Copilot

## Contact

- Email: liyuan.fan.2@student.unimelb.edu.au
- LinkedIn: pending