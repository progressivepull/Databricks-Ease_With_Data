# EXPLANATION 04 5

**Question 5**

**Why are two subnets created when deploying Azure Databricks?**

**Correct Answer:**\
✅ **One public subnet and one private subnet for network separation and security**

**Explanation**

When deploying Azure Databricks with a customer-managed Virtual Network (VNet injection), Microsoft requires **two dedicated subnets**:

- **Host (public) subnet**

- **Container (private) subnet**

This design provides:

- Network isolation

- Better security

- Private connectivity

- Firewall integration

- Traffic inspection

- Better control over network routing

Microsoft documents these subnet requirements for VNet injection deployments.

**YouTube**

**Azure Databricks – Public & Private Subnets**

<https://www.youtube.com/playlist?list=PLNj2XeCNjFeosTuxZLjfYvnW4H1hsPH07>

**Azure Databricks Networking (Official)**

<https://www.youtube.com/playlist?list=PLeK0Tsm_E67TIi_3N-FjOgrpFxbXBlqnq>

------------------------------------------------------------------------

# [README](./../../../README.md)
