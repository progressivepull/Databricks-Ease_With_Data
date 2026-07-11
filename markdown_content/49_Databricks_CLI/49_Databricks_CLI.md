# 49 Databricks CLI

**Databricks CLI (Command Line Interface)**

This lesson introduces the **Databricks CLI (Command Line Interface)**, a command-line tool that allows administrators and developers to manage Databricks workspaces and accounts using terminal commands. The CLI is built on top of the **Databricks REST API**, making it useful for automation, scripting, and CI/CD pipelines.

**What is Databricks CLI?**

The **Databricks CLI** is a command-line utility that enables users to interact with Databricks services without using the web interface.

It is essentially a **wrapper around the Databricks REST API**, providing easier-to-use commands for common administrative and development tasks.

**What Can the Databricks CLI Do?**

The CLI can manage both:

- **Databricks Accounts**

- **Databricks Workspaces**

Examples include:

- Catalogs

- Schemas

- Workspaces

- Jobs

- Clusters

- Unity Catalog

- Groups

- Metastores

- Bundles

- Pipelines

- Repositories

This makes the CLI useful for both administrators and DevOps engineers.

**Why Use the CLI?**

Instead of manually clicking through the Databricks UI, the CLI allows automation.

Benefits include:

- Automation

- Scripting

- CI/CD

- Infrastructure as Code

- Repeatable deployments

- Faster administration

Example workflow:

Developer\
↓\
Databricks CLI\
↓\
REST API\
↓\
Databricks Workspace

The CLI sends commands to the Databricks REST API, which performs the requested operation.

**Installing the Databricks CLI**

Installation depends on the operating system.

**Windows**

Uses:

winget

Example:

winget install Databricks.DatabricksCLI

**Linux**

Common methods:

- Curl

- Source builds

**macOS**

Common methods:

- Homebrew

- Curl

Databricks provides installation documentation for each platform.

**Verifying Installation**

After installation, verify the CLI:

databricks -v

Example output:

0.262

If the version is displayed, the CLI has been installed successfully.

**Authentication Methods**

The lesson covers two authentication methods.

**1. U2M (User-to-Machine)**

Uses a normal user account.

Ideal for:

- Developers

- Interactive use

- Local development

Authentication launches a browser where the user signs in using Microsoft Entra ID (Azure AD).

**2. M2M (Machine-to-Machine)**

Uses a **Service Principal**.

Ideal for:

- CI/CD pipelines

- Automation

- Azure DevOps

- Scheduled deployments

Instead of a user account, applications authenticate using credentials assigned to a service principal.

**User-to-Machine (U2M) Authentication**

Authentication command:

databricks auth login --host \<workspace-url\>

During setup:

- Specify the workspace URL.

- Choose a profile name.

- Complete browser authentication.

- The profile is saved locally.

Once authenticated, the CLI can issue commands against the workspace.

**Authentication Profiles**

Configured profiles can be viewed using:

databricks auth profiles

A profile stores authentication information for a workspace or account.

Example profile:

SK

Multiple profiles can exist for different workspaces or accounts.

**Configuration File**

CLI profiles are stored in:

.databricks.cfg

This configuration file contains:

- Profile names

- Workspace hosts

- Account hosts

- Authentication information

Having multiple profiles allows switching between different Databricks environments without re-authenticating.

**Using Help**

Every CLI command supports help.

Example:

databricks --help

Help can also be used on subcommands:

databricks catalogs --help

This displays available operations and required parameters.

**Working with Catalogs**

Example command:

databricks catalogs list

This lists all Unity Catalog catalogs available to the authenticated user.

**Working with Schemas**

Schemas can also be managed through the CLI.

Help command:

databricks schemas --help

Supported operations include:

- Create

- Delete

- Get

- List

- Update

Example creation:

databricks schemas create schema_cli --catalog-name dev

This creates a new schema named:

schema_cli

inside the **dev** catalog.

**Using Profiles**

Commands should specify which authentication profile to use.

Example:

databricks catalogs list -p SK

Using profiles is recommended because multiple workspaces or accounts may be configured on the same machine.

**Machine-to-Machine (M2M)**

Machine-to-Machine authentication uses a **Service Principal**.

Requirements:

- Client ID

- Client Secret

- Account ID

- Workspace URL

These credentials are added manually to the .databricks.cfg configuration file.

**Service Principal Profiles**

The lesson creates two profiles:

**Account Profile**

SP Account

Used for:

- Account Console operations

**Workspace Profile**

SP Workspace

Used for:

- Workspace operations

Separating these profiles allows the CLI to target either the Databricks account or a specific workspace.

**Account-Level Commands**

After configuring an account profile, account administration commands become available.

Examples include:

**List Metastores**

databricks account metastores list

**List Groups**

databricks account groups list

These commands interact with the Databricks Account Console rather than a workspace.

**Workspace Commands**

Workspace profiles continue to work with normal workspace resources.

Example:

databricks catalogs list -p SPWorkspace

This confirms the service principal has access to the workspace.

**Relationship Between Authentication Methods**

| **Authentication** | **Uses** | **Best For** |
|----|----|----|
| **U2M (User-to-Machine)** | User account | Local development, testing |
| **M2M (Machine-to-Machine)** | Service Principal | CI/CD, automation, Azure DevOps |

Both methods can coexist in the same .databricks.cfg file using separate profiles.

**Databricks Asset Bundles (DABs)**

The lesson concludes by introducing **Databricks Asset Bundles (DABs)**.

The CLI includes bundle commands:

databricks bundle --help

These commands will be used in later lessons to deploy:

- Notebooks

- Jobs

- Pipelines

- Other Databricks assets

from one environment (Dev) to another (QA or Production).

**CI/CD Integration**

The Databricks CLI is a key component of deployment automation.

Typical workflow:

Developer\
↓\
Databricks CLI\
↓\
Databricks Asset Bundles (DABs)\
↓\
Azure DevOps Pipeline\
↓\
Development\
↓\
QA\
↓\
Production

Machine-to-Machine authentication with a Service Principal is the preferred approach for automated deployments because it avoids relying on an individual user's credentials.

**Key Takeaways**

- The **Databricks CLI** is a command-line wrapper around the Databricks REST API for managing both accounts and workspaces.

- It supports automation, scripting, and CI/CD workflows by allowing users to perform Databricks operations from a terminal.

- The CLI can be installed on **Windows (Winget)**, **macOS (Homebrew/Curl)**, and **Linux (Curl/Source Builds)**.

- Installation is verified using databricks -v.

- **User-to-Machine (U2M)** authentication uses a user's Microsoft Entra ID credentials and is best for interactive development.

- **Machine-to-Machine (M2M)** authentication uses a **Service Principal** and is recommended for automation and Azure DevOps pipelines.

- Authentication profiles are stored in the .databricks.cfg file, allowing multiple workspaces and accounts to be managed from one machine.

- The CLI supports operations such as listing catalogs, creating schemas, viewing groups, and managing metastores.

- The built-in --help option provides documentation for available commands and required parameters.

- The Databricks CLI is the primary interface for working with **Databricks Asset Bundles (DABs)**, enabling automated deployment of notebooks, jobs, pipelines, and other assets across development, QA, and production environments.

# [README](./../../../README.md)
