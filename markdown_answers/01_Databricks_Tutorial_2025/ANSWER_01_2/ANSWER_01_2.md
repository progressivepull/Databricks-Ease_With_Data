# ANSWER 01 2

**What is a key characteristic of a data lake?**

A. It stores only structured data in predefined schemas\
B. It requires data to be cleaned and transformed before storage\
**C. It stores raw data in its native format until needed**\
D. It is optimized exclusively for transactional processing\
E. It only supports relational database formats

**Correct Answer:** C

------------------------------------------------------------------------

Let’s break down each option so you clearly understand **why it’s right or wrong**.

**✅ Correct Answer: C**

**“It stores raw data in its native format until needed”**

This is the defining feature of a **data lake**:

- Data is stored **as-is (raw)**

- No need to structure or clean it upfront

- Supports **schema-on-read** (you define structure when you use the data)

👉 This gives flexibility and scalability

------------------------------------------------------------------------

**❌ A. It stores only structured data in predefined schemas**

**Why wrong:**

- This describes a **data warehouse**, not a data lake

- Data lakes support:

  - Structured ✅

  - Semi-structured ✅

  - Unstructured ✅

👉 Data lakes are not limited to predefined schemas

------------------------------------------------------------------------

**❌ B. It requires data to be cleaned and transformed before storage**

**Why wrong:**

- This is **ETL (Extract, Transform, Load)** → typical of data warehouses

- Data lakes use **ELT or schema-on-read**:

  - Store first

  - Clean/process later

👉 No upfront transformation required

------------------------------------------------------------------------

**❌ D. It is optimized exclusively for transactional processing**

**Why wrong:**

- Transactional processing (OLTP) is handled by **operational databases**, not data lakes

- Data lakes are designed for:

  - Analytics

  - Big data processing

  - Machine learning

👉 Not built for transactions

------------------------------------------------------------------------

**❌ E. It only supports relational database formats**

**Why wrong:**

- Data lakes are **not limited to relational formats**

- They support:

  - JSON, CSV, Parquet

  - Images, videos

  - Logs, streaming data

👉 Much more flexible than relational systems

------------------------------------------------------------------------

**🔑 Simple Summary**

- **Data Lake = Raw + Flexible + Scalable**

- Stores data first → processes later

- That’s why **C is correct**

# [README](./../../../README.md)
