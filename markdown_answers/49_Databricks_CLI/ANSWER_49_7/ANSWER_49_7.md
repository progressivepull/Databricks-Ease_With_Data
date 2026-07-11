# ANSWER 49 7

**Question 7**

**Where are Databricks CLI authentication profiles stored?**

**A. .gitignore** ❌ Incorrect

- .gitignore tells Git which files to ignore.

**B. databricks.yaml** ❌ Incorrect

- databricks.yaml is commonly used for Databricks Asset Bundles configuration.

- It does not store CLI authentication profiles.

**C. .databricks.cfg** ✅ Correct

Example

.databricks.cfg

Contains profiles like:

DEV

TEST

PROD

Each profile stores authentication settings.

**D. settings.json** ❌ Incorrect

- Usually an IDE configuration file.

**E. bundle.toml** ❌ Incorrect

- Not the CLI authentication file.

**Key Concept**

**Profiles live in .databricks.cfg.**

# [README](./../../../README.md)
