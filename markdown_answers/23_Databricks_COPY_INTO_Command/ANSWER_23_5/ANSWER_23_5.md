# ANSWER 23 5

**Question 5**

**Which capability allows COPY INTO to automatically create columns and detect data types when loading data into a placeholder table?**

**A. Delta Time Travel** ❌ Incorrect

- Time Travel reads previous table versions.

**B. Schema Inference** ✅ Correct

Example CSV:

ID\
\
Name\
\
Salary

COPY INTO automatically determines:

ID → Integer\
\
Name → String\
\
Salary → Decimal

No manual schema is required.

**C. Liquid Clustering** ❌ Incorrect

- Clustering organizes data layout.

**D. Photon Acceleration** ❌ Incorrect

- Photon speeds execution.

**E. Auto Scaling** ❌ Incorrect

- Auto Scaling adjusts worker nodes.

**Memory Trick**

Infer

↓

Schema

# [README](./../../../README.md)
