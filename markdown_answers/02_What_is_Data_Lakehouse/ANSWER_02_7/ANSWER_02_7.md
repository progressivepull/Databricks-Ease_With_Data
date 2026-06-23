# ANSWER 02 7

How does Databricks help organizations avoid vendor lock-in?

A. By storing data only in proprietary formats\
B. By requiring all data to be stored in Databricks-managed storage\
**C. By using open formats such as Parquet, CSV, Avro, and ORC**\
D. By preventing data migration to other platforms\
E. By eliminating cloud storage providers

**Correct Answer: C**

**Understand the Core Concept First**

**What is Vendor Lock-In?**

Vendor lock-in occurs when:

- Your data is stored in a vendor's proprietary format.

- Only that vendor's tools can read the data.

- Moving to another platform becomes difficult or expensive.

Example:

Vendor Storage\
↓\
Vendor Format\
↓\
Vendor Query Engine

If you leave the vendor, you may need to:

- Convert data

- Rewrite applications

- Migrate large datasets

This creates dependency on a single vendor.

------------------------------------------------------------------------

**How Databricks Avoids Vendor Lock-In**

Databricks stores data in **open formats** such as:

- Parquet

- CSV

- Avro

- ORC

The data remains in your cloud storage:

- AWS S3

- Azure Data Lake Storage (ADLS)

- Google Cloud Storage (GCS)

Databricks uses **Delta Lake** on top of these files, but the underlying data remains yours.

Think:

Your Cloud Storage\
+\
Open Formats\
+\
Delta Lake Features

You own the data and can access it with other tools if needed.

------------------------------------------------------------------------

**A. By storing data only in proprietary formats ❌**

**Why it's wrong**

This would actually create vendor lock-in.

A proprietary format means:

Only Vendor Can Read Data

Examples of problems:

- Difficult migrations

- Dependency on one vendor

- Higher switching costs

Databricks promotes the opposite approach.

**Exam Tip**

When you see:

"proprietary format"

Think:

❌ Vendor lock-in

------------------------------------------------------------------------

**B. By requiring all data to be stored in Databricks-managed storage ❌**

**Why it's wrong**

Databricks does not require customers to store data in Databricks-owned storage.

Instead, data remains in:

- AWS

- Azure

- GCP

Customer-controlled storage.

Example:

Your AWS S3 Bucket\
↓\
Databricks Reads It

Databricks provides compute and management capabilities but does not take ownership of your storage.

**Exam Tip**

Databricks emphasizes:

Bring your own cloud storage.

Not:

Move everything into Databricks storage.

**C. By using open formats such as Parquet, CSV, Avro, and ORC ✅**

**Why it's correct**

This is the main strategy Databricks uses to avoid vendor lock-in.

Open formats provide:

**Portability**

Multiple tools can read them.

Example:

Parquet File\
↓\
Databricks\
Spark\
Snowflake\
Trino\
Presto

**Ownership**

You control the files.

**Flexibility**

You can move platforms without losing access to your data.

**Databricks Philosophy**

Open Storage\
+\
Open Formats\
=\
No Vendor Lock-In

**Exam Tip**

Keywords that usually indicate the correct answer:

- Open formats

- Parquet

- Avro

- ORC

- Customer-owned storage

------------------------------------------------------------------------

**D. By preventing data migration to other platforms ❌**

**Why it's wrong**

Preventing migration is the definition of vendor lock-in.

Databricks does the opposite.

Because data is stored in open formats:

- You can migrate it.

- You can use other analytics engines.

- You are not trapped.

**Example**

A company can:

Today → Databricks\
Future → Another Platform

and still keep access to the same data files.

**Exam Tip**

If an answer suggests making migration harder, it is usually the opposite of Databricks' philosophy.

------------------------------------------------------------------------

**E. By eliminating cloud storage providers ❌**

**Why it's wrong**

Databricks depends on cloud storage providers.

The Lakehouse architecture is built on:

- AWS S3

- Azure ADLS

- Google Cloud Storage

These are foundational components.

Databricks does not eliminate them.

Instead, it integrates with them.

**Architecture Reminder**

Cloud Storage\
↓\
Delta Lake\
↓\
Unity Catalog\
↓\
Analytics / AI

Cloud storage is the bottom layer of the Lakehouse.

**Exam Tip**

If an answer says Databricks removes cloud storage providers, it's incorrect.

------------------------------------------------------------------------

**Quick Elimination Strategy**

| **Option** | **Correct?** | **Why** |
|----|----|----|
| A. Proprietary formats | ❌ | Causes vendor lock-in |
| B. Databricks-managed storage only | ❌ | Data stays in customer cloud storage |
| C. Open formats (Parquet, CSV, Avro, ORC) | ✅ | Core strategy to avoid lock-in |
| D. Prevent migration | ❌ | Opposite of Databricks philosophy |
| E. Eliminate cloud providers | ❌ | Databricks depends on cloud storage |

------------------------------------------------------------------------

**Memory Trick**

Think of Databricks' philosophy as:

Your Data\
+\
Your Cloud Storage\
+\
Open Formats\
=\
Your Choice

Not:

Vendor Owns Data\
+\
Proprietary Format\
=\
Vendor Lock-In

Whenever you see a question about **avoiding vendor lock-in**, look for:

✅ **Open formats (Parquet, CSV, Avro, ORC)**\
✅ **Customer-owned cloud storage**

Those are the strongest clues that the answer is **C**.

# [README](./../../../README.md)
