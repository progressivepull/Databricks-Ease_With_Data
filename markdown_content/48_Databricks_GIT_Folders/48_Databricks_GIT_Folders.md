# 48 Databricks GIT Folders

**Databricks Git Folders**

This lesson explains how **Databricks Git Folders (formerly Databricks Repos)** integrate Azure DevOps Git repositories with a Databricks workspace. Git Folders enable version control, collaboration, and CI/CD by allowing notebooks and other code assets to be synchronized between Databricks and Git repositories.

**What are Databricks Git Folders?**

Databricks Git Folders allow you to connect a Git repository directly to your Databricks workspace.

Supported Git operations include:

- Clone repositories

- Commit changes

- Push changes

- Pull updates

- Branch management

This enables developers to manage notebooks and other assets using standard Git workflows instead of storing code only inside the Databricks workspace.

**Why Use Git Folders?**

Git Folders are an essential part of a **CI/CD (Continuous Integration / Continuous Deployment)** workflow.

Benefits include:

- Version control

- Team collaboration

- Change tracking

- Branch-based development

- Easy deployment across environments

Typical deployment flow:

Developer\
↓\
Databricks Workspace\
↓\
Azure DevOps Git Repository\
↓\
Azure Pipelines\
↓\
QA\
↓\
Production

This allows code such as notebooks, workflows, and pipelines to move safely from development to production.

**Azure DevOps Setup**

Before connecting Databricks, Azure DevOps must be configured.

Steps:

1.  Navigate to:

https://dev.azure.com

2.  Create an Azure DevOps Organization (if needed).

3.  Create a Project.

Example:

Ease with Data

4.  Create a Git Repository.

Example repository:

ADBCICD

Repository initialization includes:

- README

- .gitignore

The default branch is:

main

(not master).

**Azure DevOps Components**

Two Azure DevOps services are highlighted:

**Repos**

Stores:

- Notebooks

- Source code

- Configuration files

Uses Git version control.

**Pipelines**

Used later in the course for:

- Automated deployment

- CI/CD

- Environment promotion

Such as:

Dev\
→ QA\
→ Production

**Connecting Databricks to Azure DevOps**

Before creating a Git Folder, Databricks must authenticate with Azure DevOps.

Navigate to:

User Profile\
→ Settings\
→ Linked Accounts

Add Git Credentials.

Provider:

Azure DevOps

Authentication uses:

- Username

- Personal Access Token (PAT)

The PAT is generated from Azure DevOps and allows Databricks to securely access the Git repository.

**Creating a Git Folder**

Navigate to:

Workspace\
→ Create\
→ Git Folder

or

Workspace\
→ Repos\
→ Create Repo

Provide:

- Repository URL

- Git Provider

- Repository name

Databricks clones the remote repository into the workspace.

The Git Folder appears under:

Repos\
Username\
Repository

This local Git Folder stays connected to the remote Azure DevOps repository.

**Sparse Checkout**

Databricks provides an optional feature called **Sparse Checkout**.

Purpose:

- Download only selected folders from a repository.

Useful for:

- Large repositories

- Monorepos

- Reducing local workspace size

In this lesson, the full repository is cloned instead.

**Working with Branches**

After cloning the repository, developers can create and switch branches.

Example:

feature/demo

Branch operations include:

- Create branch

- Switch branch

- Pull changes

- Push changes

Branching allows multiple developers to work independently without affecting the main branch.

**Pulling Changes**

The **Pull** operation retrieves changes from the remote repository.

Azure DevOps\
↓\
Databricks Workspace

This keeps the local Git Folder synchronized with updates made by other developers.

**Creating Project Structure**

Inside the Git Folder, the lesson creates:

notebooks/

Then creates a notebook inside that folder.

Example:

Demo Repo Notebook

Organizing notebooks into folders makes projects easier to maintain and version.

**Notebook Storage Format**

By default, Databricks notebooks are stored as:

.ipynb

The lesson changes the notebook format to:

Source

Benefits:

Python notebooks become:

.py

Advantages:

- Easier Git diffs

- Cleaner version control

- Better code reviews

- More compatible with IDEs

Source format is recommended for CI/CD workflows.

**Adding Code**

Example notebook code:

spark.range(...)

After saving, Databricks detects the notebook as a modified Git file ready for commit.

**Commit and Push**

After making changes:

1.  Select modified files.

2.  Enter a commit message.

Example:

Demo notebook added

3.  Click:

Commit and Push

Databricks performs:

- Git Commit

- Git Push

The notebook is uploaded to Azure DevOps automatically.

**Viewing Repository Changes**

After pushing, Azure DevOps shows:

feature/demo\
notebooks/\
Demo Repo Notebook.py

The notebook source code is stored in Git and available to all team members.

**Version Control**

The lesson demonstrates version control by modifying the notebook.

Example:

\# This is a change

Databricks immediately marks the notebook as:

Modified (M)

This indicates the file differs from the latest committed version.

Developers can:

- Review changes

- Commit again

- Push new versions

This provides complete version history for notebooks.

**Continuous Development Workflow**

Typical workflow:

Create Notebook\
↓\
Edit Notebook\
↓\
Git detects modifications\
↓\
Commit\
↓\
Push\
↓\
Azure DevOps Repository

Every change becomes part of the project's Git history, making collaboration and rollback easier.

**Future CI/CD Integration**

This lesson prepares for future deployment automation using:

- Azure Pipelines

- Databricks Asset Bundles (DABs)

- Databricks CLI

The goal is to automate deployment of notebooks, workflows, and pipelines across environments without manual copying.

**Key Takeaways**

- **Databricks Git Folders** integrate Azure DevOps Git repositories directly into the Databricks workspace.

- Git operations such as **clone, commit, push, pull, and branch management** are supported within Databricks.

- Azure DevOps must be configured with an **organization, project, and Git repository** before integration.

- Databricks connects to Azure DevOps using **Git credentials** (username and Personal Access Token).

- Git Folders can be created from the **Workspace** or **Repos** section.

- **Sparse Checkout** allows cloning only selected folders when working with large repositories.

- Developers should use **feature branches** for isolated development before merging into the main branch.

- Saving notebooks in **Source** format (.py) instead of .ipynb improves Git version control and code reviews.

- Databricks automatically detects modified files, allowing developers to **commit and push** changes directly to Azure DevOps.

- Git Folders are a foundational component for implementing **CI/CD pipelines** with Azure Pipelines, Databricks Asset Bundles (DABs), and the Databricks CLI.

# [README](./../../../README.md)
