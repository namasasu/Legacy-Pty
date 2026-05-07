# Legacy-Pty

Project Summary
Sales Analytics Data Pipeline - Databricks Lakeflow (LEGACY_INC)
This is a enterprise-grade sales analytics platform using Databricks Lakeflow Spark Declarative Pipelines with complete medallion architecture (Bronze/Silver/Gold layers). The pipeline processes 116K+ raw records into a dimensional star schema and business-ready analytics tables.

Technical Architecture:
•	Bronze Layer: Implemented Auto Loader for incremental CSV ingestion from Unity Catalog volumes with comprehensive error handling (PERMISSIVE mode, rescued data columns, malformed record capture) and metadata tracking
•	Silver Layer: Built normalized star schema with 4 tables - 3 dimension tables (product categories: 37 rows, products, customers: 18.5K rows) and 1 fact table (sales transactions: 60.4K rows). Implemented multi-level data quality constraints (FAIL UPDATE for critical PKs, DROP ROW for invalid data, WARN for monitoring)
•	Gold Layer: Created 4 business-ready analytics tables including product sales summaries, customer lifetime value metrics, category performance analysis, and monthly sales trends with calculated KPIs (order count, average order value, customer tenure, churn status)

Key Technical Features:
•	Serverless compute with Photon engine optimization for cost efficiency
•	Comprehensive data quality framework with 50+ validation constraints across all layers
•	Cluster key optimization for query performance
•	Referential integrity validation between dimensions and facts
•	Business logic validation (age calculations, date logic, status flags)
•	Production-ready error handling and data observability

Technologies: Databricks, Spark Declarative Pipelines (SDP), SQL, Unity Catalog, Auto Loader, Photon Engine, Serverless Compute, Star Schema Modeling

Business Impact: Enabled analytics on customer behavior, product performance, and sales trends with validated, high-quality data supporting downstream BI and reporting


Full ETL process using medallion architecture.
Full Report Dashboard: https://dbc-ca9bcb57-4aa3.cloud.databricks.com/dashboardsv3/01f148705b52120196890d570bdf7a23/published?o=7474656912461022
