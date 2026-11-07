# Hi, I’m Chandra

I like building things that change things.

I’m a developer working with Python, distributed systems, and data. These days, I’m exploring AI and crypto, and building open-source tools. I’m interested in work closer to the trading desk, especially research tools, market data, and the systems that support trading.

I previously worked in Millennium’s Enterprise Risk Technology team (July 2022–February 2026). Before that, I built AI backend services at Marsview.ai, acquired by Eltropy.

[My website](https://iamknownstranger.github.io/) · [LinkedIn](https://www.linkedin.com/in/chandra-sekhar-mullu/) · [Email me](mailto:sekharmullu@gmail.com)

### What I’ve worked on

At Millennium, I designed and built a distributed stress-calculation framework covering 2M+ positions and 4,000 scenarios. I also worked on on-demand Ray/Dask clusters, an Arrow-based risk calculation library with Python and Java bindings, and a data-orchestration library used by more than 100 developers.

That work involved taking systems from design through to production, including the data pipelines and interfaces people used to get the results.

### What I’m building here

**[Portfolio Pulse](https://github.com/iamknownstranger/portfolio-pulse)** is where I work on portfolio analytics and backtesting in Python. The calculations live separately from the Streamlit interface so I can test them on their own. The backtest tracks execution timing, costs, cash, and holdings; it’s a research tool with simulated trades.

If you’re looking through the code, I’d start with the [backtest engine](https://github.com/iamknownstranger/portfolio-pulse/blob/main/common/backtesting.py) and its [regression tests](https://github.com/iamknownstranger/portfolio-pulse/blob/main/tests/test_backtesting_regressions.py). The [methodology notes](https://github.com/iamknownstranger/portfolio-pulse/blob/main/docs/BACKTEST_RESEARCH.md) explain the assumptions.

**[Igloo](https://github.com/igloodb/igloodb)** is an experimental SQL engine I’m working on in Rust, using DataFusion and Arrow. It queries PostgreSQL and Parquet together and caches results in memory. It currently runs in one process; distributed execution and Apache Iceberg integration are still on the roadmap.

One useful part to look at is [filter pushdown](https://github.com/igloodb/igloodb/blob/main/src/pushdown.rs): deciding what can run at the source while preserving the query’s meaning. There are [differential tests](https://github.com/igloodb/igloodb/blob/main/tests/pushdown.rs) for that, along with a [website and docs](https://igloodb.github.io/). Agent interfaces, broader ADBC support, and native CDC foundations are in a [separate draft preview](https://github.com/igloodb/igloodb/pull/32).

### What I work with

Python, SQL, NumPy, pandas, Polars, SciPy, Ray, Dask, Arrow, PostgreSQL, and Redis. For interfaces, I’ve used Plotly Dash and Streamlit; for delivery, AWS, Linux, Docker, Kubernetes, pytest, and GitHub Actions. My Rust work is in Igloo.

If you’re building trading tools, research platforms, or market data systems, or want to talk open source, [send me an email](mailto:sekharmullu@gmail.com).
