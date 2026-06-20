# ANSWER 01 1

**What is a key advantage of a Data Lakehouse compared to traditional data warehouses?**

A. It only stores structured data in predefined schemas\
B. It eliminates the need for any data governance\
**C. It combines the scalability of data lakes with the reliability of data warehouses**\
D. It requires all data to be processed before storage\
E. It cannot support machine learning workloads

**Correct Answer:** C. It combines the scalability of data lakes with the reliability of data warehouses

------------------------------------------------------------------------

**✅ Correct Answer: C**

**“It combines the scalability of data lakes with the reliability of data warehouses”**

This is exactly what a **Data Lakehouse** is designed to do:

- From **data lakes** → it gets scalability, low-cost storage, and ability to handle raw/unstructured data

- From **data warehouses** → it gets structure, governance, ACID transactions, and reliable querying

👉 In short: **best of both worlds**

------------------------------------------------------------------------

**❌ A. It only stores structured data in predefined schemas**

**Why wrong:**

- This describes a **traditional data warehouse**, not a lakehouse

- Lakehouses support:

  - Structured data ✅

  - Semi-structured data ✅

  - Unstructured data ✅

👉 Lakehouses are flexible, not restricted

------------------------------------------------------------------------

**❌ B. It eliminates the need for any data governance**

**Why wrong:**

- Governance is still **very important**

- In fact, lakehouses often **improve governance** (e.g., Unity Catalog)

- Features include:

  - Access control

  - Auditing

  - Data lineage

👉 No modern data system eliminates governance

------------------------------------------------------------------------

**❌ D. It requires all data to be processed before storage**

**Why wrong:**

- This is more like **ETL in traditional warehouses**

- Lakehouses support **schema-on-read**:

  - You can store raw data first

  - Process it later when needed

👉 Flexibility is a key advantage

------------------------------------------------------------------------

**❌ E. It cannot support machine learning workloads**

**Why wrong:**

- Completely false

- Lakehouses are **great for machine learning**

  - They store large volumes of raw data

  - Integrate with ML tools (e.g., Databricks ML)

👉 ML support is actually a major strength

------------------------------------------------------------------------

**🔑 Simple Summary**

- **Data Warehouse:** structured, reliable, but less flexible

- **Data Lake:** flexible, scalable, but less structured

- **Data Lakehouse:** **combines both advantages → (Correct Answer C)**

# [README](./../../../README.md)
