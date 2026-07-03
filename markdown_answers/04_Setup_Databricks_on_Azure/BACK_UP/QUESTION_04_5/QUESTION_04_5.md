# QUESTION 04 5

**Question 5**

**Why are two subnets created when deploying Azure Databricks?**

**A. One for SQL Warehouses and one for Unity Catalog ❌**

- **Why it's wrong:**

  - SQL Warehouses and Unity Catalog do not require dedicated subnets.

**B. One for storage and one for notebooks ❌**

- **Why it's wrong:**

  - Storage and notebooks are not separated by subnet.

**C. One public subnet and one private subnet for network separation and security ✅ Correct**

- **Why it's correct:**

  - Azure Databricks commonly uses:

    - Public subnet

    - Private subnet

  - This improves:

    - Security

    - Network isolation

    - Traffic control

**D. One subnet for developers and one for administrators ❌**

- **Why it's wrong:**

  - Azure networking is not organized by user roles.

**E. Azure requires exactly two subnets for every virtual network ❌**

- **Why it's wrong:**

  - Azure allows many subnet configurations.

  - The two-subnet design is specific to Databricks deployment recommendations, not an Azure requirement.

**Key Concept**

Two subnets improve **security and isolation**, not user organization.

# [README](./../../../README.md)
