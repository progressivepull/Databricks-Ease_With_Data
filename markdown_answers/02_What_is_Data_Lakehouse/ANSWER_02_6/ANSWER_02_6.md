# ANSWER 02 6

Which challenge is commonly caused by using many separate tools in traditional data platforms?

A. Reduced storage capacity\
B. Faster data processing\
C. Simplified governance\
**D. Complex integrations and higher maintenance costs**\
E. Automatic AI model training

**Correct Answer: D**

**Understand the Core Concept First**

In a traditional data platform, organizations often use separate tools for:

- ETL (data ingestion)

- Data Warehouses

- Spark processing

- AI/ML platforms

- BI dashboards

- Orchestration

- Governance and security

Example:

Tool 1 → Tool 2 → Tool 3 → Tool 4 → Tool 5

Every tool must:

- Connect to every other tool

- Share data correctly

- Maintain security permissions

- Stay synchronized

This creates complexity and cost.

Databricks solves this by providing a unified platform where these capabilities work together.

------------------------------------------------------------------------

**A. Reduced Storage Capacity ❌**

**Why it's wrong**

Using many tools does not inherently reduce storage capacity.

In fact, traditional architectures often create:

- Multiple copies of data

- Duplicate storage locations

This can actually increase storage usage rather than reduce it.

**Example**

You might have:

Data Lake = 10 TB\
Data Warehouse = 10 TB\
\
Total Storage = 20 TB

The challenge is duplication, not lack of capacity.

**Exam Tip**

Storage capacity is not the primary problem discussed in Databricks architecture.

------------------------------------------------------------------------

**B. Faster Data Processing ❌**

**Why it's wrong**

This is actually a benefit, not a challenge.

The question asks:

"Which challenge is caused by many separate tools?"

Faster processing is a positive outcome.

In reality, many separate systems often slow things down because data must move between platforms.

**Example**

ETL Tool\
↓\
Data Lake\
↓\
Warehouse\
↓\
BI Tool

Every transfer introduces latency.

**Exam Tip**

If an answer sounds like an improvement, it's probably not the challenge being asked about.

------------------------------------------------------------------------

**C. Simplified Governance ❌**

**Why it's wrong**

Many tools make governance more difficult, not simpler.

Each tool may have:

- Different security models

- Different permissions

- Different audit logs

**Example**

A user might have:

Warehouse Access = Yes\
BI Access = No\
ETL Access = Unknown

Managing permissions across systems becomes complicated.

Databricks uses Unity Catalog to centralize governance.

**Exam Tip**

Traditional multi-tool architectures usually create governance complexity, not simplification.

------------------------------------------------------------------------

**D. Complex Integrations and Higher Maintenance Costs ✅**

**Why it's correct**

This is one of the biggest problems Databricks is designed to solve.

When organizations use many tools:

**Integration Problems**

Every system must connect properly.

ETL ↔ Warehouse\
Warehouse ↔ BI\
BI ↔ Security\
ML ↔ Data Lake

More connections = more failure points.

**Maintenance Problems**

Teams must:

- Maintain integrations

- Update connectors

- Troubleshoot failures

- Manage security across platforms

**Consequences**

- Higher costs

- More complexity

- Data inconsistencies

- Security risks

**Databricks Solution**

Databricks unifies:

- Engineering

- Analytics

- AI/ML

- Governance

- Orchestration

into one ecosystem.

**Exam Tip**

When you see:

- "Many tools"

- "Multiple platforms"

- "Traditional architecture"

Think:

Complex integrations + higher maintenance costs

------------------------------------------------------------------------

**E. Automatic AI Model Training ❌**

**Why it's wrong**

Using multiple tools does not automatically train AI models.

AI model training requires:

- Data

- Features

- Algorithms

- Compute resources

Whether you have one tool or ten tools, models are not trained automatically.

**Example**

A company may use:

- Snowflake

- Tableau

- Airflow

and still have no AI models at all.

**Exam Tip**

This option is unrelated to the challenge described in the question.

------------------------------------------------------------------------

**Quick Elimination Strategy**

| **Option** | **Correct?** | **Why** |
|----|----|----|
| A. Reduced storage capacity | ❌ | Not a common issue; duplication is the issue |
| B. Faster data processing | ❌ | Benefit, not a challenge |
| C. Simplified governance | ❌ | Governance becomes more complex |
| D. Complex integrations and higher maintenance costs | ✅ | Main challenge of multi-tool architectures |
| E. Automatic AI model training | ❌ | Unrelated to tool sprawl |

------------------------------------------------------------------------

**Memory Trick**

Think of a traditional data platform as a machine built from many separate parts:

ETL + Warehouse + BI + ML + Security + Orchestration

More parts mean:

🔧 More integrations\
💰 More maintenance\
⚠️ More failures

That's why the correct answer is:

✅ **D. Complex integrations and higher maintenance costs**.

# [README](./../../../README.md)
