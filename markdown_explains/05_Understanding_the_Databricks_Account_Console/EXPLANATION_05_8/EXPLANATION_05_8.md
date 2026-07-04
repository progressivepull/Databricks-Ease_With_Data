# EXPLANATION 05 8

**Question 8**

**What is the purpose of Network Connectivity Configurations (NCC)?**

**Correct Answer:**\
✅ **To securely connect Azure resources that cannot communicate directly with Databricks**

**Explanation**

**Network Connectivity Configuration (NCC)** is an account-level networking feature used primarily with **serverless compute**.

It enables secure communication between Databricks serverless resources and your Azure resources by managing:

- Private Endpoints

- Stable service endpoints/IP ranges

- Secure connectivity to storage and databases

An NCC can be attached to one or more workspaces in the same region.

**Example**

Serverless Compute\
\
↓\
\
NCC\
\
↓\
\
Private Endpoint\
\
↓\
\
Azure Storage

**YouTube**

**Azure Databricks Serverless Networking**

https://www.youtube.com/results?search_query=Azure+Databricks+Network+Connectivity+Configuration+NCC

------------------------------------------------------------------------

# [README](./../../../README.md)
