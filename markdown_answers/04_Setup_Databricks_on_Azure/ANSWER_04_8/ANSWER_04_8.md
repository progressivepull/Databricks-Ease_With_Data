# ANSWER 04 8

**Question 8**

**During networking configuration for Azure Databricks, which setting is recommended?**

**A. Enable public IP addresses for all clusters ❌**

- **Why it's wrong:**

  - Public IPs increase the attack surface and are generally discouraged for secure enterprise deployments.

**B. Disable public IP addresses and use the custom Virtual Network ✅ Correct**

- **Why it's correct:**

  - Using a customer-managed Virtual Network with no public IPs improves:

    - Security

    - Compliance

    - Network control

**C. Use Azure's default Virtual Network without customization ❌**

- **Why it's wrong:**

  - While possible for simple setups, enterprise deployments typically use custom VNets to meet security and networking requirements.

**D. Skip Virtual Network configuration completely ❌**

- **Why it's wrong:**

  - Networking is a required part of deploying Azure Databricks.

**E. Enable anonymous public network access ❌**

- **Why it's wrong:**

  - Anonymous public access is a major security risk and is not recommended.

**Key Concept**

Best practice is to **use a custom Virtual Network and disable public IP addresses** for clusters whenever possible.

# [README](./../../../README.md)
