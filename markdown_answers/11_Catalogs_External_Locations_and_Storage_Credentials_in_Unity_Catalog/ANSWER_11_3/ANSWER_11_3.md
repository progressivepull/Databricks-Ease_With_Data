# ANSWER 11 3

**Question 3**

**Why might an organization assign different managed locations to different catalogs?**

**A. To increase Spark executor memory** ❌ Incorrect

- Storage locations have nothing to do with cluster memory.

**B. To organize data into separate storage locations for governance and isolation** ✅ Correct

Different business units often require separate storage.

Example:

Finance Catalog\
→ finance-storage\
\
HR Catalog\
→ hr-storage\
\
Engineering Catalog\
→ engineering-storage

Benefits:

- Better governance

- Security isolation

- Easier compliance

- Independent lifecycle management

**C. To eliminate the need for schemas** ❌ Incorrect

- Schemas are still required.

**D. To replace Unity Catalog permissions** ❌ Incorrect

- Storage organization does not replace access control.

**E. To improve notebook collaboration** ❌ Incorrect

- Notebook collaboration is unrelated.

**Key Concept**

Separate Catalog

↓

Separate Storage

↓

Better Governance

# [README](./../../../README.md)
