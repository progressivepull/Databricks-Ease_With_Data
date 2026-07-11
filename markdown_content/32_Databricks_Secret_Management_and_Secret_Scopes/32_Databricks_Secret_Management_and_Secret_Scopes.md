# 32 Databricks Secret Management and Secret Scopes

**Databricks Secret Management & Secret Scopes**

This lesson introduces **Databricks Secret Management**, which provides a secure way to store and retrieve sensitive information such as passwords, API keys, JDBC URLs, hostnames, and connection strings. Instead of embedding credentials directly in notebooks or jobs, Databricks stores them in **Secret Scopes** and retrieves them securely using dbutils.secrets. The lesson covers two types of Secret Scopes: **Azure Key Vault-backed** and **Databricks-backed**.

**1. Why Use Secret Scopes?**

Sensitive information should **never** be hardcoded into notebooks or jobs.

Examples include:

- Database passwords

- API keys

- JDBC URLs

- Hostnames

- Tokens

- Usernames

Instead, Databricks recommends storing them in **Secret Scopes**.

Benefits:

- Improved security

- Centralized credential management

- Easier credential rotation

- Prevents accidental exposure

**2. Types of Secret Scopes**

Databricks supports two types.

**Azure Key Vault-backed Secret Scope**

Secrets remain stored in **Azure Key Vault**.

Databricks only retrieves them when requested.

Advantages:

- Enterprise-grade security

- Centralized secret management

- Azure-managed encryption

- Works well across multiple services

**Databricks-backed Secret Scope**

Secrets are stored directly inside Databricks.

Advantages:

- Simple setup

- No Azure Key Vault required

- Good for development environments

**3. Azure Key Vault-backed Architecture**

Notebook\
│\
dbutils.secrets.get()\
│\
Secret Scope\
│\
Azure Key Vault\
│\
Secret

Databricks never requires the notebook to contain the actual secret value.

**4. Creating an Azure Key Vault**

The lesson creates a Key Vault in Azure.

Configuration includes:

- Resource Group

- Unique Key Vault name

- Region

- Networking

- Tags

The Key Vault becomes the secure storage location for secrets.

**5. Network Security**

The Key Vault is configured with:

- Selected Networks

- Databricks Virtual Network (VNet)

- Trusted Microsoft Services

- Firewall rules

- Local IP whitelist

This restricts access to approved networks only.

**6. Granting Databricks Access**

Databricks must receive permission to access the Key Vault.

The lesson assigns:

Azure Databricks\
\
↓\
\
Key Vault Administrator Role

This allows Databricks to retrieve secrets securely.

**7. Creating an Azure Key Vault-backed Secret Scope**

A Secret Scope is created inside Databricks by providing:

- Scope Name

- Key Vault DNS Name

- Azure Resource ID

Once created, Databricks can reference secrets stored inside Azure Key Vault.

**8. DBUtils Secrets Module**

Secret management is performed through the **DBUtils Secrets** module.

Main commands include:

dbutils.secrets.help()

Available operations include:

- List scopes

- List secrets

- Get secrets

**9. Listing Secret Scopes**

To view available scopes:

dbutils.secrets.listScopes()

Example output:

AKV\
DB-Scope

This displays every Secret Scope accessible to the current user.

**10. Listing Secrets**

To see secrets inside a scope:

dbutils.secrets.list("AKV")

Initially the scope contains no secrets.

After adding secrets to Azure Key Vault, they become visible through Databricks.

**11. Adding Secrets to Azure Key Vault**

The lesson creates a secret:

DBPassword

Stored securely inside Azure Key Vault.

Once added:

Azure Key Vault\
\
↓\
\
Databricks Secret Scope\
\
↓\
\
Notebook Access

No notebook changes are required beyond calling the secret.

**12. Retrieving Secrets**

Secrets are retrieved using:

dbutils.secrets.get(scope, key)

Example:

dbutils.secrets.get(\
"AKV",\
"DBPassword"\
)

Databricks automatically **redacts** the returned value in notebook output to prevent accidental disclosure.

**13. Databricks-backed Secret Scopes**

Unlike Azure-backed scopes, these store secrets inside Databricks itself.

They are managed using the **Databricks CLI**.

Workflow:

Databricks CLI\
\
↓\
\
Create Scope\
\
↓\
\
Add Secret\
\
↓\
\
Retrieve with DBUtils

**14. Installing Databricks CLI**

The lesson installs the Databricks CLI on Windows using **Winget**.

After installation:

databricks -v

verifies that the CLI is installed successfully.

**15. Authenticating the CLI**

The CLI is authenticated using:

databricks auth login

Authentication requires:

- Workspace URL

- User login

- Profile creation

Once authenticated, CLI commands can manage Databricks resources.

**16. Creating a Databricks-backed Scope**

Using the CLI:

databricks secrets create-scope

creates a new Secret Scope.

Example:

DB-Scope

The scope becomes immediately available inside Databricks.

**17. Adding Secrets via CLI**

Secrets are added using:

databricks secrets put-secret

Example:

DBHost

with a value such as:

xyz.com

The CLI securely stores the value inside the Databricks-backed Secret Scope.

**18. Viewing Secrets**

Inside Databricks:

dbutils.secrets.list("DB-Scope")

shows available secret names.

To retrieve a specific secret:

dbutils.secrets.get(\
"DB-Scope",\
"DBHost"\
)

The value is masked in notebook output.

**19. Using Secrets in Code**

Secrets can be injected directly into application code.

Examples include:

- JDBC URLs

- Database usernames

- Passwords

- API tokens

- Hostnames

- Table names

Instead of hardcoding values:

Notebook\
\
↓\
\
dbutils.secrets.get()\
\
↓\
\
Secure Credential\
\
↓\
\
JDBC Connection

This keeps notebooks secure and portable.

**20. Access Control Lists (ACLs)**

Secret Scopes support **Access Control Lists (ACLs)**.

ACLs determine:

- Who can use a scope

- Who can read secrets

- Who can manage permissions

ACLs are managed through the Databricks CLI.

This allows organizations to enforce least-privilege access.

**21. Azure Key Vault vs Databricks-backed Scopes**

| **Feature**             | **Azure Key Vault-backed** | **Databricks-backed** |
|-------------------------|----------------------------|-----------------------|
| Secret Storage          | Azure Key Vault            | Databricks            |
| Security Management     | Azure                      | Databricks            |
| Setup Complexity        | Higher                     | Simpler               |
| Enterprise Integration  | Excellent                  | Good                  |
| External Reuse          | Yes                        | No                    |
| Requires Databricks CLI | No                         | Yes (for management)  |

**Best Practices**

- Never hardcode passwords, API keys, or tokens in notebooks or jobs.

- Use **Azure Key Vault-backed Secret Scopes** for enterprise production environments where centralized secret management is required.

- Use **Databricks-backed Secret Scopes** for simpler deployments, development, or testing.

- Retrieve secrets with dbutils.secrets.get() so sensitive values remain hidden in notebook output.

- Protect Secret Scopes with **ACLs** to ensure only authorized users and applications can access them.

- Store all connection-related information (such as JDBC URLs, usernames, passwords, and hostnames) in Secret Scopes rather than embedding them in code.

# [README](./../../../README.md)
