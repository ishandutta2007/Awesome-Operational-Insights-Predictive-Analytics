# Awesome-Operational-Insights-Predictive-Analytics

# Awesome Operational Insights & Predictive Analytics

> A curated list of top Operational Insights and Predictive Analytics platforms — both SaaS/Hosted commercial observability and BI suites and open-source alternatives for anomaly detection, forecasting, and root-cause analysis.
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [Datadog](#datadog)
  - [Dynatrace](#dynatrace)
  - [New Relic](#new-relic)
  - [Splunk](#splunk)
  - [Tableau](#tableau)
  - [Power BI](#power-bi)
- [Open-Source Software](#-open-source-software)
  - [Netdata](#netdata)
  - [Coroot](#coroot)
  - [OpenObserve](#openobserve)
  - [Monoscope](#monoscope)
  - [Scry](#scry)
  - [NexusBI](#nexusbi)
  - [NVIDIA Kumo](#nvidia-kumo)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Operational Insights and Predictive Analytics platforms. These are not open-source but are included as reference points for feature comparison.

### Datadog
**Type:** Full-stack observability with anomaly detection and forecasting
Datadog provides infrastructure monitoring, APM, log management, and synthetic monitoring with built-in anomaly detection and forecasting. It correlates metrics, traces, and logs to surface operational insights, with dashboards and alerting that can trigger on predicted thresholds.

### Dynatrace
**Type:** AI-driven observability with predictive root cause
Dynatrace uses its Davis AI engine for automatic discovery, dependency mapping, and AI-powered root cause analysis. It predicts performance degradation and surfaces operational insights without manual configuration, positioned for enterprises needing automated problem isolation.

### New Relic
**Type:** Observability with applied intelligence
New Relic offers APM, infrastructure monitoring, and applied intelligence for anomaly detection, with usage-based pricing and a generous free tier. It provides dashboards, alerting, and predictive insights across the full stack.

### Splunk
**Type:** Machine data analytics and predictive insights
Splunk ingests and analyzes machine data for operational intelligence, with SPL queries, anomaly detection, and predictive analytics. It is the long-standing enterprise standard for log-based operational insights, with extensive security and IT use cases.

### Tableau
**Type:** Visual analytics with predictive modeling
Tableau provides visual data exploration and dashboarding with built-in predictive modeling (forecasting, clustering, trend lines). It is positioned for business analysts wanting to explore operational data visually and surface insights without deep statistical expertise.

### Power BI
**Type:** Business analytics with AI insights
Power BI provides business intelligence with AI-powered insights, natural language queries, and forecasting capabilities. It is the natural choice for Microsoft-centric organizations wanting operational analytics integrated with their existing data stack.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Operational Insights and Predictive Analytics tools. The open-source ecosystem spans **real-time monitoring with ML**, **observability with root-cause analysis**, **log/metric/trace platforms with anomaly detection**, and **specialized predictive libraries**.

### Netdata
**Stack:** C / Go | **License:** GPL-3.0 (Agent)
Netdata provides real-time, per-second metrics collection with a built-in dashboard, **ML-based anomaly detection**, and alerting—all with zero manual setup . It uses only ~5% CPU and ~150 MiB RAM by default, and a University of Amsterdam study found it the most energy-efficient monitoring tool among those compared, with no impact on monitored workloads . It supports 800+ data collection integrations, stores metrics in tiered write-once files, and includes **zero-touch machine learning** for proactive problem detection . Alert notifications support PagerDuty, Slack, Teams, email, Discord, Telegram, Jira, and ServiceNow .  
**Best for:** Hands-on troubleshooting and real-time performance analysis with built-in ML anomaly detection, with minimal resource overhead.

### Coroot
**Stack:** Go / ClickHouse | **License:** Apache-2.0
Coroot is an open-source observability and APM tool with **AI-powered Root Cause Analysis**, combining metrics, logs, traces, continuous profiling, and SLO-based alerting with predefined dashboards and inspections . It continuously audits telemetry data to highlight issues and weak spots in infrastructure . The **anomaly-detection** repository compares statistical methods, LLMs, and Jev-style decision models on synthetic p99 latency scenarios, with a minute-by-minute replay site . It also provides a Kubernetes lab that reproduces real production incidents for testing root-cause-analysis tools .  
**Best for:** Teams wanting AI-powered RCA across metrics, logs, and traces with a focus on infrastructure auditing and incident reproduction.

### OpenObserve
**Stack:** Rust | **License:** AGPL-3.0
OpenObserve is an open-source observability platform for logs, metrics, traces, RUM (web, Android, iOS), session replay, pipelines, SLO, and LLM observability . It is positioned as a "sophisticated, simple and highly performant alternative to Datadog, Splunk, and Elasticsearch with 140x lower storage costs and single binary deployment" . It provides the data foundation for operational insights with cost-efficient storage.  
**Best for:** Teams wanting a cost-efficient, self-hosted observability backend for logs, metrics, and traces, accepting that ML/forecasting must be layered on top.

### Monoscope
**Stack:** Go / S3-compatible storage | **License:** AGPL-3.0
Monoscope is an open-source observability platform that stores telemetry in **S3-compatible storage**, with **natural language queries**, **AI agents that run on a schedule to detect anomalies**, and email reports . It is OpenTelemetry-native with 750+ integrations, live tail, and unified views correlating logs, metrics, traces, and session replays . The **MCP server** exposes itself as a Model Context Protocol server so Claude Desktop, Cursor, or custom agents can search events, manage monitors, and run composite workflows like natural-language-to-KQL and LLM-assisted root cause .  
**Best for:** Teams wanting cost-efficient S3-backed observability with scheduled AI anomaly detection and AI agent integration.

### Scry
**Stack:** Python / PyTorch / FastAPI | **License:** Apache-2.0
Scry predicts infrastructure failure states from a stream of metrics, sorting each resource into one of **five operational states** (NORMAL, PRE_SCALE, PRE_FAILURE, ACTIVE_DEGRADATION, ANOMALY) with a recommended action and priority . It uses a **dual-encoder temporal VAE plus deep embedded clustering** (X-DEC model) trained on your own metrics, with an optional Chronos forecasting layer. It is **data-source agnostic** (Parquet/CSV from local or S3/GCS/ADLS/MinIO via DuckDB) and runs fully offline with no cloud dependencies . The FastAPI service exposes `/predict`, `/forecast`, `/drift`, `/anomaly`, and `/accuracy` endpoints.  
**Best for:** Teams wanting a focused, trainable predictive failure model for infrastructure metrics, accepting that you bring your own data and train your own model.

### NexusBI
**Stack:** FastAPI / React / PostgreSQL | **License:** Open Source (GitHub)
NexusBI is an AI-powered natural-language BI platform with **NL→SQL→dashboard**, a power-user SQL editor, **root-cause analysis**, **proactive AI digest**, an agentic copilot, and a semantic/trust layer . Key operational insight features include **forecasting**, **anomaly detection**, and a **"Why?" hierarchical root-cause tree** that decomposes a metric into a multi-level driver tree with contribution percentages and a deterministic fallback when AI is unavailable . It supports RBAC, row-level security, embedded analytics, and white-label. The project started as a course project but is actively developed with PRs, tests, and CI .  
**Best for:** Teams wanting a self-hosted BI platform with natural language querying, forecasting, anomaly detection, and hierarchical root-cause analysis, accepting a younger project.

### NVIDIA Kumo
**Stack:** Python / PyTorch | **License:** Open Model (NVIDIA)
NVIDIA Kumo is a family of **open models and libraries for making predictions from tabular, relational, and time-series data**, including **forecasting**, **anomaly detection**, and risk scoring . The **Kumo Forecast** model explores time-series forecasting for demand planning and capacity management, with support for short- and long-horizon forecasting and optional retrieval of historical patterns. **Kumo Anomaly** uses diffusion-based modeling for time-series imputation and anomaly detection with adaptive thresholds . Libraries install via `pip install kumo-engine`, with Snowflake and Databricks integrations available. It is not a monitoring platform but a predictive modeling toolkit.  
**Best for:** Data science teams wanting pretrained models for forecasting and anomaly detection on structured/tabular data, accepting that you integrate them into your own pipelines.

---

## 📊 Comparison at a Glance

| Software | License | Stack | Anomaly Detection | Forecasting | Root Cause | Self-Hosted | Best For |
|----------|---------|-------|-------------------|-------------|------------|-------------|----------|
| **Datadog** | Proprietary | Cloud | ✅ | ✅ | (Correlation) | ❌ | Full-stack observability |
| **Dynatrace** | Proprietary | Cloud | ✅ | ✅ | ✅ Davis AI | ❌ | AI-driven RCA |
| **Splunk** | Proprietary | Cloud/On-prem | ✅ | ✅ | (SPL) | (On-prem) | Log-based insights |
| **Netdata** | GPL-3.0 | C/Go | ✅ ML | (Check) | ❌ | ✅ | Real-time ML monitoring |
| **Coroot** | Apache-2.0 | Go/ClickHouse | ✅ | ❌ | ✅ AI RCA | ✅ | AI-powered observability |
| **OpenObserve** | AGPL-3.0 | Rust | (Layer on top) | ❌ | ❌ | ✅ | Cost-efficient telemetry |
| **Monoscope** | AGPL-3.0 | Go/S3 | ✅ AI agents | ❌ | (LLM) | ✅ | S3-backed + AI agents |
| **Scry** | Apache-2.0 | Python/PyTorch | ✅ X-DEC | ✅ Chronos | ❌ | ✅ | Predictive failure states |
| **NexusBI** | Open Source | FastAPI/React | ✅ | ✅ | ✅ "Why?" tree | ✅ | NL BI + root-cause |
| **Kumo** | Open Model | Python/PyTorch | ✅ | ✅ | ❌ | ✅ (Library) | Pretrained predictive models |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Operational Insights or Predictive Analytics tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source.

**Note on the open-source ecosystem:** Operational insights and predictive analytics is a broad category where the right tool depends on whether you need **real-time monitoring with ML** (Netdata), **AI-powered root cause analysis** (Coroot), **cost-efficient telemetry storage** (OpenObserve, Monoscope), **predictive failure modeling** (Scry, Kumo), or **natural-language BI with root-cause** (NexusBI). **Netdata** is the most mature open-source option for zero-config ML anomaly detection , while **Coroot** provides the strongest AI-driven RCA for infrastructure . For teams wanting to build custom predictive models, **Scry** and **NVIDIA Kumo** offer trainable foundations .

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
