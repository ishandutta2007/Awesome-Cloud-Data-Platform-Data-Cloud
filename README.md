# Awesome-Cloud-Data-Platform-Data-Cloud

# Awesome-Cloud-Data-Platform-Data-Cloud
**Top Cloud Data Platform Data Cloud (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Lakehouse Architectures, Open Table Formats, Federated Query Engines & Self-Hosted Analytics Platforms*
**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Cloud Data Platforms & Data Clouds**. These tools enable organizations to store, govern, and analyze data at scale—from fully managed platforms with unified governance and AI integration to open-source engines and table formats that give teams complete control over their data architecture and vendor independence.

**Examples** include Snowflake AI Data Cloud, Databricks Data Intelligence Platform, Google BigQuery, AWS Redshift, Microsoft Fabric, Cloudera CDP, Teradata VantageCloud, Oracle ADW, SingleStore, and Dremio (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted analytics, open lakehouse formats, and federated query infrastructure. **Critical note**: The open-source data platform landscape has matured to the point where a fully open lakehouse stack is viable—**Apache Iceberg** is the de facto open table format , **StarRocks** and **Trino** handle query acceleration and federation , and **Apache Polaris** and **Gravitino** provide open catalogs . No single open-source project matches Databricks' unified platform experience, but a composed stack covers most analytical workloads.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Databricks Data Intelligence Platform](https://www.databricks.com/)**
  **Lakehouse platform built on Apache Spark**, combining data lake flexibility with warehouse performance. Uses **Delta Lake** (open format, now with UniForm for Iceberg compatibility), **Unity Catalog** for unified governance across tables/volumes/models, and **Photon** vectorized engine . Ranked #1 overall in Futurum's 2026 Data Intelligence Platforms report (92.5), launching Lakebase for sub-second Postgres write-backs . **Pricing**: Consumption-based (DBUs). **Free tier**: Community Edition limited. **Best for**: code-first teams focused on ML and data engineering wanting open lakehouse architecture .

- **[Snowflake AI Data Cloud](https://www.snowflake.com/)**
  **Cloud-native data warehouse** with separation of storage, compute, and services. Ranked Elite status (91.9) in Futurum 2026, having **open-sourced Polaris Catalog for Apache Iceberg** and launched native Snowflake Postgres . Supports Iceberg tables and cross-cloud data sharing without copying . **Pricing**: Consumption-based (Snowflake credits). **Free tier**: Trial credits. **Best for**: teams wanting fully managed simplicity with multi-cloud flexibility and minimal operational overhead .

- **[Google Cloud BigQuery](https://cloud.google.com/bigquery)**
  **Fully serverless data warehouse** on Google Cloud with zero infrastructure management. **BigQuery ML** for building models in SQL; **BI Engine** for sub-second dashboards; real-time streaming ingestion . **Pricing**: On-demand and capacity-based options. **Free tier**: Limited. **Best for**: Google Cloud organizations wanting a truly serverless platform with no cluster management .

- **[AWS Redshift](https://aws.amazon.com/redshift/)**
  **Cloud data warehouse** deeply integrated with AWS ecosystem (S3, Glue, SageMaker, Kinesis). **Redshift Spectrum** queries S3 directly; **AQUA** accelerates large scans; supports Apache Iceberg read/write . **Pricing**: Provisioned or Serverless. **Free tier**: AWS Free Tier applies. **Best for**: AWS-centric organizations wanting deep native integration .

- **[Microsoft Fabric](https://www.microsoft.com/fabric)**
  **Unified data platform** built on OneLake, combining data integration, analytics, and Power BI. **Fabric Databases (GA)** and **Cosmos DB in Fabric (preview)** enable zero-ETL operational-to-analytical flows . Ranked Elite (90.4) in Futurum 2026 despite optimistic-concurrency write bottlenecks across OneLake . **Pricing**: Capacity-based (CUs). **Free tier**: Trial available. **Best for**: Microsoft-centric organizations with existing Power BI and Azure identity investments .

- **[Dremio](https://www.dremio.com/)**
  **Open data lakehouse platform** with SQL query engine built on Apache Arrow, querying data directly on S3/lakes without separate warehouse. **Arctic** provides Git-like Iceberg catalog management . **Pricing**: Quote-only. **Free tier**: Trial available. **Best for**: teams wanting lakehouse analytics without data duplication into a warehouse.

- **[SingleStore](https://www.singlestore.com/)**
  **Real-time distributed SQL database** for operational analytics, combining transactions and analytics in one engine. **Pricing**: Quote-only; free Starter Workspace. **Free tier**: Yes. **Best for**: workloads needing sub-second analytics on fresh operational data.

- **[Teradata VantageCloud](https://www.teradata.com/)**
  **Enterprise data warehouse** with cloud-native architecture and AI/ML integration. **Pricing**: Quote-only. **Free tier**: None. **Best for**: large enterprises with existing Teradata investments migrating to cloud.

- **[Oracle Autonomous Data Warehouse](https://www.oracle.com/autonomous-database/)**
  **Self-driving cloud data warehouse** with automated tuning, patching, and scaling. **Pricing**: Consumption-based (OCPUs). **Free tier**: Limited Always Free tier. **Best for**: Oracle-centric enterprises wanting minimal DBA overhead.

- **[Cloudera Data Platform](https://www.cloudera.com/)**
  **Hybrid data platform** with shared data experience (SDX) across on-premises and cloud. **Pricing**: Quote-only. **Free tier**: None. **Best for**: organizations with existing Hadoop/Cloudera investments needing hybrid deployment.

## Open-Source GitHub Projects

- **[Apache Iceberg](https://github.com/apache/iceberg)**
  **Open table format for huge analytic tables** (Apache 2.0) — **the de facto standard for open lakehouse storage**, with the broadest multi-engine support and neutral Apache governance . **Features**: Hidden partitioning and partition evolution; snapshot isolation with ACID; schema evolution; time travel; supports Parquet, ORC, Avro. Industry momentum: Databricks acquired Tabular (Iceberg creators), AWS shipped S3 Tables, Snowflake open-sourced Polaris . **Tech stack**: Java. **Deploy**: Integrated with compute engines; catalogs provided separately. **Trade-off**: **Table format only**—needs catalog (Polaris/Nessie) and storage (S3/MinIO). **Best for**: organizations building vendor-neutral lakehouses where multiple engines must access the same tables simultaneously.

- **[StarRocks](https://github.com/StarRocks/starrocks)**
  **High-performance OLAP database with lakehouse acceleration** (Apache 2.0, Linux Foundation) — **the most mature open-source option for accelerating BI queries on lake data** . **Features**: **Multi-Catalog** reads Iceberg/Hudi/Delta/Paimon directly without data movement; **asynchronous incremental materialized views** with automatic query rewrite; **MySQL protocol** for BI tool compatibility; **vectorized + CBO + Runtime Filter** for performance; **separation of storage and compute** (v3.0+) . **Tech stack**: C++, Java. **Deploy**: Self-hosted (Kubernetes, Docker) or cloud. **Trade-off**: **Acceleration layer, not source of truth**—materialized views are copies; lake remains authoritative. Larger learning curve than ClickHouse for simple deployments. **Best for**: teams with lakehouse architecture needing sub-second BI performance (p95 < 1s) and high concurrency (>100 QPS) .

- **[Trino](https://github.com/trinodb/trino)**
  **Distributed SQL query engine for federated analytics** (Apache 2.0) — **the standard for querying across heterogeneous data sources without moving data** . **Features**: Connector architecture queries HDFS, Hive, Kafka, MySQL, PostgreSQL, Iceberg, Delta, and more; no storage of its own—purely a query layer; massively parallel processing; used by Datto for Iceberg analytics achieving 2–3× query speedup . **Tech stack**: Java. **Deploy**: Self-hosted (Kubernetes, bare metal). **Trade-off**: **Query engine only**—no storage, no catalog management, no materialized views. **Best for**: organizations with data scattered across multiple systems needing a unified SQL query interface—especially those with existing Iceberg lakes .

- **[Apache Doris](https://github.com/apache/doris)**
  **MPP analytical database** (Apache 2.0) — **the full-featured open-source OLAP engine** with strong real-time update support and MySQL compatibility . **Features**: **Unique Key model** for upserts and row-level updates; **high-concurrency point queries** (thousands QPS); automatic load balancing and replication; Hive/Iceberg catalog support; active Apache community . **Tech stack**: C++, Java. **Deploy**: Self-hosted. **Trade-off**: **Lake integration less mature than StarRocks**; not designed for extreme single-table aggregation like ClickHouse. **Best for**: enterprise reporting and ad-hoc analytics needing both high concurrency and real-time updates, especially in MySQL-centric environments .

- **[ClickHouse](https://github.com/ClickHouse/ClickHouse)**
  **Column-oriented database for real-time analytics** (Apache 2.0) — **the fastest engine for single-table aggregation and log analytics** . **Features**: **MergeTree engine family** with rich indexing and partitioning; vectorized execution; excellent for logs, time-series, and wide-table aggregations; single-node can handle billions of rows with second-level queries . **Tech stack**: C++. **Deploy**: Self-hosted or ClickHouse Cloud. **Trade-off**: **Weak JOIN performance**; **not suitable for high-frequency updates** (ReplacingMergeTree deduplicates but doesn't guarantee real-time visibility); **lake integration weaker** than StarRocks/Doris . **Best for**: log analysis, user behavior analytics, and read-heavy single-table aggregation where JOINs are minimal.

- **[Apache Polaris](https://github.com/apache/polaris)**
  **Open-source Iceberg catalog** (Apache 2.0, Apache TLP February 2026) — **the open-source foundation of Snowflake's Open Catalog offering** . **Features**: **Pure Iceberg REST specification**; **RBAC** with principals, roles, and privileges; **credential vending** for scoped short-lived access; **catalog federation** to front existing Hive Metastore or other catalogs . **Tech stack**: Java. **Deploy**: Self-hosted. **Trade-off**: **Iceberg-only**—no support for models, volumes, or vectors as first-class citizens. **Best for**: teams wanting a clean, foundation-governed Iceberg catalog with federation for gradual migration from Hive .

- **[Apache Gravitino](https://github.com/apache/gravitino)**
  **Federated metadata lake catalog** (Apache 2.0, Apache TLP 2025) — **the most ambitious open-source catalog for heterogeneous metadata** . **Features**: **Federates metadata across Hive, Iceberg, Hudi, Kafka, and relational databases**; unified API; credential vending; access control; nascent lineage and MCP support . **Tech stack**: Java. **Deploy**: Self-hosted. **Trade-off**: **Documentation incomplete and confusing**, making implementation challenging ; no first-class model/vector support like Unity Catalog. **Best for**: organizations with multiple existing catalogs needing a federated metadata layer without migrating everything to one format .

- **[Lakekeeper](https://github.com/lakekeeper/lakekeeper)**
  **Lightweight Iceberg REST catalog in Rust** (Apache 2.0) — **the easiest open-source catalog to deploy and evaluate** . **Features**: **Rust-based** for performance and low resource usage; **pure Iceberg REST**; access control; credential vending; **excellent documentation and working Docker playground** . **Tech stack**: Rust. **Deploy**: Self-hosted (Docker). **Trade-off**: **Iceberg-only**; no broader entity support (models, volumes); smaller community than Polaris or Gravitino. **Best for**: teams wanting a simple, well-documented Iceberg catalog with minimal operational overhead—especially those new to open lakehouse architecture .

### Additional Strong Open-Source Options

- **Apache Hudi** — Open data lake platform with upserts and incremental processing (Apache 2.0). **Note**: Strong for CDC and streaming upserts (Uber, Robinhood use cases) but proved less efficient for bulk loading in benchmarks compared to Delta/Iceberg . **Best for**: streaming-heavy ingestion with record-level mutations.
- **Delta Lake** — Open table format from Databricks (Apache 2.0). **Note**: Fastest for bulk loading in benchmarks; strongest when Spark is the primary engine . **Best for**: Spark-centric teams already in Databricks ecosystem.
- **Apache Nessie** — Git-like catalog for Iceberg (Apache 2.0). **Note**: Catalog-level branching and tagging for data versioning; not focused on multi-modal assets . **Best for**: teams needing Git-flow for data with dev/stage/prod isolation.

**Frameworks for building custom systems**: Combine **MinIO** or S3 for storage with **Apache Iceberg** as the table format, **Apache Polaris** or **Lakekeeper** as the catalog, and **StarRocks** or **Trino** for query—creating a fully open-source lakehouse. **None of these match Databricks' unified experience or Snowflake's managed simplicity**, but for teams prioritizing vendor independence and cost control, the open stack is production-viable.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Cloud data platforms handling enterprise data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls, encryption, and audit logging.
- **The "managed platform" vs. "query engine" vs. "table format" vs. "catalog" distinction is critical.** **Snowflake, Databricks, BigQuery, Redshift, Fabric, Dremio, SingleStore, Teradata, Oracle ADW, and Cloudera** are **managed platforms**—they bundle storage, compute, and governance. **StarRocks, Trino, Doris, and ClickHouse** are **query engines**—they query data but don't store it (Trino) or store their own data (StarRocks/Doris/ClickHouse). **Apache Iceberg, Delta Lake, and Hudi** are **table formats**—they define how data files are organized. **Polaris, Gravitino, Lakekeeper, and Nessie** are **catalogs**—they manage metadata and access. **Choose based on whether you need a complete platform, a query layer, a format, or a catalog.**
- **Apache Iceberg is the safest bet for long-term openness.** With the broadest multi-engine support, neutral Apache governance, and industry momentum (Databricks acquiring Tabular, AWS S3 Tables, Snowflake Polaris), it has become the de facto open standard . **Delta Lake has the largest installed base** but is anchored to Databricks . **Hudi excels at streaming upserts** but has a narrower position .
- **StarRocks is the leading open-source lakehouse accelerator.** Its asynchronous incremental materialized views with automatic query rewrite, Multi-Catalog lake access, and MySQL protocol make it the pragmatic choice for BI acceleration on Iceberg/Hudi/Delta . **ClickHouse remains the fastest for single-table aggregation** but is weak on JOINs and unsuitable for high-frequency updates .
- **Trino is the federation standard** but not a platform. It queries everything and stores nothing—**pair it with Iceberg for a complete lakehouse query layer** .
- **Lakekeeper is the easiest open catalog to start with**, with excellent documentation and a working Docker playground . **Polaris is the foundation-governed choice** with Snowflake backing . **Gravitino is the federation choice** for heterogeneous metadata, but its documentation is a barrier .
- **Pricing opacity varies.** Snowflake, Databricks, BigQuery, Redshift, Fabric, and SingleStore publish consumption-based pricing. Dremio, Teradata, Oracle ADW, and Cloudera require sales contact. **Validate with direct vendor conversations against your workload shape—steady vs. spiky consumption changes the calculus significantly** .
- Self-hosted open-source solutions require proper infrastructure (object storage, compute clusters, catalog services), security hardening, and ongoing maintenance. **Lakehouse components are business-critical**—ensure your deployment meets your organization's reliability and security requirements before migrating production workloads.

---

**Made for data engineers, platform architects, and organizations building transparent cloud data platform solutions.**
Let's make Cloud Data Platforms & Data Clouds more open, data-driven, and vendor-independent.
