# ANSWER 05 6

**Question 6**

**What is a Service Principal in Databricks primarily used for?**

**A. Managing cluster hardware** ❌ Incorrect

- Databricks manages infrastructure automatically.

- Service Principals do not manage hardware.

**B. Storing Delta tables** ❌ Incorrect

- Delta tables are stored in cloud storage.

- Service Principals are identities, not storage.

**C. Acting as a non-human identity for automation and production workloads** ✅ **Correct**

- Service Principals represent applications instead of people.

- Common uses include:

  - CI/CD pipelines

  - Automated jobs

  - APIs

  - Scheduled workflows

  - Infrastructure automation

**D. Creating Virtual Networks** ❌ Incorrect

- Virtual Networks are created in Azure, AWS, or GCP.

- Service Principals may authenticate automation that creates them, but they do not create networks themselves.

**E. Managing notebook version history** ❌ Incorrect

- Notebook versioning is handled by Git integration or workspace features.

**Key Concept**

A Service Principal is simply an **application identity**.

------------------------------------------------------------------------

# [README](./../../../README.md)
