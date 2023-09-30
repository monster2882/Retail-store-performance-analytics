# Retail-store-performance-analytics
Project used greenplum, clickhouse, airflow, superset

Project Name: Data Integration and Showcase Building
Overview
This project aims to automate the process of data integration and showcase construction using various tools and technologies, including Greenplum, Clickhouse, Apache Superset, and Apache Airflow. It involves the extraction, transformation, and loading (ETL) of data from multiple sources into data showcases for analytical purposes.

Technical Components
1. Data Sources
Stores (stores)

Description: Text table for stores.
Data Loading Method: Loaded from a file via gpfdist from the local machine.
Traffic (traffic)

Description: Information about customers entering the store, sent to the data store once per hour from metering systems.
Data Loading Method: Loaded from an external PostgreSQL database via PXF.
Checks (bills_head, bills_item)

Description: Check data stored in two separate tables gp.bills_head and gp.bills_item.
Data Loading Method: Loaded from an external PostgreSQL database via PXF.
Connection Parameters: [Provide connection parameters here]
Coupons (coupons)

Description: Discount Coupons data.
Data Loading Method: Loaded from a file via gpfdist from the local machine.
Stock Promotions (stock_promos)

Description: List of promotions in the company that are current at the time the report was generated.
Promotions (promos)

Description: List of the current promotions in the company at the time the report is generated.
Promotion Types (promo_types)

Description: List of the current promo types in the company at the time of reporting.
2. Data Processing and Workflow
The ETL process is fully automated using Apache Airflow, ensuring seamless data extraction, transformation, and loading.
3. Data Storage
Data showcases are loaded into Clickhouse for efficient querying and analysis.
4. Reporting
Reports are generated using Apache Superset, providing insights and visualizations based on the integrated data.