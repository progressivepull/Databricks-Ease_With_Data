# ANSWER 37 9

**Question 9**

**What is an advantage of using is_member() instead of a metadata table for column masking?**

**A. It requires maintaining a custom user-to-group mapping table. ❌ Incorrect**

That's actually what is_member() helps avoid.

**B. It works only for administrators. ❌ Incorrect**

It works for any authenticated user.

**C. It simplifies authorization by using existing Databricks or identity-provider groups without maintaining custom mappings. ✅ Correct**

Instead of:

Metadata Table

you simply use:

is_member('HR')

If HR membership changes:

- Azure AD

- Okta

- Databricks Groups

already contain the updated membership.

No metadata maintenance.

**D. It permanently stores masked values in the table. ❌ Incorrect**

Masking never changes stored data.

**E. It replaces Object-Level Security. ❌ Incorrect**

Object-Level Security still controls access to catalogs, schemas, and tables.

**Why C is correct**

is_member() leverages existing identity-provider or Databricks group memberships, reducing administrative overhead and eliminating the need for a separate authorization mapping table.

# [README](./../../../README.md)
