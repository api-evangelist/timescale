<!-- fetched 2026-10-13 from https://www.tigerdata.com/docs/ by sweep-shape-compat.py; text extracted from the provider's own page -->

Tiger Data Documentation | Tiger Data Docs Skip to content Tiger Data Docs 
 Get started Get started Choose your setup 
 Tiger Console 
 Tiger CLI and MCP 
 Self-hosted TimescaleDB 
 News and updates Contribute to docs 
 Learn Learn Tutorials 
 Tiger Cloud 
 Tiger CLI and MCP 
 Capabilities and comparison 
 Data model 
 Hypertables 
 Hyperfunctions 
 Chunks and time buckets 
 Hypercore 
 Continuous aggregates (CAGGs) 
 Data lifecycle 
 Search 
 Glossary 
 Build Build Build with Tiger CLI and MCP 
 Quickstarts 
 Data lifecycle 
 Write and query data 
 Automate with jobs and policies 
 Spread data across storage tiers 
 Use hyperfunctions for analytics 
 Keep pre-computed aggregations up to date 
 Optimize storage and query speed 
 Make queries and schemas faster 
 Troubleshooting 
 Migrate Migrate Migrate to Tiger Cloud 
 Sync and stream 
 Upload files 
 Integrate Integrate Connect to Tiger Data 
 Type of tool 
 Industry 
 Platform 
 First party/third party 
 Technology 
 Troubleshooting 
 Deploy Deploy Tiger Cloud on AWS 
 Tiger Cloud on Azure 
 Self-hosted TimescaleDB 
 Managed Service for TimescaleDB 
 Limitations 
 Reference Reference TimescaleDB 
 TimescaleDB Toolkit 
 Tiger CLI Tiger MCP Tiger Cloud REST API 
 Search ⌘K Search Ctrl K 
 Start a free trial 
 0 Get started with Tiger Data 
 Choose your setup Compare Tiger Data products 
 Cloud-exclusive features 
 Compare TimescaleDB editions 
 Tiger Console 5-minute quickstart 
 Create a Tiger Cloud account 
 Create a Tiger Cloud service 
 Supported regions 
 Tiger CLI and MCP Get started with Tiger CLI 
 Integrate Tiger Cloud with your AI agent 
 Get started with the REST API 
 Self-hosted TimescaleDB 10-minute quickstart 
 Install self-hosted TimescaleDB 
 Connect your app 
 Supported platforms 
 News and updates Overview 
 Changelog 
 Release notes 
 Contribute to docs 
 1 Overview What is Tiger Data 
 Tiger Data architecture for real-time analytics 
 Tutorials Overview 
 Create Tiger Cloud services with Terraform 
 Simulate an IoT sensor dataset 
 Ingest real-time financial data 
 Analyze application events with UUIDv7 
 Build hybrid search with BM25 and vectors 
 Build a production RAG system with Postgres 
 Aggregate organizational data with AI agents 
 Analyze stock market data 
 Analyze NYC taxi data 
 Analyze Bitcoin blockchain 
 Analyze energy consumption 
 Visualize financial tick data with Grafana 
 Visualize transport and geospatial data with Grafana 
 Tiger Data cookbook 
 Tiger Cloud Tiger Cloud 
 Cloud-exclusive features 
 Tiger Cloud essentials 
 Tiger CLI and MCP 
 Capabilities and comparison Understand capabilities 
 Compare the features in Tiger Data products 
 Data model Design your data model 
 Wide, narrow, and medium tables 
 Primary keys, time columns, and uniqueness 
 Schema optimization 
 Hypertables Understand hypertables 
 Create and configure a hypertable 
 Partition a hypertable 
 Hypertable indexes 
 Hypertable operations 
 Hyperfunctions 
 Chunks and time buckets Understand chunks 
 Size hypertable chunks 
 Understand time buckets 
 Use time buckets 
 Manually drop chunks 
 Hypercore Understand hypercore 
 Compression methods 
 Continuous aggregates (CAGGs) Understand continuous aggregates 
 Time and continuous aggregates 
 Hierarchical continuous aggregates 
 Real-time aggregates 
 Materialized hypertables 
 Data lifecycle Understand the data lifecycle 
 Hypertables and chunks 
 Time buckets 
 Continuous aggregates 
 Hypercore and the columnstore 
 Tiered storage 
 Data retention 
 Search Key vector concepts for pgvector 
 Understand pg_textsearch and BM25 search 
 Understand pgvector and pgvectorscale 
 Glossary 
 2 Overview 
 Build with Tiger CLI and MCP Common tasks 
 Best practices for AI agents 
 Cookbook 
 Quickstarts Overview 
 Your first hypertable 
 Basic compression with hypercore 
 Data lifecycle Your first hypertable 
 Set up hypercore 
 Create a continuous aggregate 
 Manage storage and tiering 
 Create a retention policy 
 Create and manage custom jobs 
 Write and query data Write and query data 
 Write data Insert data 
 Update data 
 Upsert data 
 Delete data 
 Query data SELECT data 
 Advanced analytic queries 
 Query external data sources with FDW 
 Run queries from Tiger Console 
 Automate with jobs and policies About automation 
 Add a data retention policy 
 Create and manage custom jobs 
 Create a custom retention job 
 Custom job to downsample and compress chunks 
 Custom job for automatic tablespace management 
 Spread data across storage tiers Manage storage and tiering 
 Query tiered data 
 Replicas and forks with tiered data 
 Use hyperfunctions for analytics Hyperfunctions overview 
 Counter aggregation 
 Function pipelines 
 Gapfilling and interpolation Gapfilling and interpolation 
 Time bucket gapfill 
 Last observation carried forward 
 Heartbeat aggregation 
 Hyperloglog 
 Percentile approximation Percentile approximation 
 Approximate percentiles 
 Advanced aggregation methods 
 Statistical aggregation 
 Time-weighted averages 
 Keep pre-computed aggregations up to date Create a continuous aggregate 
 Refresh continuous aggregates 
 Create an index on a continuous aggregate 
 Convert continuous aggregates to the columnstore 
 Drop data from continuous aggregates 
 Migrate a continuous aggregate to the new form 
 Optimize storage and query speed 
 Make queries and schemas faster Performance optimization 
 Accelerate queries using indexes 
 Get faster DISTINCT queries with SkipScan 
 Automatically route queries to continuous aggregates 
 Ensure data integrity with constraints 
 Alter and update table schemas 
 Handle semi-structured data with JSON 
 Enforce constraints with unique indexes 
 Improve query and upsert performance 
 Improve hypertable performance 
 Retrofit chunk intervals 
 Improve storage performance using tablespaces 
 Automate tasks with triggers 
 Troubleshooting Common issues 
 Troubleshoot continuous aggregates 
 Troubleshoot hypertables 
 Troubleshoot hypercore 
 Troubleshoot import and ingest 
 Troubleshoot queries 
 Troubleshoot schema management 
 Troubleshoot time buckets 
 Troubleshoot data retention 
 Troubleshoot data tiering 
 Troubleshoot jobs 
 Troubleshoot hyperfunctions 
 3 Overview Overview 
 Choose a migration approach 
 Migrate to Tiger Cloud Livesync replication Livesync replication 
 Advanced topics 
 Troubleshooting 
 Migrate with downtime 
 FAQ and troubleshooting 
 Dual-write and backfill Dual-write and backfill 
 From TimescaleDB 
 From PostgreSQL 
 From other databases 
 timescaledb-backfill tool 
 Sync and stream Sync from PostgreSQL 
 Sync from S3 
 Stream from Kafka 
 Upload files Upload in Tiger Console 
 Upload in the terminal 
 4 Overview 
 Connect to Tiger Data 
 Type of tool Data engineering & ETL Overview 
 Amazon SageMaker 
 Apache Airflow 
 AWS Lambda 
 Debezium 
 Decodable 
 Supabase 
 Data ingestion & streaming Overview 
 Apache Kafka 
 EMQX 
 Fivetran 
 HighByte 
 HiveMQ 
 Ignition 
 Kepware KEPServerEX 
 Litmus Edge 
 Node-RED 
 BI & visualization Overview 
 Cube 
 Metabase 
 Mode Analytics 
 Power BI 
 Retool 
 Streamlit 
 Tableau 
 Connectors Overview 
 Source Apache Kafka 
 PostgreSQL 
 Amazon S3 
 Destination Tiger Lake (Iceberg) Set up Iceberg connector 
 Query from Snowflake 
 Query with AWS Glue and Athena 
 Code & libraries Overview 
 Connect your app 
 Prisma 
 Query & administration Overview 
 Azure Data Studio 
 DBeaver 
 LibreDB Studio 
 pgAdmin 
 PostgreSQL 
 psql 
 qStudio 
 Secure connectivity Overview 
 Amazon Web Services 
 Corporate data center 
 Google Cloud 
 Microsoft Azure 
 Observability & alerting Overview 
 Amazon CloudWatch 
 Azure Monitor 
 Datadog 
 Grafana 
 Prometheus 
 Telegraf 
 Exported metrics 
 Configuration & deployment Overview 
 CloudNativePG 
 Kubernetes 
 Terraform 
 Industry Oil and gas 
 IoT 
 Energy 
 Crypto 
 Healthcare 
 Manufacturing 
 Platform Tiger Cloud on AWS 
 Tiger Cloud on Azure 
 Self-Hosted 
 First party/third party First party 
 Third party 
 Technology AWS 
 Azure 
 GCP 
 Grafana 
 Kafka 
 Kubernetes 
 PostgreSQL 
 Prometheus 
 Python 
 REST API 
 SQL 
 Terraform 
 Troubleshooting 
 5 Overview 
 Tiger Cloud on AWS Configuration About configuration 
 Configure database parameters 
 Advanced parameters 
 Service management About Tiger Cloud services 
 Tiger Console overview 
 Service explorer 
 Service management 
 Manually change compute resources 
 Connection pooling 
 Fork services 
 High availability Overview 
 Manage high availability 
 Read scaling 
 Back up and recover services 
 Monitor your services 
 Security Overview 
 Passwordless database access 
 Client credentials 
 IP allow list 
 Control user access to projects 
 Multi-factor authentication 
 Manage data security in your service 
 SAML authentication 
 Connect with a stricter SSL mode 
 VPC Peering 
 AWS Transit Gateway 
 Private endpoints 
 Extensions PostgreSQL extensions 
 Optimize full text search with BM25 
 Encrypt data using pgcrypto 
 Create a chatbot using pgvector 
 Analyse geospatial data with PostGIS 
 Maintenance and upgrades 
 Billing and account management 
 Troubleshoot 
 Vectorizer and LLM calls migration guide 
 Tiger Cloud on Azure Configuration About configuration 
 Configure database parameters 
 Advanced parameters 
 Service management About Tiger Cloud services 
 Tiger Console overview 
 Service explorer 
 Service management 
 Manually change compute resources 
 Connection pooling 
 Fork services 
 High availability Overview 
 Manage high availability 
 Read scaling 
 Back up and recover services 
 Monitor your services 
 Security Overview 
 Passwordless database access 
 Client credentials 
 IP allow list 
 Control user access to projects 
 Multi-factor authentication 
 Manage data security in your service 
 SAML authentication 
 Connect with a stricter SSL mode 
 Private endpoints 
 Extensions PostgreSQL extensions 
 Optimize full text search with BM25 
 Encrypt data using pgcrypto 
 Create a chatbot using pgvector 
 Analyse geospatial data with PostGIS 
 Maintenance and upgrades 
 Billing and account management 
 Troubleshoot 
 Vectorizer and LLM calls migration guide 
 Self-hosted TimescaleDB Self-hosted TimescaleDB 
 Configuration Configuration guide 
 About configuration 
 Using timescaledb-tune 
 Manual PostgreSQL configuration 
 TimescaleDB configuration 
 Docker configuration 
 Telemetry 
 Backup and restore Backup and restore 
 Logical backup 
 Physical backups 
 Migrate to self-hosted TimescaleDB Migration guide 
 Migrate entire database 
 Migrate schema then data 
 Migrate tables from the same database 
 Migrate data from InfluxDB 
 Manage storage using tablespaces 
 Replication and high availability Replication and HA 
 About high availability 
 Configure replication 
 Additional tooling Available tools 
 TimescaleDB Tune 
 Install and update TimescaleDB Toolkit 
 Upgrade self-hosted TimescaleDB Upgrade guide 
 Upgrade to a minor version 
 Upgrade to a major version 
 Upgrade TimescaleDB in Docker 
 Upgrade PostgreSQL 
 Downgrade to a minor version 
 Uninstall self-hosted TimescaleDB 
 Troubleshooting 
 Managed Service for TimescaleDB Managed Service for TimescaleDB 
 Create an MST service 
 About MST 
 Ingest data 
 User management 
 Billing 
 Connection pools 
 Viewing service logs 
 VPC peering VPC peering 
 Configure VPC peering 
 VPC peering on AWS 
 VPC peering on GCP 
 VPC peering on Azure 
 AWS Transit Gateway 
 Integrations MST integrations 
 Google Data Studio 
 Grafana 
 Logging 
 Datadog 
 Prometheus 
 Supported extensions 
 Postgres dblink extension 
 Security 
 PostgreSQL read replica 
 Maintenance 
 Failover 
 Backups 
 Aiven client 
 Migrate to MST 
 REST API 
 Index issues 
 Troubleshooting 
 Limitations 
 6 Overview 
 TimescaleDB Overview 
 Hypertables and chunks Overview 
 Table creation CREATE TABLE 
 create_hypertable() 
 CREATE INDEX (Transaction Per Chunk) 
 create_hypertable() (old interface) 
 Chunk management create_chunk() 
 show_chunks() 
 drop_chunk() 
 drop_chunks() 
 move_chunk() 
 reorder_chunk() 
 merge_chunks() 
 merge_chunks_concurrently() 
 split_chunk() 
 chunk_rewrite_cleanup() 
 attach_chunk() 
 detach_chunk() 
 set_chunk_time_interval() 
 set_integer_now_func() 
 add_dimension() 
 add_dimension() (deprecated) 
 Size and statistics hypertable_size() 
 hypertable_detailed_size() 
 hypertable_index_size() 
 hypertable_approximate_size() 
 hypertable_approximate_detailed_size() 
 chunks_detailed_size() 
 Tablespace management attach_tablespace() 
 detach_tablespace() 
 detach_tablespaces() 
 show_tablespaces() 
 Reordering and policies add_reorder_policy() 
 remove_reorder_policy() 
 Query optimization enable_chunk_skipping() 
 disable_chunk_skipping() 
 Hypercore Overview 
 Policies add_columnstore_policy() 
 remove_columnstore_policy() 
 add_compaction_policy() 
 remove_compaction_policy() 
 Manual conversion ALTER TABLE (hypercore) 
 convert_to_columnstore() 
 convert_to_rowstore() 
 Statistics and information chunk_columnstore_stats() 
 hypertable_columnstore_stats() 
 chunk_columnstore_settings 
 hypertable_columnstore_settings 
 Continuous aggregates Overview 
 Create and modify CAGGs CREATE MATERIALIZED VIEW 
 ALTER MATERIALIZED VIEW 
 DROP MATERIALIZED VIEW 
 cagg_migrate() 
 refresh_continuous_aggregate() 
 Manage policies add_continuous_aggregate_policy() 
 remove_continuous_aggregate_policy() 
 Experimental policy management add_policies() 
 alter_policies() 
 remove_policies() 
 remove_all_policies() 
 show_policies() 
 Hyperfunctions Overview 
 Time series utilities days_in_month() 
 first() 
 last() 
 month_normalize() 
 time_bucket() 
 to_epoch() 
 Distribution analysis approximate_row_count() 
 histogram() 
 Gapfilling interpolate() 
 locf() 
 time_bucket_gapfill() 
 Data retention Overview 
 add_retention_policy() 
 remove_retention_policy() 
 Jobs and automation Overview 
 add_job() 
 alter_job() 
 delete_job() 
 run_job() 
 UUIDv7 functions Overview 
 generate_uuidv7() 
 to_uuidv7() 
 to_uuidv7_boundary() 
 uuid_timestamp() 
 uuid_timestamp_micros() 
 uuid_version() 
 Informational views Overview 
 Hypertable and chunk information timescaledb_information.chunks 
 timescaledb_information.dimensions 
 timescaledb_information.hypertables 
 timescaledb_information.continuous_aggregates 
 Columnstore information chunk_columnstore_settings 
 hypertable_columnstore_settings 
 Jobs and policies timescaledb_information.job_errors 
 timescaledb_information.job_history 
 timescaledb_information.job_stats 
 timescaledb_information.jobs 
 timescaledb_experimental.policies 
 Configuration Overview 
 GUC parameters 
 Configuration parameters 
 Administration Overview 
 get_telemetry_report() 
 timescaledb_post_restore() 
 timescaledb_pre_restore() 
 API reference tag overview 
 TimescaleDB Toolkit Overview 
 Approximate count distinct approx_count_distinct() 
 distinct_count() 
 hyperloglog() 
 rollup() 
 stderror() 
 Statistical and regression analysis Overview 
 One variable average() 
 kurtosis() 
 num_vals() 
 rolling() 
 rollup() 
 skewness() 
 stats_agg() (one variable) 
 stddev() 
 sum() 
 variance() 
 Two variables average_y() | average_x() 
 corr() 
 covariance() 
 determination_coeff() 
 intercept() 
 kurtosis_y() | kurtosis_x() 
 num_vals() 
 rolling() 
 rollup() 
 skewness_y() | skewness_x() 
 slope() 
 stats_agg() (two variables) 
 stddev_y() | stddev_x() 
 sum_y() | sum_x() 
 variance_y() | variance_x() 
 x_intercept() 
 Minimum and maximum Overview 
 Minimum values into_array() 
 into_values() 
 min_n() 
 rollup() 
 Maximum values into_array() 
 into_values() 
 max_n() 
 rollup() 
 Minimum values by into_values() 
 min_n_by() 
 rollup() 
 Maximum values by into_values() 
 max_n_by() 
 rollup() 
 Financial analysis candlestick() 
 candlestick_agg() 
 close() 
 close_time() 
 high() 
 high_time() 
 low() 
 low_time() 
 open() 
 open_time() 
 rollup() 
 volume() 
 vwap() 
 Percentile approximation Overview 
 UddSketch approx_percentile() 
 approx_percentile_array() 
 approx_percentile_rank() 
 error() 
 mean() 
 num_vals() 
 percentile_agg() 
 rollup() 
 total() 
 uddsketch() 
 t-digest approx_percentile() 
 approx_percentile_rank() 
 max_val() 
 mean() 
 min_val() 
 num_vals() 
 rollup() 
 tdigest() 
 total() 
 Counters and gauges Overview 
 Counter aggregation corr() 
 counter_agg() 
 counter_zero_time() 
 delta() 
 extrapolated_delta() 
 extrapolated_rate() 
 first_time() 
 first_val() 
 idelta_left() 
 idelta_right() 
 intercept() 
 interpolated_delta() 
 interpolated_rate() 
 irate_left() 
 irate_right() 
 last_time() 
 last_val() 
 num_changes() 
 num_elements() 
 num_resets() 
 rate() 
 rollup() 
 slope() 
 time_delta() 
 with_bounds() 
 Gauge aggregation corr() 
 delta() 
 extrapolated_delta() 
 extrapolated_rate() 
 gauge_agg() 
 gauge_zero_time() 
 idelta_left() 
 idelta_right() 
 intercept() 
 interpolated_delta() 
 interpolated_rate() 
 irate_left() 
 irate_right() 
 num_changes() 
 num_elements() 
 rate() 
 rollup() 
 slope() 
 time_delta() 
 with_bounds() 
 Time-weighted calculations average() 
 first_time() 
 first_val() 
 integral() 
 interpolated_average() 
 interpolated_integral() 
 last_time() 
 last_val() 
 rollup() 
 time_weight() 
 Downsampling asap_smooth() 
 gp_lttb() 
 lttb() 
 Timevector rollup() 
 timevector() 
 unnest() 
 Frequency analysis Overview 
 Frequency aggregation freq_agg() 
 into_values() 
 max_frequency() 
 mcv_agg() 
 min_frequency() 
 rollup() 
 topn() 
 Count-min sketch approx_count() 
 count_min_sketch() 
 State tracking Overview 
 Compact state aggregation compact_state_agg() 
 duration_in() 
 interpolated_duration_in() 
 into_values() 
 rollup() 
 State aggregation duration_in() 
 interpolated_duration_in() 
 interpolated_state_periods() 
 interpolated_state_timeline() 
 into_values() 
 rollup() 
 state_agg() 
 state_at() 
 state_periods() 
 state_timeline() 
 Heartbeat aggregation dead_ranges() 
 downtime() 
 heartbeat_agg() 
 interpolate() 
 interpolated_downtime() 
 interpolated_uptime() 
 live_at() 
 live_ranges() 
 num_gaps() 
 num_live_ranges() 
 rollup() 
 trim_to() 
 uptime() 
 Saturating math saturating_add() 
 saturating_add_pos() 
 saturating_mul() 
 saturating_sub() 
 saturating_sub_pos() 
 Tiger Cloud Overview 
 Tiger CLI 
 Tiger MCP 
 Tiger Cloud REST API Overview 
 Auth 
 Projects Get 
 Vpcs List 
 Create 
 Retrieve 
 Delete 
 Rename 
 Peerings List 
 Create 
 Retrieve 
 Delete 
 Services List 
 Create 
 Retrieve 
 Delete 
 Start 
 Stop 
 Attach To Vpc 
 Detach From Vpc 
 Resize 
 Enable Pooler 
 Disable Pooler 
 Fork Service 
 Update Password 
 Set Environment 
 Logs 
 Set Ha 
 Replica Sets Retrieve Replica Sets 
 Replica Sets 
 Delete 
 Resize 
 Enable Pooler 
 Disable Pooler 
 Set Environment 
 Data tiering Overview 
 add_tiering_policy() 
 remove_tiering_policy() 
 tier_chunk() 
 untier_chunk() 
 disable_tiering() 
 Auto 
 Light 
 Dark 
 Start a free trial 
 Get started 
 Learn 
 Build 
 Migrate 
 Integrate 
 Deploy 
 Reference 
 Start a free trial 
 0 Get started with Tiger Data 
 Choose your setup Compare Tiger Data products 
 Cloud-exclusive features 
 Compare TimescaleDB editions 
 Tiger Console 5-minute quickstart 
 Create a Tiger Cloud account 
 Create a Tiger Cloud service 
 Supported regions 
 Tiger CLI and MCP Get started with Tiger CLI 
 Integrate Tiger Cloud with your AI agent 
 Get started with the REST API 
 Self-hosted TimescaleDB 10-minute quickstart 
 Install self-hosted TimescaleDB 
 Connect your app 
 Supported platforms 
 News and updates Overview 
 Changelog 
 Release notes 
 Contribute to docs 
 1 Overview What is Tiger Data 
 Tiger Data architecture for real-time analytics 
 Tutorials Overview 
 Create Tiger Cloud services with Terraform 
 Simulate an IoT sensor dataset 
 Ingest real-time financial data 
 Analyze application events with UUIDv7 
 Build hybrid search with BM25 and vectors 
 Build a production RAG system with Postgres 
 Aggregate organizational data with AI agents 
 Analyze stock market data 
 Analyze NYC taxi data 
 Analyze Bitcoin blockchain 
 Analyze energy consumption 
 Visualize financial tick data with Grafana 
 Visualize transport and geospatial data with Grafana 
 Tiger Data cookbook 
 Tiger Cloud Tiger Cloud 
 Cloud-exclusive features 
 Tiger Cloud essentials 
 Tiger CLI and MCP 
 Capabilities and comparison Understand capabilities 
 Compare the features in Tiger Data products 
 Data model Design your data model 
 Wide, narrow, and medium tables 
 Primary keys, time columns, and uniqueness 
 Schema optimization 
 Hypertables Understand hypertables 
 Create and configure a hypertable 
 Partition a hypertable 
 Hypertable indexes 
 Hypertable operations 
 Hyperfunctions 
 Chunks and time buckets Understand chunks 
 Size hypertable chunks 
 Understand time buckets 
 Use time buckets 
 Manually drop chunks 
 Hypercore Understand hypercore 
 Compression methods 
 Continuous aggregates (CAGGs) Understand continuous aggregates 
 Time and continuous aggregates 
 Hierarchical continuous aggregates 
 Real-time aggregates 
 Materialized hypertables 
 Data lifecycle Understand the data lifecycle 
 Hypertables and chunks 
 Time buckets 
 Continuous aggregates 
 Hypercore and the columnstore 
 Tiered storage 
 Data retention 
 Search Key vector concepts for pgvector 
 Understand pg_textsearch and BM25 search 
 Understand pgvector and pgvectorscale 
 Glossary 
 2 Overview 
 Build with Tiger CLI and MCP Common tasks 
 Best practices for AI agents 
 Cookbook 
 Quickstarts Overview 
 Your first hypertable 
 Basic compression with hypercore 
 Data lifecycle Your first hypertable 
 Set up hypercore 
 Create a continuous aggregate 
 Manage storage and tiering 
 Create a retention policy 
 Create and manage custom jobs 
 Write and query data Write and query data 
 Write data Insert data 
 Update data 
 Upsert data 
 Delete data 
 Query data SELECT data 
 Advanced analytic queries 
 Query external data sources with FDW 
 Run queries from Tiger Console 
 Automate with jobs and policies About automation 
 Add a data retention policy 
 Create and manage custom jobs 
 Create a custom retention job 
 Custom job to downsample and compress chunks 
 Custom job for automatic tablespace management 
 Spread data across storage tiers Manage storage and tiering 
 Query tiered data 
 Replicas and forks with tiered data 
 Use hyperfunctions for analytics Hyperfunctions overview 
 Counter aggregation 
 Function pipelines 
 Gapfilling and interpolation Gapfilling and interpolation 
 Time bucket gapfill 
 Last observation carried forward 
 Heartbeat aggregation 
 Hyperloglog 
 Percentile approximation Percentile approximation 
 Approximate percentiles 
 Advanced aggregation methods 
 Statistical aggregation 
 Time-weighted averages 
 Keep pre-computed aggregations up to date Create a continuous aggregate 
 Refresh continuous aggregates 
 Create an index on a continuous aggregate 
 Convert continuous aggregates to the columnstore 
 Drop data from continuous aggregates 
 Migrate a continuous aggregate to the new form 
 Optimize storage and query speed 
 Make queries and schemas faster Performance optimization 
 Accelerate queries using indexes 
 Get faster DISTINCT queries with SkipScan 
 Automatically route queries to continuous aggregates 
 Ensure data integrity with constraints 
 Alter and update table schemas 
 Handle semi-structured data with JSON 
 Enforce constraints with unique indexes 
 Improve query and upsert performance 
 Improve hypertable performance 
 Retrofit chunk intervals 
 Improve storage performance using tablespaces 
 Automate tasks with triggers 
 Troubleshooting Common issues 
 Troubleshoot continuous aggregates 
 Troubleshoot hypertables 
 Troubleshoot hypercore 
 Troubleshoot import and ingest 
 Troubleshoot queries 
 Troubleshoot schema management 
 Troubleshoot time buckets 
 Troubleshoot data retention 
 Troubleshoot data tiering 
 Troubleshoot jobs 
 Troubleshoot hyperfunctions 
 3 Overview Overview 
 Choose a migration approach 
 Migrate to Tiger Cloud Livesync replication Livesync replication 
 Advanced topics 
 Troubleshooting 
 Migrate with downtime 
 FAQ and troubleshooting 
 Dual-write and backfill Dual-write and backfill 
 From TimescaleDB 
 From PostgreSQL 
 From other databases 
 timescaledb-backfill tool 
 Sync and stream Sync from PostgreSQL 
 Sync from S3 
 Stream from Kafka 
 Upload files Upload in Tiger Console 
 Upload in the terminal 
 4 Overview 
 Connect to Tiger Data 
 Type of tool Data engineering & ETL Overview 
 Amazon SageMaker 
 Apache Airflow 
 AWS Lambda 
 Debezium 
 Decodable 
 Supabase 
 Data ingestion & streaming Overview 
 Apache Kafka 
 EMQX 
 Fivetran 
 HighByte 
 HiveMQ 
 Ignition 
 Kepware KEPServerEX 
 Litmus Edge 
 Node-RED 
 BI & visualization Overview 
 Cube 
 Metabase 
 Mode Analytics 
 Power BI 
 Retool 
 Streamlit 
 Tableau 
 Connectors Overview 
 Source Apache Kafka 
 PostgreSQL 
 Amazon S3 
 Destination Tiger Lake (Iceberg) Set up Iceberg connector 
 Query from Snowflake 
 Query with AWS Glue and Athena 
 Code & libraries Overview 
 Connect your app 
 Prisma 
 Query & administration Overview 
 Azure Data Studio 
 DBeaver 
 LibreDB Studio 
 pgAdmin 
 PostgreSQL 
 psql 
 qStudio 
 Secure connectivity Overview 
 Amazon Web Services 
 Corporate data center 
 Google Cloud 
 Microsoft Azure 
 Observability & alerting Overview 
 Amazon CloudWatch 
 Azure Monitor 
 Datadog 
 Grafana 
 Prometheus 
 Telegraf 
 Exported metrics 
 Configuration & deployment Overview 
 CloudNativePG 
 Kubernetes 
 Terraform 
 Industry Oil and gas 
 IoT 
 Energy 
 Crypto 
 Healthcare 
 Manufacturing 
 Platform Tiger Cloud on AWS 
 Tiger Cloud on Azure 
 Self-Hosted 
 First party/third party First party 
 Third party 
 Technology AWS 
 Azure 
 GCP 
 Grafana 
 Kafka 
 Kubernetes 
 PostgreSQL 
 Prometheus 
 Python 
 REST API 
 SQL 
 Terraform 
 Troubleshooting 
 5 Overview 
 Tiger Cloud on AWS Configuration About configuration 
 Configure database parameters 
 Advanced parameters 
 Service management About Tiger Cloud services 
 Tiger Console overview 
 Service explorer 
 Service management 
 Manually change compute resources 
 Connection pooling 
 Fork services 
 High availability Overview 
 Manage high availability 
 Read scaling 
 Back up and recover services 
 Monitor your services 
 Security Overview 
 Passwordless database access 
 Client credentials 
 IP allow list 
 Control user access to projects 
 Multi-factor authentication 
 Manage data security in your service 
 SAML authentication 
 Connect with a stricter SSL mode 
 VPC Peering 
 AWS Transit Gateway 
 Private endpoints 
 Extensions PostgreSQL extensions 
 Optimize full text search with BM25 
 Encrypt data using pgcrypto 
 Create a chatbot using pgvector 
 Analyse geospatial data with PostGIS 
 Maintenance and upgrades 
 Billing and account management 
 Troubleshoot 
 Vectorizer and LLM calls migration guide 
 Tiger Cloud on Azure Configuration About configuration 
 Configure database parameters 
 Advanced parameters 
 Service management About Tiger Cloud services 
 Tiger Console overview 
 Service explorer 
 Service management 
 Manually change compute resources 
 Connection pooling 
 Fork services 
 High availability Overview 
 Manage high availability 
 Read scaling 
 Back up and recover services 
 Monitor your services 
 Security Overview 
 Passwordless database access 
 Client credentials 
 IP allow list 
 Control user access to projects 
 Multi-factor authentication 
 Manage data security in your service 
 SAML authentication 
 Connect with a stricter SSL mode 
 Private endpoints 
 Extensions PostgreSQL extensions 
 Optimize full text search with BM25 
 Encrypt data using pgcrypto 
 Create a chatbot using pgvector 
 Analyse geospatial data with PostGIS 
 Maintenance and upgrades 
 Billing and account management 
 Troubleshoot 
 Vectorizer and LLM calls migration guide 
 Self-hosted TimescaleDB Self-hosted TimescaleDB 
 Configuration Configuration guide 
 About configuration 
 Using timescaledb-tune 
 Manual PostgreSQL configuration 
 TimescaleDB configuration 
 Docker configuration 
 Telemetry 
 Backup and restore Backup and restore 
 Logical backup 
 Physical backups 
 Migrate to self-hosted TimescaleDB Migration guide 
 Migrate entire database 
 Migrate schema then data 
 Migrate tables from the same database 
 Migrate data from InfluxDB 
 Manage storage using tablespaces 
 Replication and high availability Replication and HA 
 About high availability 
 Configure replication 
 Additional tooling Available tools 
 TimescaleDB Tune 
 Install and update TimescaleDB Toolkit 
 Upgrade self-hosted TimescaleDB Upgrade guide 
 Upgrade to a minor version 
 Upgrade to a major version 
 Upgrade TimescaleDB in Docker 
 Upgrade PostgreSQL 
 Downgrade to a minor version 
 Uninstall self-hosted TimescaleDB 
 Troubleshooting 
 Managed Service for TimescaleDB Managed Service for TimescaleDB 
 Create an MST service 
 About MST 
 Ingest data 
 User management 
 Billing 
 Connection pools 
 Viewing service logs 
 VPC peering VPC peering 
 Configure VPC peering 
 VPC peering on AWS 
 VPC peering on GCP 
 VPC peering on Azure 
 AWS Transit Gateway 
 Integrations MST integrations 
 Google Data Studio 
 Grafana 
 Logging 
 Datadog 
 Prometheus 
 Supported extensions 
 Postgres dblink extension 
 Security 
 PostgreSQL read replica 
 Maintenance 
 Failover 
 Backups 
 Aiven client 
 Migrate to MST 
 REST API 
 Index issues 
 Troubleshooting 
 Limitations 
 6 Overview 
 TimescaleDB Overview 
 Hypertables and chunks Overview 
 Table creation CREATE TABLE 
 create_hypertable() 
 CREATE INDEX (Transaction Per Chunk) 
 create_hypertable() (old interface) 
 Chunk management create_chunk() 
 show_chunks() 
 drop_chunk() 
 drop_chunks() 
 move_chunk() 
 reorder_chunk() 
 merge_chunks() 
 merge_chunks_concurrently() 
 split_chunk() 
 chunk_rewrite_cleanup() 
 attach_chunk() 
 detach_chunk() 
 set_chunk_time_interval() 
 set_integer_now_func() 
 add_dimension() 
 add_dimension() (deprecated) 
 Size and statistics hypertable_size() 
 hypertable_detailed_size() 
 hypertable_index_size() 
 hypertable_approximate_size() 
 hypertable_approximate_detailed_size() 
 chunks_detailed_size() 
 Tablespace management attach_tablespace() 
 detach_tablespace() 
 detach_tablespaces() 
 show_tablespaces() 
 Reordering and policies add_reorder_policy() 
 remove_reorder_policy() 
 Query optimization enable_chunk_skipping() 
 disable_chunk_skipping() 
 Hypercore Overview 
 Policies add_columnstore_policy() 
 remove_columnstore_policy() 
 add_compaction_policy() 
 remove_compaction_policy() 
 Manual conversion ALTER TABLE (hypercore) 
 convert_to_columnstore() 
 convert_to_rowstore() 
 Statistics and information chunk_columnstore_stats() 
 hypertable_columnstore_stats() 
 chunk_columnstore_settings 
 hypertable_columnstore_settings 
 Continuous aggregates Overview 
 Create and modify CAGGs CREATE MATERIALIZED VIEW 
 ALTER MATERIALIZED VIEW 
 DROP MATERIALIZED VIEW 
 cagg_migrate() 
 refresh_continuous_aggregate() 
 Manage policies add_continuous_aggregate_policy() 
 remove_continuous_aggregate_policy() 
 Experimental policy management add_policies() 
 alter_policies() 
 remove_policies() 
 remove_all_policies() 
 show_policies() 
 Hyperfunctions Overview 
 Time series utilities days_in_month() 
 first() 
 last() 
 month_normalize() 
 time_bucket() 
 to_epoch() 
 Distribution analysis approximate_row_count() 
 histogram() 
 Gapfilling interpolate() 
 locf() 
 time_bucket_gapfill() 
 Data retention Overview 
 add_retention_policy() 
 remove_retention_policy() 
 Jobs and automation Overview 
 add_job() 
 alter_job() 
 delete_job() 
 run_job() 
 UUIDv7 functions Overview 
 generate_uuidv7() 
 to_uuidv7() 
 to_uuidv7_boundary() 
 uuid_timestamp() 
 uuid_timestamp_micros() 
 uuid_version() 
 Informational views Overview 
 Hypertable and chunk information timescaledb_information.chunks 
 timescaledb_information.dimensions 
 timescaledb_information.hypertables 
 timescaledb_information.continuous_aggregates 
 Columnstore information chunk_columnstore_settings 
 hypertable_columnstore_settings 
 Jobs and policies timescaledb_information.job_errors 
 timescaledb_information.job_history 
 timescaledb_information.job_stats 
 timescaledb_information.jobs 
 timescaledb_experimental.policies 
 Configuration Overview 
 GUC parameters 
 Configuration parameters 
 Administration Overview 
 get_telemetry_report() 
 timescaledb_post_restore() 
 timescaledb_pre_restore() 
 API reference tag overview 
 TimescaleDB Toolkit Overview 
 Approximate count distinct approx_count_distinct() 
 distinct_count() 
 hyperloglog() 
 rollup() 
 stderror() 
 Statistical and regression analysis Overview 
 One variable average() 
 kurtosis() 
 num_vals() 
 rolling() 
 rollup() 
 skewness() 
 stats_agg() (one variable) 
 stddev() 
 sum() 
 variance() 
 Two variables average_y() | average_x() 
 corr() 
 covariance() 
 determination_coeff() 
 intercept() 
 kurtosis_y() | kurtosis_x() 
 num_vals() 
 rolling() 
 rollup() 
 skewness_y() | skewness_x() 
 slope() 
 stats_agg() (two variables) 
 stddev_y() | stddev_x() 
 sum_y() | sum_x() 
 variance_y() | variance_x() 
 x_intercept() 
 Minimum and maximum Overview 
 Minimum values into_array() 
 into_values() 
 min_n() 
 rollup() 
 Maximum values into_array() 
 into_values() 
 max_n() 
 rollup() 
 Minimum values by into_values() 
 min_n_by() 
 rollup() 
 Maximum values by into_values() 
 max_n_by() 
 rollup() 
 Financial analysis candlestick() 
 candlestick_agg() 
 close() 
 close_time() 
 high() 
 high_time() 
 low() 
 low_time() 
 open() 
 open_time() 
 rollup() 
 volume() 
 vwap() 
 Percentile approximation Overview 
 UddSketch approx_percentile() 
 approx_percentile_array() 
 approx_percentile_rank() 
 error() 
 mean() 
 num_vals() 
 percentile_agg() 
 rollup() 
 total() 
 uddsketch() 
 t-digest approx_percentile() 
 approx_percentile_rank() 
 max_val() 
 mean() 
 min_val() 
 num_vals() 
 rollup() 
 tdigest() 
 total() 
 Counters and gauges Overview 
 Counter aggregation corr() 
 counter_agg() 
 counter_zero_time() 
 delta() 
 extrapolated_delta() 
 extrapolated_rate() 
 first_time() 
 first_val() 
 idelta_left() 
 idelta_right() 
 intercept() 
 interpolated_delta() 
 interpolated_rate() 
 irate_left() 
 irate_right() 
 last_time() 
 last_val() 
 num_changes() 
 num_elements() 
 num_resets() 
 rate() 
 rollup() 
 slope() 
 time_delta() 
 with_bounds() 
 Gauge aggregation corr() 
 delta() 
 extrapolated_delta() 
 extrapolated_rate() 
 gauge_agg() 
 gauge_zero_time() 
 idelta_left() 
 idelta_right() 
 intercept() 
 interpolated_delta() 
 interpolated_rate() 
 irate_left() 
 irate_right() 
 num_changes() 
 num_elements() 
 rate() 
 rollup() 
 slope() 
 time_delta() 
 with_bounds() 
 Time-weighted calculations average() 
 first_time() 
 first_val() 
 integral() 
 interpolated_average() 
 interpolated_integral() 
 last_time() 
 last_val() 
 rollup() 
 time_weight() 
 Downsampling asap_smooth() 
 gp_lttb() 
 lttb() 
 Timevector rollup() 
 timevector() 
 unnest() 
 Frequency analysis Overview 
 Frequency aggregation freq_agg() 
 into_values() 
 max_frequency() 
 mcv_agg() 
 min_frequency() 
 rollup() 
 topn() 
 Count-min sketch approx_count() 
 count_min_sketch() 
 State tracking Overview 
 Compact state aggregation compact_state_agg() 
 duration_in() 
 interpolated_duration_in() 
 into_values() 
 rollup() 
 State aggregation duration_in() 
 interpolated_duration_in() 
 interpolated_state_periods() 
 interpolated_state_timeline() 
 into_values() 
 rollup() 
 state_agg() 
 state_at() 
 state_periods() 
 state_timeline() 
 Heartbeat aggregation dead_ranges() 
 downtime() 
 heartbeat_agg() 
 interpolate() 
 interpolated_downtime() 
 interpolated_uptime() 
 live_at() 
 live_ranges() 
 num_gaps() 
 num_live_ranges() 
 rollup() 
 trim_to() 
 uptime() 
 Saturating math saturating_add() 
 saturating_add_pos() 
 saturating_mul() 
 saturating_sub() 
 saturating_sub_pos() 
 Tiger Cloud Overview 
 Tiger CLI 
 Tiger MCP 
 Tiger Cloud REST API Overview 
 Auth 
 Projects Get 
 Vpcs List 
 Create 
 Retrieve 
 Delete 
 Rename 
 Peerings List 
 Create 
 Retrieve 
 Delete 
 Services List 
 Create 
 Retrieve 
 Delete 
 Start 
 Stop 
 Attach To Vpc 
 Detach From Vpc 
 Resize 
 Enable Pooler 
 Disable Pooler 
 Fork Service 
 Update Password 
 Set Environment 
 Logs 
 Set Ha 
 Replica Sets Retrieve Replica Sets 
 Replica Sets 
 Delete 
 Resize 
 Enable Pooler 
 Disable Pooler 
 Set Environment 
 Data tiering Overview 
 add_tiering_policy() 
 remove_tiering_policy() 
 tier_chunk() 
 untier_chunk() 
 disable_tiering() 
 Tiger Data Documentation
 Tiger Data are the creators of TimescaleDB, the leading open-source relational database for time-series data. Our tools help you ingest, store, and analyze massive datasets with the full power of SQL.
 Run TimescaleDB on Tiger Cloud
 Step-by-step tutorials and guides for running our fully-managed service.
 Start with Cloud 
 Deploy TimescaleDB locally
 Installation guides, configuration tips, and best practices for self-hosting.
 Start with TimescaleDB 
 Explore
 Explore the docs to find what you need, whether you are learning new concepts, following a tutorial, or looking up a detail. Each area below is a starting point; open a section to go deeper.
 Learn TimescaleDB concepts
 Learn
 Concepts, comparisons, and vocabulary: how TimescaleDB fits together, from hypertables to data lifecycle, plus a glossary.
 Build
 Task-by-task guides: tutorials, examples, data management, continuous aggregates, performance, and cost patterns.
 Deploy
 Run on Tiger Cloud, self-hosted TimescaleDB, or Managed Service for TimescaleDB: install, configure, and operate in your environment.
 Reference
 SQL functions, Toolkit APIs, configuration settings, and the REST API: look up syntax and behavior while you build.
 Core features
 TimescaleDB is a PostgreSQL extension, not a separate database or fork, so you keep the same clients, drivers, and SQL you use with plain PostgreSQL. On top of that, it adds objects and commands for time-partitioned tables, rollups, compression, retention, and other time-series and analytics work.
 Open Build
 Hypertables
 Automatic time-based partitioning for PostgreSQL tables. Scale to billions of rows with no changes to your queries.
 Continuous aggregation
 Incrementally materialized views that stay up to date automatically. Ideal for dashboards and real-time reporting.
 Columnstore
 Transparent columnar compression that reduces storage by up to 95%. Query and modify compressed data with standard SQL.
 AI & vectors
 Store and query vector embeddings alongside your time-series data with pgvector integration for semantic search.
 pg_textsearch
 BM25 full-text search in PostgreSQL. Rank documents by relevance and combine search with relational queries.
 Retention
 Automated retention policies, tiered storage, and data management. Keep what matters, archive the rest.
 What's new
 Follow doc changes in the changelog, check out the current platform status or the TimescaleDB release notes on GitHub.
 View changelog
 Service status
 Current status and incident history for Tiger Data services. Open the status page to subscribe to updates.
 TimescaleDB releases
 Release notes, downloads, and highlights for each TimescaleDB version on GitHub.
Suggest an edit to this page
 --> 
Privacy Preferences
