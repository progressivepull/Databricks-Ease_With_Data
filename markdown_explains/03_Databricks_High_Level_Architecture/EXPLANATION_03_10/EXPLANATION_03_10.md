# EXPLANATION 03 10

**Service Principal**

A **Service Principal** is a **non-human identity** used by applications, scripts, automation tools, or services to securely access cloud resources without using a person's username and password.

Think of it as a **service account** that represents an application instead of a user.

**Why use a Service Principal?**

Instead of a developer logging in with their own account, an application authenticates using a Service Principal.

For example:

User Login\
\
John\
↓\
Azure AD\
↓\
Storage Account

With automation:

Application\
↓\
Service Principal\
↓\
Azure AD\
↓\
Azure Storage

This allows automated jobs to run even when no one is logged in.

**Components of a Service Principal**

A Service Principal typically has three pieces of information:

- **Client ID (Application ID):** A unique identifier for the application.

- **Tenant ID:** Identifies the organization (directory) where the application is registered.

- **Client Secret** (or a certificate): The application's credential, similar to a password.

Example:

Tenant ID:\
72f988bf-xxxx-xxxx-xxxx-xxxxxxxxxxxx\
\
Client ID:\
3c8d5a11-xxxx-xxxx-xxxx-xxxxxxxxxxxx\
\
Client Secret:\
\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*\*

**How it Works**

1.  An application requests an access token from the identity provider (such as Microsoft Entra ID).

2.  It presents its Client ID and Client Secret (or certificate).

3.  The identity provider verifies the credentials.

4.  If successful, it issues an access token.

5.  The application uses the token to access cloud resources.

Application\
│\
│ Client ID + Secret\
▼\
Microsoft Entra ID\
│\
│ Access Token\
▼\
Azure Storage\
Azure SQL\
Azure Key Vault\
Databricks

**Example in Databricks**

A Service Principal is commonly used to let Databricks access cloud storage securely.

Example workflow:

Databricks Job\
│\
▼\
Service Principal\
│\
▼\
Microsoft Entra ID\
│\
▼\
Azure Data Lake Storage (ADLS Gen2)

The Service Principal authenticates to Microsoft Entra ID, receives a token, and Databricks uses that token to read or write data in ADLS Gen2.

**Common Use Cases**

- Automated ETL pipelines

- Scheduled jobs

- CI/CD deployments

- Infrastructure as Code (Terraform, Bicep)

- Applications accessing databases or storage

- Databricks accessing cloud storage

- Azure Functions, Logic Apps, and other cloud services

**Benefits**

- **Improved security:** No personal user credentials are embedded in code.

- **Least privilege:** Grant only the permissions the application needs.

- **Automation:** Works without user interaction.

- **Auditability:** Actions are logged under the Service Principal rather than an individual user.

- **Credential management:** Secrets or certificates can be rotated without affecting users.

**Service Principal vs. User Account**

| **Feature** | **User Account** | **Service Principal** |
|----|----|----|
| Represents | A person | An application or service |
| Login method | Username and password, MFA | Client ID + Secret or certificate |
| Interactive sign-in | Yes | No |
| Used for automation | No | Yes |
| Can have permissions | Yes | Yes |
| Subject to MFA | Often | No (uses application credentials) |

**Real-World Example**

Suppose your company runs a nightly job that copies sales data from Azure Storage into Databricks:

1.  A scheduled job starts at 2:00 AM.

2.  The job authenticates using a Service Principal.

3.  Microsoft Entra ID issues an access token.

4.  The job reads files from Azure Data Lake Storage.

5.  The data is processed and stored in Delta tables.

Because the job uses a Service Principal instead of a person's account, it continues to run reliably even if an employee leaves the company or changes their password.

------------------------------------------------------------------------

Here are some excellent YouTube videos on **Service Principals** in Azure and Databricks.

**1. Mount using Service Principal in Azure Databricks**

▶️ [Mount using Service Principal in Databricks (YouTube)](https://www.youtube.com/watch?v=CfAKO_w3ia4&utm_source=chatgpt.com)

**What you'll learn:**

- What a Service Principal is

- Creating a Service Principal

- Finding the Client ID, Tenant ID, and Client Secret

- Accessing Azure Data Lake Storage from Databricks

- Using Azure Key Vault with Databricks

------------------------------------------------------------------------

**2. Access Azure Data Lake Storage Using a Service Principal in Databricks**

▶️ [Accessing Azure Data Lake Storage Using Service Principal (YouTube)](https://www.youtube.com/watch?v=fQUp2BN3l3Y&utm_source=chatgpt.com)

**What you'll learn:**

- Registering a Service Principal in Microsoft Entra ID

- Assigning permissions

- Configuring Spark settings

- Securely accessing Azure Data Lake Storage (ADLS Gen2) from Databricks

------------------------------------------------------------------------

**Official Documentation**

- [Microsoft Learn – Service Principals in Azure Databricks](https://learn.microsoft.com/en-us/azure/databricks/admin/users-groups/service-principals?utm_source=chatgpt.com)

- [Microsoft Learn – Manage Service Principals](https://learn.microsoft.com/en-us/azure/databricks/admin/users-groups/manage-service-principals?utm_source=chatgpt.com)

- [Microsoft Learn – Authenticate with Microsoft Entra Service Principals](https://learn.microsoft.com/en-us/azure/databricks/dev-tools/auth/azure-sp?utm_source=chatgpt.com)

These resources explain how Service Principals are used for automation, CI/CD pipelines, scheduled jobs, and secure access to Azure and Databricks resources.

# [README](./../../../README.md)
