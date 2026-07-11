# ANSWER 40 4

**Question 4**

**Why do Serverless notebooks and jobs typically start within seconds?**

**A. Users preconfigure all clusters before execution.** ❌ Incorrect

- That defeats the purpose of Serverless.

**B. Databricks maintains a fleet of pre-provisioned virtual machines ready to run workloads.** ✅ Correct

- Databricks keeps compute resources warm.

- Instead of creating new VMs every time, it assigns available ones.

- This greatly reduces startup time.

**C. Serverless disables Spark initialization.** ❌ Incorrect

- Spark still initializes.

- The startup is simply optimized.

**D. The data is cached permanently in memory.** ❌ Incorrect

- Data isn't permanently cached.

- Startup speed comes from pre-provisioned compute.

**E. All jobs execute on a single shared cluster.** ❌ Incorrect

- Jobs are not forced onto one cluster.

**Key Concept**

Warm compute pools = fast startup.

# [README](./../../../README.md)
