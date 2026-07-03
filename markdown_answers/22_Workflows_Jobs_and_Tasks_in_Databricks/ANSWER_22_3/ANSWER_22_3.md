# ANSWER 22 3

**Question 3**

**Which of the following is a supported Databricks Workflow task type?**

**A. Kubernetes Deployment** ❌ Incorrect

- Kubernetes deployments are managed outside Databricks.

**B. Azure Logic App** ❌ Incorrect

- Logic Apps are Azure services.

**C. Delta Live Tables (DLT)** ✅ Correct

DLT pipelines can be executed directly as Workflow tasks.

Example:

Workflow\
\
↓\
\
Notebook\
\
↓\
\
DLT Pipeline\
\
↓\
\
SQL Task

Everything becomes part of one workflow.

**D. Azure Function** ❌ Incorrect

- Azure Functions are external services.

**E. Docker Compose** ❌ Incorrect

- Docker Compose isn't a Databricks Workflow task.

------------------------------------------------------------------------

**Memory Trick**

Workflow Task

↓

DLT Supported

------------------------------------------------------------------------

# [README](./../../../README.md)
