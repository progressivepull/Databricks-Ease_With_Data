# ANSWER 49 6

**Question 6**

**Which authentication method is recommended for CI/CD pipelines and automated deployments?**

**A. User-to-Machine (U2M)** ❌ Incorrect

- U2M requires user interaction.

- CI/CD pipelines should run without manual login.

**B. Browser-based authentication only** ❌ Incorrect

- CI/CD systems cannot depend on browser prompts.

**C. Machine-to-Machine (M2M) using a Service Principal** ✅ Correct

Pipeline

↓

Service Principal

↓

CLI

↓

Databricks

No human interaction required.

This is the recommended production approach.

**D. Password-only authentication** ❌ Incorrect

- Password-based automation is insecure and generally discouraged.

**E. Interactive Microsoft Entra ID login** ❌ Incorrect

- Interactive login is unsuitable for automated pipelines.

**Key Concept**

**Automation = M2M**

# [README](./../../../README.md)
