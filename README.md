# Chandra Sekhar Mullu

**Quantitative Developer | Risk Technology | Python & Distributed Systems**

I build systems for financial risk calculations, portfolio research, and data-intensive applications. Previously a Quantitative Developer in Millennium's Enterprise Risk Technology team (July 2022 - February 2026); before that, an AI Backend Engineer at Marsview.ai, acquired by Eltropy.

[Portfolio](https://iamknownstranger.github.io/) · [LinkedIn](https://www.linkedin.com/in/chandra-sekhar-mullu/) · [Email](mailto:sekharmullu@gmail.com)

### Production experience

- **Risk computation:** designed and built a distributed stress-calculation framework spanning 2M+ positions and 4,000 scenarios.
- **Developer infrastructure:** built a data-orchestration library adopted by 100+ developers and on-demand Ray/Dask cluster provisioning with resource quotas and cost-aware autoscaling.
- **Data delivery:** implemented event-driven ETL for risk reporting, reducing reporting SLAs by three hours; built an Apache Arrow-based calculation library with Python and Java bindings.

### Selected public work

| Project | What it demonstrates | Explore |
| --- | --- | --- |
| **Portfolio Pulse** | Python portfolio analytics, risk metrics, constrained allocation, and cost-aware backtesting. Explicit execution timing, cash accounting, and walk-forward validation. | [Code](https://github.com/iamknownstranger/portfolio-pulse) · [Research methodology](https://github.com/iamknownstranger/portfolio-pulse/blob/main/docs/BACKTEST_RESEARCH.md) · [Regression tests](https://github.com/iamknownstranger/portfolio-pulse/blob/main/tests/test_backtesting_regressions.py) |
| **Igloo** | Experimental Rust SQL engine using DataFusion and Arrow: PostgreSQL/Parquet federation, conservative filter pushdown, PostgreSQL wire protocol, and an in-memory LRU/TTL result cache. | [Code](https://github.com/igloodb/igloodb) · [Website & docs](https://igloodb.github.io/) · [Pushdown implementation](https://github.com/igloodb/igloodb/blob/main/src/pushdown.rs) |

**Scope matters:** Portfolio Pulse is a research application with hypothetical results, not a live trading system. Igloo's default branch is single-node; distributed execution and Apache Iceberg integration are roadmap work. Its agent/ADBC/native-CDC work is a separate [draft preview](https://github.com/igloodb/igloodb/pull/32).

### Technical focus

- **Quant & research:** Python, SQL, NumPy, pandas, Polars, SciPy, portfolio/risk analytics, Plotly Dash, Streamlit.
- **Compute & data:** Ray, Dask, event-driven ETL, Apache Arrow, PostgreSQL, Redis; Rust and DataFusion in Igloo.
- **Delivery:** AWS, Linux, Docker, Kubernetes, pytest, GitHub Actions.

### A useful starting point for a technical conversation

- **Research correctness:** [Backtest engine](https://github.com/iamknownstranger/portfolio-pulse/blob/main/common/backtesting.py) - signals at close t execute at the next common close, with self-funded transaction costs and an execution ledger.
- **Query correctness:** [Pushdown tests](https://github.com/igloodb/igloodb/blob/main/tests/pushdown.rs) - compare pushed and unpushed results; exclude string ordering where PostgreSQL collation can disagree with Arrow.
- **Cache design:** [Arrow-native cache](https://github.com/igloodb/igloodb/blob/main/src/cache_layer.rs) - bounded entry count, TTL, shared record batches, and deterministic clock-based tests.

For quant-development and risk-technology conversations: **[sekharmullu@gmail.com](mailto:sekharmullu@gmail.com)**.
