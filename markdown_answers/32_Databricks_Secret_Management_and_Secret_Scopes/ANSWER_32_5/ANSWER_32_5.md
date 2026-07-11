# ANSWER 32 5

**Question 5**

**Which DBUtils command displays all Secret Scopes that are accessible to the current user?**

**A. dbutils.secrets.showScopes() ❌ Incorrect**

- Not a valid DBUtils command.

------------------------------------------------------------------------

**B. dbutils.secrets.listSecrets() ❌ Incorrect**

- Lists secrets within a scope, not the available scopes themselves.

------------------------------------------------------------------------

**C. dbutils.secrets.listScopes() ✅ Correct**

Example:

dbutils.secrets.listScopes()

Returns the Secret Scopes the current user can access.

------------------------------------------------------------------------

**D. dbutils.secrets.helpScopes() ❌ Incorrect**

- Not a valid command.

------------------------------------------------------------------------

**E. dbutils.secrets.displayScopes() ❌ Incorrect**

- Does not exist.

------------------------------------------------------------------------

**Why C is correct**

listScopes() shows all Secret Scopes available to the current user.

------------------------------------------------------------------------

# [README](./../../../README.md)
