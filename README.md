

# Multivariate Time Series Anomaly Detection and Root Cause Analysis

A curated collection of datasets for multivariate time series anomaly detection (TSAD) and root cause analysis (RCA).

---

## Table of Contents

- [Recent Datasets and Benchmarks (2024-2026)](#recent-datasets-and-benchmarks-2024-2026)
- [Repository Structure](#repository-structure)
- [Core Stack (2025-2026)](#core-stack-2025-2026)
- [Categories](#categories)
- [Contributing](#contributing)

---

## Recent Datasets and Benchmarks (2024-2026)

### 1. RCAEval (WWW 2025 / ASE 2024)

Comprehensive benchmark for microservice root cause analysis.

- 9 datasets
- 735 failure cases
- Includes metrics, traces, and logs
- Systems: Online Boutique, Sock Shop, Train Ticket

GitHub: https://github.com/alibaba-research/RCAEval

---

### 2. Amazon PetShop Root Cause Analysis

Synthetic and semi-real benchmark for microservice RCA developed by Amazon Science.

- Injected failures
- Multivariate telemetry
- RCA labels
- Suitable for causal propagation analysis

GitHub: https://github.com/amazon-science/petshop-rca

---

### 3. BARO

Metric-based RCA benchmark and evaluation framework.

- Systems: Online Boutique, Sock Shop, Train Ticket
- Fault types: CPU, memory, latency injections

GitHub: https://github.com/NetManAIOps/BARO

---

### 4. LEMMA-RCA (2024)

Multimodal benchmark for low-level failure root cause analysis.

- Modalities: metrics, logs, traces
- Domains: IT systems, OT systems, water systems, microservices

Website: https://lemma-rca.github.io/

Paper: *LEMMA-RCA: A Multi-modal Benchmark for Low-level Failure Root Cause Analysis in IT and OT Systems*

---

### 5. Syncause Benchmark

Benchmark focused on observability-driven RCA pipelines.

GitHub: https://github.com/OpenObservability/syncause

---

### 6. HolisticRCA

Cloud-native RCA benchmark and framework.

GitHub: https://github.com/huangzx/HolisticRCA

---

### 7. AERCA (ICLR 2025 Oral)

Granger-causal root cause analysis for multivariate time series.

GitHub: https://github.com/AERCA-Paper/AERCA

---

### 8. RootCLAM

Causal inference framework for anomaly localization.

GitHub: https://github.com/NetManAIOps/RootCLAM

---

### 9. C-GATS (Amazon Science)

Conditional synthetic anomaly generation framework.

- Generates level shifts, contextual anomalies, and point anomalies

Paper: *Conditional Synthetic Anomaly Generation for Time Series Anomaly Detection*

---

### 10. GutenTAG

Synthetic time series anomaly generation framework.

- Multivariate support
- Configurable anomaly injection
- Benchmark-oriented design

GitHub: https://github.com/Wickus/GutenTAG

---

### 11. mTADS

Synthetic benchmark suite for anomaly detection.

GitHub: https://github.com/TimeSeriesBench/TSB-AD

---

### 12. Mulan (2024)

Cross-modal root cause analysis using logs, metrics, and causal discovery.

Paper: *Mulan: Multi-Modal Root Cause Analysis*

---

### 13. causRCA Dataset (2026)

Industrial benchmark with causal graph annotations.

- 92 variables
- Digital twin generated failures
- Explicit causal structures

Paper: *causRCA: Causal Root Cause Analysis for Industrial Systems*

---

### 14. Conditional Attribution RCA (2026)

Explainable RCA framework for industrial multivariate systems.

- Evaluated on SWaT and MSDS
- Focus on temporal localization
- Dependency-preserving attribution

Paper: *Conditional Attribution for Root Cause Analysis in Multivariate Systems*

---

### 15. Industrial Counterfactual RCA (2024)

Counterfactual reasoning framework for industrial RCA.

Paper: *Counterfactual Reasoning for Root Cause Analysis in Industrial Systems*

---

### 16. ProRCA (2025)

Probabilistic causal RCA framework and Python package.

- Synthetic anomaly injection
- Causal pathway tracing

Paper: *ProRCA: Probabilistic Causal RCA*

---

### 17. SWaT

Industrial water treatment anomaly detection dataset.

- Multivariate sensor streams
- Attack scenarios
- Frequently used for RCA evaluation

Dataset Portal: https://itrust.sutd.edu.sg/datasets/

---

### 18. WADI

Large-scale industrial multivariate anomaly dataset.

Dataset Portal: https://itrust.sutd.edu.sg/datasets/




### Key Research Directions

* Counterfactual RCA
* Causal discovery
* Multimodal reasoning
* Temporal attribution
* Graph-based RCA
* Foundation models for observability
* Explainable anomaly detection
* Industrial digital twins



