# ANSWER 10 6

**Question 6**

**Which Azure RBAC role must be assigned to the Access Connector so it can access the storage account?**

**A. Reader** ❌ Incorrect

- Reader only allows viewing Azure resources.

- It cannot read or write storage data.

**B. Contributor** ❌ Incorrect

- Contributor manages Azure resources.

- It does not automatically provide data access inside storage accounts.

**C. Storage Blob Data Contributor** ✅ Correct

This role allows:

- Read blobs

- Write blobs

- Delete blobs

- Manage files in ADLS Gen2

It gives Unity Catalog the permissions it needs.

**D. Owner** ❌ Incorrect

- Owner is excessive.

- Least-privilege principles recommend using Storage Blob Data Contributor instead.

**E. Storage Account Key Operator** ❌ Incorrect

- This role manages storage account keys.

- Unity Catalog uses Managed Identity instead.

**Memory Trick**

Managed Identity needs:

Storage Blob Data Contributor

# [README](./../../../README.md)
