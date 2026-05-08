# Awesome Time Series Anomaly Detection and Root Cause Analysis Datasets

A curated list of public datasets, synthetic generators, and benchmarks for multivariate time series anomaly detection (TSAD), root cause analysis (RCA), and observability-driven AIOps research.

This README is designed to help readers decide **before clicking a link** whether a resource matches their problem. Each entry summarizes the task fit, telemetry type, available ground truth, and access caveats.

## Contents

- [Quick Decision Guide](#quick-decision-guide)
- [How to Read the Tables](#how-to-read-the-tables)
- [Recent Datasets and Benchmarks](#recent-datasets-and-benchmarks)
- [Established Public Datasets](#established-public-datasets)
- [Synthetic Data and Anomaly Generation](#synthetic-data-and-anomaly-generation)
- [Research Directions](#research-directions)
- [Contributing](#contributing)

## Quick Decision Guide

| If you are looking for... | Start with | Why |
| --- | --- | --- |
| Microservice RCA with multiple telemetry types | [RCAEval](https://github.com/phamquiluan/RCAEval), [LEMMA-RCA](https://lemma-rca.github.io/), [MSDS](https://github.com/sedrac3/msds) | These cover service incidents with metrics, logs, traces, or multi-source observability data. |
| Metric-only RCA or anomaly localization | [BARO](https://github.com/phamquiluan/baro), [AERCA](https://github.com/AERCA-Paper/AERCA), [RootCLAM](https://github.com/NetManAIOps/RootCLAM) | These are better fits when the model operates mainly on time-series metrics or causal signals. |
| Industrial or cyber-physical TSAD | [SWaT](https://itrust.sutd.edu.sg/datasets/), [WADI](https://itrust.sutd.edu.sg/datasets/), [SKAB](https://www.kaggle.com/datasets/dsv/2693815) | These focus on sensors, actuators, water systems, and physical-process anomalies. |
| Server monitoring anomaly detection | [SMD](https://github.com/NetManAIOps/OmniAnomaly), [NAB](https://github.com/numenta/NAB) | These are common baselines for infrastructure and streaming anomaly detection. |
| Broad TSAD baselines | [UCR Time Series Anomaly Archive](https://www.cs.ucr.edu/~eamonn/time_series_data_2018/), [NAB](https://github.com/numenta/NAB) | These are useful when you need general anomaly detection benchmarks rather than RCA-specific data. |
| Synthetic anomaly generation | [GutenTAG](https://github.com/Wickus/GutenTAG), [mTADS / TSB-AD](https://github.com/TimeSeriesBench/TSB-AD), C-GATS | These help when you need controllable anomaly types, stress tests, or generated benchmark data. |
| Causal graphs or causal RCA | causRCA, [AERCA](https://github.com/AERCA-Paper/AERCA), [RootCLAM](https://github.com/NetManAIOps/RootCLAM) | These are closer to root-cause ranking, causal attribution, or causal-structure experiments. |

## How to Read the Tables

| Column | Meaning |
| --- | --- |
| **Best fit** | The problem this resource is most likely to help with. |
| **Signals** | The data types used, such as metrics, logs, traces, sensors, topology, or causal graphs. |
| **Ground truth** | What labels or evaluation targets are available from the resource description. |
| **Before clicking** | The main reason to open the link, plus any caveat known from this list. |

## Recent Datasets and Benchmarks

| Resource | Best fit | Signals | Ground truth | Before clicking |
| --- | --- | --- | --- | --- |
| [RCAEval](https://github.com/phamquiluan/RCAEval) | Benchmarking microservice RCA across multiple systems | Metrics, traces, logs | Failure cases and RCA targets | Good first stop for modern microservice RCA evaluation. Covers Online Boutique, Sock Shop, and Train Ticket. |
| [Amazon PetShop Root Cause Analysis](https://github.com/amazon-science/petshop-root-cause-analysis) | Studying injected failures and causal propagation in a service benchmark | Multivariate telemetry | RCA labels | Useful when you want synthetic or semi-real service incidents from an Amazon Science benchmark. |
| [BARO](https://github.com/phamquiluan/baro) | Metric-based RCA on cloud-native benchmark systems | Metrics | Fault injection labels | Choose this when logs and traces are not central to your method. |
| [LEMMA-RCA](https://lemma-rca.github.io/) | Multimodal RCA across IT, OT, and microservice settings | Metrics, logs, traces | Low-level failure labels | Useful when your method combines telemetry modalities instead of using metrics only. |
| [Syncause Benchmark](https://github.com/Syncause/syncause-benchmark) | Observability-driven RCA pipeline evaluation | Observability telemetry | RCA-oriented benchmark targets | Open this if your work is about end-to-end RCA workflows over observability data. |
| [HolisticRCA](https://github.com/baiyanquan/HolisticRCA) | Cloud-native RCA framework comparison | Cloud telemetry | RCA-oriented benchmark targets | Useful for cloud-native incident analysis and holistic RCA methods. |
| [AERCA](https://github.com/AERCA-Paper/AERCA) | Granger-causal RCA for multivariate time series | Multivariate time series | Root-cause ranking / causal targets | Best fit if your model explicitly uses temporal causal relationships. |
| [RootCLAM](https://github.com/NetManAIOps/RootCLAM) | Causal anomaly localization | Metrics and causal signals | Anomaly localization targets | Useful when the output is a likely root metric or causal source. |
| Mulan | Cross-modal RCA with causal discovery | Logs, metrics | RCA targets | Canonical link still needed. Keep it as a candidate if you need log-metric fusion. |
| causRCA Dataset | Industrial RCA with explicit causal structure | Multivariate time series, causal graph | Causal graph annotations | Canonical link still needed. Promising when graph ground truth matters. |
| Conditional Attribution RCA | Explainable RCA and temporal attribution | Multivariate time series | Temporal localization / attribution targets | Canonical link still needed. Relevant for explainability and dependency-preserving attribution. |
| Industrial Counterfactual RCA | Counterfactual reasoning for industrial incidents | Industrial time series | Counterfactual RCA targets | Canonical link still needed. Relevant if your method asks "what would have happened otherwise?" |
| ProRCA | Probabilistic causal RCA with synthetic injection | Synthetic anomalies, causal pathways | Causal pathway targets | Canonical link still needed. Relevant for probabilistic RCA and generated faults. |

## Established Public Datasets

| Resource | Best fit | Signals | Ground truth | Before clicking |
| --- | --- | --- | --- | --- |
| [SWaT](https://itrust.sutd.edu.sg/datasets/) | Industrial control-system anomaly detection and RCA | Water-treatment sensors and actuators | Attack / anomaly scenarios | Strong fit for cyber-physical systems. Access may require following the dataset portal process. |
| [WADI](https://itrust.sutd.edu.sg/datasets/) | Larger-scale water-distribution anomaly detection | Water-distribution sensors | Attack / anomaly scenarios | Use when SWaT is too small or you need a larger industrial process. Access is through the same portal. |
| [Skoltech Anomaly Benchmark (SKAB)](https://www.kaggle.com/datasets/dsv/2693815) | Physical testbed TSAD with injected anomalies | Water-circulation telemetry | Injected anomaly labels | Useful for fast experiments on multivariate industrial-like data. Hosted on Kaggle. |
| [UCR Time Series Anomaly Archive](https://www.cs.ucr.edu/~eamonn/time_series_data_2018/) | General-purpose TSAD benchmarking | Mostly univariate time series | Anomaly labels | Good for broad algorithm baselines, less suitable for RCA or multivariate observability. |
| [Server Machine Dataset (SMD)](https://github.com/NetManAIOps/OmniAnomaly) | Server metric anomaly detection | 38-dimensional machine metrics | Anomaly labels | Common baseline for infrastructure TSAD across 28 machines. |
| [Multi-Source Distributed System (MSDS)](https://github.com/sedrac3/msds) | Distributed-system AIOps research | Traces, logs, metrics | Incident / anomaly labels | Open this when you need more than metrics and care about distributed-system telemetry. |
| [Numenta Anomaly Benchmark (NAB)](https://github.com/numenta/NAB) | Streaming anomaly detection | Real-world and artificial time series | Anomaly windows / labels | Useful for streaming evaluation, less focused on multivariate RCA. |
| [Hugging Face Time Series Datasets](https://huggingface.co/datasets?other=time-series) | Discovering additional datasets | Varies by dataset | Varies by dataset | This is an index, not one benchmark. Use it when the curated list does not cover your domain. |

## Synthetic Data and Anomaly Generation

| Resource | Best fit | Signals / Output | Control level | Before clicking |
| --- | --- | --- | --- | --- |
| C-GATS | Conditional synthetic anomaly generation | Generated time series anomalies | Level shifts, contextual anomalies, point anomalies | Canonical link still needed. Relevant when anomaly type control is more important than a fixed dataset. |
| [GutenTAG](https://github.com/Wickus/GutenTAG) | Configurable synthetic TSAD experiments | Synthetic univariate or multivariate time series | Configurable anomaly injection | Choose this when you want to generate repeatable test cases rather than download a fixed benchmark. |
| [mTADS / TSB-AD](https://github.com/TimeSeriesBench/TSB-AD) | Synthetic and benchmark TSAD evaluation | Benchmark datasets and tooling | Benchmark-suite level | Useful when you want a broader TSAD benchmark suite with synthetic data support. |

## Research Directions

- Counterfactual root cause analysis
- Causal discovery for multivariate time series
- Multimodal RCA over metrics, logs, traces, and topology
- Temporal attribution and timestamp-level localization
- Graph-based RCA for service dependencies and causal propagation
- Foundation models for observability and AIOps
- Explainable anomaly detection
- Industrial digital twins and simulator-generated incidents
- Synthetic anomaly generation with controllable severity and dependency structure

## Contributing

Contributions are welcome. To keep the list useful before readers click through, new entries should include:

- A stable project, paper, dataset, or code link.
- The primary task: TSAD, RCA, anomaly localization, causal discovery, or synthetic generation.
- The telemetry type: metrics, logs, traces, sensors, topology, causal graph, or mixed.
- The available ground truth: anomaly labels, RCA labels, fault injections, causal graph, attack windows, or none.
- One sentence explaining when a reader should choose it over nearby alternatives.
- Licensing notes, access requirements, or account requirements when known.

Prefer primary sources such as the official repository, dataset portal, benchmark page, or paper page.
