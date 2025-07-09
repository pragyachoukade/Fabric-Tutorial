# Microsoft Fabric Learning Journey 🚀

Welcome to my hands-on learning repository documenting Microsoft Fabric. This project highlights my end-to-end workflows: data ingestion, transformation, semantic modeling, governance, and deployments.

---

## 🧭 What’s Inside

| Area             | Description                                                                                  |
|------------------|----------------------------------------------------------------------------------------------|
| **Workspace Setup** | Workspace (`PragyaWS`), `pragyaLakehouse`, pipelines, dataflows, notebook development |
| **Data Ingestion**  | Pipelines copying data from GitHub & Azure Data Lake into lakehouse, conditional logic    |
| **Transforms**       | Dataflows and PySpark notebooks transforming raw data into silver and gold layers        |
| **Semantic Modeling**| Created managed tables and gold schema in warehouse for cross-object querying            |
| **ML & Wrangler**    | Explored AutoML, Data Wrangler workflows, lineage, and governance best practices         |
| **Deployment**       | Built deployment pipelines for Power BI content promotion across environments            |

---
## 🧠 Project Highlights

These milestones showcase my hands‑on experience and technical skills using Microsoft Fabric:

1. **Workspace & Lakehouse Setup**  
   Initiated `PragyaWS` workspace and established `pragyaLakehouse` for organizing all pipeline and transformation artifacts.  

![image](https://github.com/user-attachments/assets/3a3386e3-5e15-4392-b210-490d45e3a3b4)

2. **Ingestion Pipeline: GitHub to Lakehouse**  
   Built the `tutorial1` pipeline using **Lookup → ForEach → Copy**, fetching data from GitHub and loading into the lakehouse. Data lineage, connectors, and mapping logic captured.  

   ![image](https://github.com/user-attachments/assets/df6b8e8c-7339-43a1-88f2-6bafd81510f9)


3. **Ingestion Pipeline: Azure Data Lake → Lakehouse**  
   Created a secondary pipeline to ingest from Azure Data Lake Storage (ADLS) to lakehouse to ensure data continuity and error tolerance.  

   ![image](https://github.com/user-attachments/assets/625c7497-5648-4d3e-87fe-14badf826cfb)


4. **Transformation via Dataflow**  
   Constructed a **Dataflow Gen2** transformation targeting the silver layer within the lakehouse using joins, cleanses, and logic chaining.  

   ![image](https://github.com/user-attachments/assets/d356fa3e-be5a-4914-8906-b453d64924ef)


5. **Parent Pipeline Orchestration**  
   Used an **Invoke Pipeline** approach to orchestrate upstream ingestion pipelines into a consolidated ingestion workflow, bridging raw to silver transitions.  

   ![image](https://github.com/user-attachments/assets/ebbce951-b133-42c9-b094-c1ade06555b0)


6. **PySpark Notebook: Silver → Gold Transformation**  
   Executed a PySpark notebook in the same workspace to process silver-layer data and save transformed DataFrames as managed tables for warehouse ingestion.  
    **Transformations**
   I processed raw data into the gold schema using PySpark.  
   View the transformation logic in the notebook:

   [silver-to-gold transformation notebook](./Transformed_Data/Silver_Notebook.ipynb)

7. **Gold Schema & Managed Tables in Warehouse**  
   Created a warehouse with a `gold` schema by converting silver data into managed tables—enabling cross-object querying and BI-ready datasets.  
   *Insert warehouse schema screenshot*

8. **Explored AutoML & Data Wrangling**  
   Applied AutoML for model training and used Data Wrangler to perform feature engineering; documented lineage, governance, and metadata handling.  
   *Insert governance/catalog screenshot*

9. **Deployment Pipelines (Power BI)**  
   Configured Power BI deployment pipelines to promote artifacts across Dev → Test → Prod, applying deployment rules to bind models and reports per environment.  
   *Insert deployment pipeline screenshot*

---


