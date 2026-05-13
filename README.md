# Liyuan Fan

Master of Data Science at the University of Melbourne, focused on LLM applications, RAG, agentic analytics, and data-driven decision support.

I work on systems that turn messy domain data into searchable evidence, interpretable signals, and decision-ready outputs.

## Featured Projects

### Climate Claim Verification RAG

Built a multi-stage fact-checking pipeline for climate science claims, covering claim-evidence retrieval and four-way claim classification.

- Method: Bi-Encoder retrieval, Cross-Encoder reranking, Transformer / open-source LLM verification, hard negative sampling
- Evaluation: public evaluation rank 5; H-mean 0.35, Evidence Retrieval F-score 0.26, Claim Classification Accuracy 0.57
- Repository: `climate-claim-verification-rag`

### Wildfire Burn-window Decision Support

Developed a prescribed-burn window analysis workflow over gridded climate data for Victoria, translating expert prescriptions into rule-based operational windows.

- Data: VicClim6 NetCDF climate data, 1972-2024, Victoria, about 4 km grid resolution, hourly variables
- Method: Xarray/Dask processing, variable alignment, burn suitability rules, limiting-factor analysis, threshold sensitivity analysis
- Result: 2024 demo identified 6.49% all-condition burn windows and clear monthly/hourly operating patterns
- Repository: `wildfire-burn-window-decision-support`

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