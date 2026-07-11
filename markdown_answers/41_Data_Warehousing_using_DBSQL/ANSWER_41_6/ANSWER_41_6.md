# ANSWER 41 6

**Question 6**

**How do SQL Warehouses improve support for many simultaneous users?**

**A. By limiting queries to a single cluster** ❌ Incorrect

- That would create bottlenecks.

**B. By disabling autoscaling during peak workloads** ❌ Incorrect

- Autoscaling improves concurrency.

**C. By using multiple clusters and Intelligent Workload Management to distribute concurrent queries** ✅ Correct

- Serverless SQL Warehouses:

  - Scale horizontally

  - Use multiple clusters

  - Balance workloads

  - Prevent one query from blocking others

This improves:

- Concurrency

- Performance

- Responsiveness

**D. By caching every table permanently in memory** ❌ Incorrect

- Not all data is permanently cached.

**E. By preventing users from running long-running queries** ❌ Incorrect

- Long-running queries are allowed.

**Key Concept**

**Concurrency = Multiple clusters + Intelligent Workload Management**

# [README](./../../../README.md)
