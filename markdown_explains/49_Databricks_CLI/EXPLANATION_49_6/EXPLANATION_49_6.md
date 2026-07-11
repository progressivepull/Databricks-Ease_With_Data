# EXPLANATION 49 6

**Question 6**

**Which authentication method is recommended for CI/CD pipelines and automated deployments?**

**Correct Answer:**\
**C. Machine-to-Machine (M2M) using a Service Principal**

**Why C is Correct**

CI/CD pipelines should not rely on an individual user's credentials.

Instead, use:

- Service Principal

- OAuth Machine-to-Machine (M2M)

Benefits:

- Non-interactive

- Secure

- Rotatable credentials

- Suitable for automated deployments

This is the recommended authentication method for production automation. ([docs.databricks.com](https://docs.databricks.com/aws/en/dev-tools/auth/oauth-m2m))

**Why the other choices are wrong**

User accounts can expire, be disabled, or require interactive sign-in, making them unsuitable for unattended pipelines.

**Memory Tip**

**Pipeline = M2M**

**Individual YouTube Video**

https://www.youtube.com/watch?v=5s8N4vV5m9M

**YouTube Search**

https://www.youtube.com/results?search_query=Databricks+OAuth+M2M+Service+Principal

# [README](./../../../README.md)
