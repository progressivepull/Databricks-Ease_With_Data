# ANSWER 17 1

**Question 1**

**What is the primary purpose of Volumes in Unity Catalog?**

**A. To store only Delta transaction logs** ❌ Incorrect

- Delta transaction logs (\_delta_log) are part of Delta tables.

- Volumes are **general-purpose file storage**, not transaction log storage.

**B. To replace Delta tables for structured data** ❌ Incorrect

- Delta tables remain the preferred way to store structured, queryable data.

- Volumes complement tables—they do not replace them.

**C. To provide governed storage for structured, semi-structured, and unstructured files** ✅ Correct

Volumes allow Unity Catalog to govern **files**, not just tables.

Examples of files stored in volumes:

- CSV

- JSON

- XML

- Images

- PDFs

- ZIP files

- Machine Learning models

- Audio

- Video

Think of a Volume as a **secure, governed folder** inside Unity Catalog.

Metastore\
↓\
Catalog\
↓\
Schema\
├── Tables\
├── Views\
└── Volume\
├── Images\
├── PDFs\
├── CSV\
└── ML Models

**D. To create Spark clusters automatically** ❌ Incorrect

- Volumes are storage objects.

- Spark clusters are compute resources.

**E. To manage SQL Warehouse configurations** ❌ Incorrect

- SQL Warehouses are compute resources.

- Volumes have nothing to do with warehouse configuration.

------------------------------------------------------------------------

**Memory Trick**

**Table**

→ Structured data

**Volume**

→ Files

------------------------------------------------------------------------

# [README](./../../../README.md)
