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

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS/Hosted Platforms](#saashosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## Sector Overview & Market Dynamics

The global Cloud Data Platform market is valued at approximately **$45–50 billion** (expanding at a 17–25% CAGR toward a trillion-dollar cloud ecosystem by 2026+), powered by GenAI workloads, open table formats, and decoupled storage-compute architectures. The sector exhibits **moderate-to-high fragmentation**: while foundational compute and storage are anchored by hyperscaler oligopolies (AWS, Microsoft Azure, Google Cloud) and dominant lakehouse platforms (Databricks, Snowflake), the broader landscape remains intensely fragmented across specialized open formats, federated query engines, metadata catalogs, and regional sovereign clouds.

## SaaS/Hosted Platforms

| Platform | Company Valuation / Revenue Size | Starting Pricing | Free Tier / Trial Limit | Best For / Key Differentiators |
|:---|:---|:---|:---|:---|
| **[Microsoft Fabric](https://www.microsoft.com/fabric)** | ~$3.88 Trillion (Public Market Cap) | Starting at **$0.18/CU-hour** (Pay-as-you-go F2 tier, ~$262/month; 1-year reserved from ~$154/month) + OneLake storage ($0.023/GB/mo) | **60-day free trial** with access to high-capacity trial SKUs (e.g., F64 equivalent) and 1 TB OneLake storage | Microsoft-centric enterprise ecosystems with heavy Power BI investments seeking unified OneLake SaaS governance. |
| **[Google Cloud BigQuery](https://cloud.google.com/bigquery)** | ~$3.46 Trillion (Alphabet Public Market Cap) | **$6.25 per TiB** scanned (on-demand query pricing); active storage at **$0.020 per GiB/month** | **Always Free Tier**: 1 TiB of query data processed per month and 10 GiB of active storage per month; plus **$300 credit 90-day GCP trial** | Serverless SQL analytics with zero cluster management, integrated BigQuery ML, and BI Engine acceleration. |
| **[AWS Redshift](https://aws.amazon.com/redshift/)** | ~$2.59 Trillion (Amazon Public Market Cap) | Provisioned instances starting at **$0.543/hour** (`dc2.large`); Redshift Serverless starting at **$0.375/RPU-hour** (~$1.50/hour for minimum 4 RPUs) | **$300 credit 90-day trial** for Redshift Serverless; or **2-month free trial** of provisioned `dc2.large` (up to 750 hours/month) | AWS-native ecosystems requiring tight integration with S3, AWS Glue, SageMaker, and Redshift Spectrum. |
| **[Oracle Autonomous Data Warehouse](https://www.oracle.com/autonomous-database/)** | ~$360–430 Billion (Public Market Cap) | Starting at **$0.336 per ECPU/hour** (License Included, min 2 ECPUs = $0.672/hour); BYOL starts at **$0.0807 per ECPU/hour** | **Always Free Tier**: 2 Autonomous Database instances with 1 OCPU / 20 GB storage each; plus **$300 credit 30-day OCI trial** | Oracle shops seeking automated self-tuning, automated patching, zero-maintenance operational lakehouse analytics. |
| **[Databricks Data Intelligence Platform](https://www.databricks.com/)** | ~$190 Billion (Private Valuation) | Serverless / Jobs compute starting at **~$0.07 to $0.15/DBU**; standard compute at **$0.20–$0.40/DBU** (plus underlying cloud VM infrastructure) | **Databricks Free Edition** (forever free serverless environment with daily quota for learning/prototyping); plus **14-day trial with $400 in trial credits** | Code-first engineering and data science teams using Apache Spark, Delta Lake (UniForm), and Unity Catalog. |
| **[Snowflake AI Data Cloud](https://www.snowflake.com/)** | ~$110–115 Billion (Public Market Cap) | Standard Edition starting at **$2.00 per Snowflake Credit** (on-demand compute); cloud storage from **$23/TB/month** | **30-day free trial with $400 in trial credits** (no credit card required upfront) | Fully managed SQL lakehouse/warehouse simplicity, multi-cloud data sharing, and Apache Iceberg (Polaris) support. |
| **[Cloudera Data Platform](https://www.cloudera.com/)** | ~$5.3 Billion (Private Equity Buyout Valuation) | Starting at **$0.04/CCU-hour** (Data Hub) to **$0.07/CCU-hour** (Data Warehouse / Engineering Core rate; all-purpose at $0.20/CCU-hr) | **60-day cloud trial** available via direct Cloudera tenant registration; no self-service always-free tier | Hybrid enterprise architectures with legacy Hadoop/Cloudera estates transitioning to public/private clouds via SDX. |
| **[Teradata VantageCloud](https://www.teradata.com/)** | ~$3.2 Billion (Public Market Cap) | VantageCloud Lake on AWS starting from software usage contracts + AWS compute (~$0.50–$2.00+/node-hr depending on shape) | **Teradata VantageCloud Developer Edition** on AWS Marketplace (free software license up to 2 nodes, pay only EC2/EBS infrastructure costs) | Large-scale enterprises with heavy historical on-premises Teradata migrations requiring high-concurrency complex SQL. |
| **[Dremio](https://www.dremio.com/)** | ~$2.0 Billion (Private Valuation) | Dremio Cloud Standard starting at **$0.20 per DCU** (Dremio Compute Unit, time-based consumption) | **Forever-free Standard tier** (restricted to Small engines and limited users/tables); plus **30-day trial with $400 in trial credits** | Lakehouse query federation on Apache Arrow and direct querying over Amazon S3/ADLS without data duplication. |
| **[SingleStore](https://www.singlestore.com/)** | ~$1.0–1.3 Billion (Private Valuation) | Standard Edition dedicated workspaces starting at **$0.99/hour** (`S-00` tier: 2 vCPU, 16 GB RAM at 0.25 credits/hr; $3.96/credit) | **Always Free Shared Tier** (Helios Shared Edition for developer testing/prototyping); plus **free trial credits** on Standard Edition | Sub-second operational analytics and real-time HTAP ingestion combining transactional and analytical workloads. |

## Open-Source GitHub Projects

Curated list of open-source table formats, query engines, catalogs, and analytics execution frameworks, ranked by GitHub community stars:

1. **[ClickHouse](https://github.com/ClickHouse/ClickHouse)** [![GitHub stars](https://img.shields.io/github/stars/ClickHouse/ClickHouse?style=social&color=white)](https://github.com/ClickHouse/ClickHouse/stargazers)  
   **Column-oriented database for real-time analytics** (Apache 2.0) — The fastest open-source engine for single-table aggregation, time-series, and log analytics with vectorized execution. Features MergeTree storage engines, advanced data skipping indices, and sub-second execution across billions of records.

2. **[Apache Spark](https://github.com/apache/spark)** [![GitHub stars](https://img.shields.io/github/stars/apache/spark?style=social&color=white)](https://github.com/apache/spark/stargazers)  
   **Unified analytics engine for large-scale data processing** (Apache 2.0) — The benchmark standard for distributed data pipelines, batch transformations, streaming (Structured Streaming), and machine learning across open lakehouse architectures.

3. **[DuckDB](https://github.com/duckdb/duckdb)** [![GitHub stars](https://img.shields.io/github/stars/duckdb/duckdb?style=social&color=white)](https://github.com/duckdb/duckdb/stargazers)  
   **In-process SQL OLAP database management system** (MIT) — The "SQLite for analytics", delivering columnar vectorized execution within application runtimes. Directly reads and queries Apache Iceberg, Delta Lake, and Parquet files in S3 and local storage without infrastructure overhead.

4. **[Apache Doris](https://github.com/apache/doris)** [![GitHub stars](https://img.shields.io/github/stars/apache/doris?style=social&color=white)](https://github.com/apache/doris/stargazers)  
   **MPP analytical database** (Apache 2.0) — High-concurrency OLAP engine with native MySQL protocol compatibility, real-time update handling via Unique Key upserts, inverted indexing for full-text search, and lakehouse catalog acceleration.

5. **[Trino](https://github.com/trinodb/trino)** [![GitHub stars](https://img.shields.io/github/stars/trinodb/trino?style=social&color=white)](https://github.com/trinodb/trino/stargazers)  
   **Distributed SQL query engine for federated analytics** (Apache 2.0) — The industry standard for querying heterogeneous data sources at massive scale without moving data. Connects natively to Apache Iceberg, Delta Lake, Hive, relational databases, Kafka, and NoSQL stores.

6. **[StarRocks](https://github.com/StarRocks/starrocks)** [![GitHub stars](https://img.shields.io/github/stars/StarRocks/starrocks?style=social&color=white)](https://github.com/StarRocks/starrocks/stargazers)  
   **Next-gen sub-second OLAP lakehouse engine** (Apache 2.0, Linux Foundation) — High-performance vectorized query engine featuring asynchronous incremental materialized views with automated rewrite, separation of storage and compute, and multi-catalog lake querying (Iceberg, Delta Lake, Hudi, Paimon).

7. **[Apache Arrow DataFusion](https://github.com/apache/arrow-datafusion)** [![GitHub stars](https://img.shields.io/github/stars/apache/arrow-datafusion?style=social&color=white)](https://github.com/apache/arrow-datafusion/stargazers)  
   **Extensible SQL query engine and execution framework written in Rust** (Apache 2.0) — Blazing-fast in-memory columnar query engine utilizing Apache Arrow memory format; powering the next generation of custom data platforms, distributed query engines, and database systems.

8. **[Apache Iceberg](https://github.com/apache/iceberg)** [![GitHub stars](https://img.shields.io/github/stars/apache/iceberg?style=social&color=white)](https://github.com/apache/iceberg/stargazers)  
   **Open table format for huge analytic tables** (Apache 2.0) — The de facto open standard for modern lakehouses with vendor-neutral Apache governance. Delivers full ACID transactions, partition evolution, schema evolution, hidden partitioning, and time-travel querying across engines.

9. **[Delta Lake](https://github.com/delta-io/delta)** [![GitHub stars](https://img.shields.io/github/stars/delta-io/delta?style=social&color=white)](https://github.com/delta-io/delta/stargazers)  
   **Open-source storage framework for ACID lakehouses** (Apache 2.0) — Storage layer powering lakehouses with transaction logs, schema enforcement, time travel, and UniForm (Universal Format) for cross-format reading across Iceberg and Hudi readers.

10. **[Apache Hudi](https://github.com/apache/hudi)** [![GitHub stars](https://img.shields.io/github/stars/apache/hudi?style=social&color=white)](https://github.com/apache/hudi/stargazers)  
    **Transactional data lake platform** (Apache 2.0) — Specialized in streaming ingestion, change data capture (CDC), and record-level mutations with Copy-On-Write and Merge-On-Read storage primitives and built-in indexing.

11. **[Apache Pinot](https://github.com/apache/pinot)** [![GitHub stars](https://img.shields.io/github/stars/apache/pinot?style=social&color=white)](https://github.com/apache/pinot/stargazers)  
    **Real-time distributed OLAP datastore** (Apache 2.0) — Designed for low-latency, user-facing real-time analytics at ultra-high throughput (tens of thousands of QPS), indexing streaming data from Kafka/Kinesis and batch data from S3/HDFS.

12. **[Unity Catalog](https://github.com/unitycatalog/unitycatalog)** [![GitHub stars](https://img.shields.io/github/stars/unitycatalog/unitycatalog?style=social&color=white)](https://github.com/unitycatalog/unitycatalog/stargazers)  
    **Open universal catalog for data and AI governance** (Apache 2.0) — Provides unified metadata, data access control, credential vending, and governance across tables (Delta, Iceberg), unstructured files, and AI models.

13. **[Apache Gravitino](https://github.com/apache/gravitino)** [![GitHub stars](https://img.shields.io/github/stars/apache/gravitino?style=social&color=white)](https://github.com/apache/gravitino/stargazers)  
    **Federated metadata lakehouse catalog** (Apache 2.0) — Unifies heterogeneous metadata governance across relational databases, open table formats (Iceberg, Hudi), messaging systems (Kafka), and AI assets with centralized security and credential vending.

14. **[Apache Polaris](https://github.com/apache/polaris)** [![GitHub stars](https://img.shields.io/github/stars/apache/polaris?style=social&color=white)](https://github.com/apache/polaris/stargazers)  
    **Open-source Iceberg REST catalog** (Apache 2.0) — Neutral, multi-engine catalog based on the Apache Iceberg REST specification. Implements centralized RBAC, credential vending for cloud storage, and catalog federation.

15. **[Apache Nessie](https://github.com/projectnessie/nessie)** [![GitHub stars](https://img.shields.io/github/stars/projectnessie/nessie?style=social&color=white)](https://github.com/projectnessie/nessie/stargazers)  
    **Git-like transactional catalog for Iceberg and Delta** (Apache 2.0) — Brings Git concepts (branches, tags, commits, and merges) to data lakehouse catalogs, facilitating isolated dev/stage/prod environments and data experimentation.

16. **[Lakekeeper](https://github.com/lakekeeper/lakekeeper)** [![GitHub stars](https://img.shields.io/github/stars/lakekeeper/lakekeeper?style=social&color=white)](https://github.com/lakekeeper/lakekeeper/stargazers)  
    **Rust-native Iceberg REST catalog** (Apache 2.0) — Ultra-lightweight, high-performance catalog implementing the Iceberg REST standard with access control, multi-tenant workspace separation, and low operational footprint.

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
