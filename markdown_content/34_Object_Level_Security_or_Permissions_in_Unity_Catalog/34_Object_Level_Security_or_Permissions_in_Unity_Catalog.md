# 34 Object Level Security or Permissions in Unity Catalog

**Object-Level Security (Permissions) in Unity Catalog**

This lesson explains how **Unity Catalog Object-Level Security** controls access to catalogs, schemas, tables, views, volumes, functions, and models. It covers the Unity Catalog object hierarchy, inheritance of permissions, top-down and bottom-up permission models, common privileges, and how to manage permissions using both the Databricks UI and SQL.

**1. What is Object-Level Security?**

Object-Level Security is the process of granting permissions on individual Unity Catalog objects.

Permissions determine:

- Who can view objects

- Who can read data

- Who can modify data

- Who can create objects

- Who can manage permissions

This enables organizations to implement fine-grained access control across their data platform.

**2. Unity Catalog Object Hierarchy**

Unity Catalog organizes objects in a hierarchical structure.

Metastore\
│\
├── Catalog\
│ │\
│ ├── Schema\
│ │ │\
│ │ ├── Tables\
│ │ ├── Views\
│ │ ├── Volumes\
│ │ ├── Functions\
│ │ └── Models

Permissions can be assigned at any level of this hierarchy.

**3. Permission Inheritance**

Unity Catalog supports **permission inheritance**.

If a permission is granted on a parent object, child objects automatically inherit it.

Example:

Catalog\
│\
├── Schema\
│ │\
│ ├── Table

Granting **SELECT** on the Catalog allows the permission to flow down to the Schema and then to the Tables beneath it.

**4. Top-Down Permission Model**

Top-down (parent-to-child) permission assignment is used for **bulk access**.

Example:

Grant SELECT on Catalog\
\
↓\
\
All Schemas inherit\
\
↓\
\
All Tables inherit

This approach is ideal when users need access to an entire catalog or schema rather than individual objects.

**5. Bottom-Up Permission Model**

Bottom-up permission assignment is used for **fine-grained access**.

Example:

Grant SELECT on Table\
\
↓\
\
Grant USE SCHEMA\
\
↓\
\
Grant USE CATALOG

This approach gives users access to only specific objects instead of everything under a catalog.

**6. Bulk vs Fine-Grained Permissions**

**Bulk Permissions**

Grant at:

- Catalog

- Schema

Benefits:

- Easier administration

- Less configuration

- Automatic inheritance

**Fine-Grained Permissions**

Grant at:

- Table

- View

- Volume

- Function

Benefits:

- Better security

- Least-privilege access

- Object-specific permissions

**7. Metastore Administrator**

The **Metastore Administrator** is the highest administrative role.

Capabilities include:

- Create catalogs

- Create external locations

- Create credentials

- Manage securable objects

- Assign permissions

Metastore Admins effectively control all child objects beneath the Metastore.

**8. Granting CREATE CATALOG**

The lesson demonstrates granting permission to create catalogs.

SQL example:

GRANT CREATE CATALOG\
ON METASTORE\
TO \`DE_GROUP\`;

After this permission is granted, members of the Data Engineer group can create new catalogs even though they are not Metastore Administrators.

**9. Viewing Existing Permissions**

Permissions can be inspected with SQL.

Example:

SHOW GRANTS\
ON METASTORE;

This displays:

- Principals

- Granted privileges

- Target object

Useful for auditing and troubleshooting access.

**10. Catalog Browse Permission**

The **Browse** privilege allows users to:

- See that catalogs exist

- View metadata

- View lineage

It **does not** allow users to query or modify data.

Objects appear visible but inaccessible until additional permissions are granted.

**11. Removing Browse Permission**

If Browse permission is revoked:

- The catalog disappears from Catalog Explorer.

- Users cannot see the catalog.

- No metadata or lineage is visible.

This effectively hides the catalog from unauthorized users.

**12. Required Permissions for Reading Tables**

To query a table, users need more than **SELECT**.

Required permissions are:

- **USE CATALOG**

- **USE SCHEMA**

- **SELECT**

Without **USE CATALOG** or **USE SCHEMA**, a user cannot access the table even if SELECT has been granted.

**13. Reading Volumes**

Volumes use their own privilege.

READ VOLUME

Granting **READ VOLUME** allows users to read files stored in Unity Catalog Volumes.

It does **not** grant access to tables.

**14. Inherited Permissions**

Permissions granted at higher levels automatically appear on child objects as **Inherited**.

Example:

Catalog\
\
↓\
\
Schema\
\
↓\
\
Table

If SELECT is granted at the Catalog level, the Table's Permissions page will indicate that SELECT is inherited from the parent.

**15. Fine-Grained Access Example**

The lesson grants a Data Engineer group access to:

- One table (customer_raw)

- One volume (landing)

Required permissions:

- SELECT on the table

- READ VOLUME on the volume

- USE SCHEMA

- USE CATALOG

Result:

- Users can access only the authorized objects.

- Other objects remain hidden.

**16. Browse vs Select**

Example:

Browse\
\
↓\
\
Object Visible\
\
↓\
\
Cannot Query

versus

Select\
\
↓\
\
Object Visible\
\
↓\
\
Can Query Data

Browse provides discovery, while SELECT provides data access.

**17. Common Unity Catalog Privileges**

**Read Privileges**

- SELECT

- READ VOLUME

- EXECUTE (Functions)

**Create Privileges**

- CREATE SCHEMA

- CREATE TABLE

- CREATE FUNCTION

- CREATE VIEW

**Modify Privileges**

- MODIFY

- WRITE VOLUME

- REFRESH (Materialized Views)

These permissions determine the operations users can perform on Unity Catalog objects.

**18. ALL PRIVILEGES**

Granting **ALL PRIVILEGES** gives nearly every operational permission on an object.

Includes capabilities such as:

- Read

- Write

- Create

- Modify

However, it **does not** include the ability to manage permissions or ownership.

**19. MANAGE Privilege**

**MANAGE** is separate from **ALL PRIVILEGES**.

Users with MANAGE can:

- Rename objects

- Drop objects

- Change permissions

- Act similarly to an owner

Because of its power, MANAGE should be granted only to trusted administrators.

**20. Managing Permissions**

Permissions can be managed in two ways.

**Using the Catalog Explorer UI**

Administrators can:

- Grant permissions

- Revoke permissions

- View inherited privileges

**Using SQL**

Example:

GRANT SELECT\
ON TABLE dev.bronze.customer_raw\
TO \`DE_GROUP\`;

SQL is preferred for automation, scripting, and Infrastructure-as-Code.

**21. Practical Permission Strategies**

**Top-Down Strategy**

Grant permissions at the Catalog or Schema level when many users need access to the same set of objects.

**Bottom-Up Strategy**

Grant permissions at the Table or Volume level when users need access to only a few specific objects.

Using the appropriate strategy helps balance ease of administration with security.

**Best Practices**

- Use the **top-down** permission model for broad, shared access and the **bottom-up** model for least-privilege, object-specific access.

- Remember that **SELECT** alone is not enough—users also need **USE CATALOG** and **USE SCHEMA** to query tables.

- Grant **BROWSE** only when users need to discover catalogs, schemas, or lineage without accessing the data.

- Reserve the **MANAGE** privilege for administrators, since it allows renaming, dropping objects, and changing permissions.

- Use **groups** (such as Data Engineers or Data Analysts) instead of granting permissions directly to individual users whenever possible to simplify administration.

- Prefer **SQL GRANT/REVOKE** statements for repeatable, automated permission management, while the Catalog Explorer UI is convenient for interactive administration.

# [README](./../../../README.md)
