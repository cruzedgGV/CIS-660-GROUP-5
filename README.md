# CIS-660-GROUP-5
GitHub Repo containing Data Engineering Phase 4: Pipeline Architecture &amp; Governance Group project files

Data Governance & Security PDF is attached to this repo with the name Phase 4- Data Governance & Security.pdf.

Architecture diagram is attached to this repo with the name Phase4_architechture_Diagram.png.

Dataset is sourced from Kaggle's Instacart Market Basket Analysis at https://www.kaggle.com/datasets/psparks/instacart-market-basket-analysis.

Pipeline stages are as follows:
  Bronze Layer (Raw Ingestion): The raw Instacart CSV files are ingested and written exactly as
received into the bronze directory. This preserves the original data state for traceability and
reproducibility.

  Silver Layer (Cleansed & Typed): The pipeline reads from the bronze layer and applies schema
enforcement, data type casting, and structured transformations. The cleaned datasets are stored in
Parquet format in the silver directory for optimized performance and consistency.

  Gold Layer (Curated Business Table): The Silver layer datasets are joined and aggregated to
produce the department_kpi table. This table answers the business question: Which departments
generate the highest number of orders? The curated output is written in Parquet format to the
gold directory.

To run this code, simply have all CSV files in the same directory as the 660_project_Phase4.ipynb file and click run on Google Colab. Outputs folders and Parquet files will be in their bronze, silver, and gold directories under the instacart_pipeline directory as described in the pipeline stages above.
