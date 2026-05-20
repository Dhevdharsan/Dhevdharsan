# Hi, I'm Dhev 👋

I'm a Machine Learning Engineer and M.S. Computer Science student at UMass Amherst (GPA: 4.0, graduating May 2027). I've shipped production AI systems from scratch — a RAG-powered log intelligence platform, a live agentic research agent, and a distributed ML pipeline over 1M+ flight records — and held the work to a standard rigorous enough to publish twice: peer-reviewed papers in medical imaging AI in Frontiers in Radiology (2025) and Springer ICAECT (2024). I'm an AWS Certified Solutions Architect with end-to-end experience across model development, backend infrastructure, and cloud deployment. I'm actively looking for Summer 2026 AI/ML and Software Engineering internships where I can build things that ship.

---

## 📫 Connect

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?style=flat&logo=linkedin)](https://linkedin.com/in/dhevdharsan-bs)
[![Email](https://img.shields.io/badge/Email-grey?style=flat&logo=gmail)](mailto:dbhavanisati@umass.edu)
[![AWS](https://img.shields.io/badge/AWS%20Certified-FF9900?style=flat&logo=amazonaws&logoColor=white)](https://cp.certmetrics.com/amazon/en/public/verify/credential/a232b2aeccc24b59acfa3f3196ac1778)

---

## 🧠 What I work on

- **LLM systems** — RAG pipelines, agentic AI, prompt engineering, vector search with pgvector
- **ML pipelines** — anomaly detection, medical imaging, unsupervised clustering, transfer learning, game-playing agents
- **Distributed systems** — PySpark, MLlib, distributed hyperparameter tuning, big data pipelines
- **Production backends** — async FastAPI microservices, Docker, Redis, PostgreSQL, deployed to cloud
- **Applied research** — NRIQA for LDCT imaging (Frontiers in Radiology 2025), cataract detection (Springer ICAECT 2024)

**Languages:** Python · SQL · JavaScript · TypeScript

---

## 🚀 Projects

### [LogSense AI — Unsupervised Anomaly Detection & Log Analytics](https://github.com/Dhevdharsan)
`Python` `FastAPI` `PostgreSQL` `pgvector` `Redis` `Llama 3` `Docker` `Next.js`

A production-grade containerized platform that detects anomalies in log streams and explains them in plain English using a RAG pipeline. An unsupervised ML pipeline (TF-IDF → Isolation Forest → DBSCAN) processes 500 logs in 1.5s, surfacing 4.8% anomalies across 15 behavioral clusters. Llama 3 (Ollama) retrieves relevant cluster context via pgvector embeddings and generates root cause summaries delivered on a real-time Next.js dashboard.

---

### [Agentic Research Assistant — Live AI Agent](https://github.com/Dhevdharsan)
`Python` `FastAPI` `OpenAI API` `BeautifulSoup4` `ThreadPoolExecutor` `Render`

A live agentic system that concurrently scrapes the web, extracts structured facts using JSON-mode LLM calls, and attributes every output to a source URL — eliminating hallucinations at the retrieval layer. Real-time FastAPI streaming delivers results as they arrive; production deployment on Render required resolving Nginx load-balancer buffering and a pydantic-core Rust compilation conflict.

---

### [GauntletAgent — Heads-Up Limit Texas Hold'em AI](https://github.com/Dhevdharsan)
`Python` `Alpha-Beta Minimax` `Q-Learning` `Genetic Algorithm` `Monte Carlo`

A poker-playing AI agent built on a 6-stage decision pipeline: precomputed preflop hand tables, time-bounded Monte Carlo post-flop evaluation, opponent profiling across 5 behavioral styles (maniac → calling station), a 3-tier bluff layer (semi-bluff, slow play, river bluff), and depth-3 Alpha-Beta Minimax search with profile-weighted opponent nodes instead of worst-case assumptions. Weights were trained in two phases — Q-Learning for initial policy across 3 difficulty tiers, then a Genetic Algorithm over a 4-opponent Gauntlet to escape a local optimum and converge to a tight-aggressive profile that folds under pressure and values strong hands heavily.

---

### [Smart Expense Analyzer](https://github.com/Dhevdharsan)
`Python` `FastAPI` `Next.js` `Celery` `Redis` `Supabase` `XGBoost` `Hugging Face` `LangChain` `Tesseract` `Chart.js`

A full-stack AI-powered expense tracking app built for the UMass Five College community (CS 520, Spring 2026) that eliminates manual receipt entry through an event-driven asynchronous pipeline: Tesseract OCR extracts merchant, amount, and date from uploaded receipt images; facebook/bart-large-mnli zero-shot classifies each expense into one of 10 categories; XGBoost forecasts next-month spend with burnout probability using lag features and a sigmoid function. The API gateway returns HTTP 202 in under 200ms by offloading all OCR and NLP computation to a Celery/Redis worker, with Supabase Realtime pushing status to the client — backed by 46 automated tests at 63% backend coverage.

---

### [FlightDelayPredictor — Distributed ML Pipeline](https://github.com/Dhevdharsan/FlightDelayPredictor)
`PySpark` `Spark MLlib` `Databricks` `SQL` `Parquet` `GBT` `Logistic Regression`

A scalable distributed ML system built on Apache Spark to predict domestic U.S. flight delays across 1M+ records — a dataset that triggers memory spilling and extreme latency in single-node Pandas environments. PySpark's Lazy Evaluation and Catalyst Optimizer handle preprocessing and feature engineering (StringIndexing, One-Hot Encoding for high-cardinality airline/airport fields, VectorAssembler), while Gradient Boosted Trees trained via distributed Grid Search hyperparameter tuning achieved AUC 0.6535 after resolving severe class imbalance through downsampling.

---

### [Diagnosis-Based NRIQA & LDCT Image Enhancement](https://github.com/Dhevdharsan) — *Published, Frontiers in Radiology 2025*
`Python` `scikit-learn` `OpenCV` `SHAP` `GCP T4 GPU`

A No-Reference Image Quality Assessment framework for 1,000 low-dose CT scans using 25 SHAP-selected features (GLCM, LBP, frequency-domain); SVR + Grid Search + 100-fold CV achieved PLCC 0.9671, surpassing all prior JND baselines (best previous: 0.955). A Laplacian sharpening post-processing pipeline improved 96% of scans, with 88% independently scored high-quality by radiologists.

---

### [Cataract Detection via Deep Learning — Comparative Study](https://github.com/Dhevdharsan) — *Published, Springer ICAECT 2024 (Scopus & WoS)*
`Python` `PyTorch` `TensorFlow` `ResNet-50` `GCP`

Fine-tuned ResNet-50 on 1,015 retinal images with augmentation (40° rotation, 20% zoom/shear), achieving 83% accuracy and outperforming EfficientNet (70%) across precision, recall, F1, and AUC. A systematic transfer learning comparison from ImageNet weights demonstrated ResNet-50's advantage on limited labeled medical data — findings published and indexed in Scopus and Web of Science.

---

## 📄 Research Publications

- **Bhavani Satish Kumar, D. et al.** "Diagnosis-Based No-Reference Image Quality Assessment for LDCT." *Frontiers in Radiology*, 2025. DOI: 10.3389/fradi.2025.1704113 [[Link]](https://www.frontiersin.org/journals/radiology/articles/10.3389/fradi.2025.1704113/full)
- **Balasubramanian, N., Bhavani Satish Kumar, D. et al.** "Cataract Detection via Deep Learning: A Comparative Study." *Springer ICAECT 2024* (Scopus & Web of Science). [[Link]](https://www.google.co.in/books/edition/Advances_in_Electrical_and_Computer_Tech/dW9fEQAAQBAJ?hl=en&gbpv=1&pg=PA106&printsec=frontcover)

---

## 🏅 Certifications

- AWS Certified Solutions Architect – Associate (July 2024) · [Verify](https://cp.certmetrics.com/amazon/en/public/verify/credential/a232b2aeccc24b59acfa3f3196ac1778)
- AWS Cloud Practitioner Essentials (November 2023)
