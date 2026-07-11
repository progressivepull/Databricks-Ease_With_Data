# 36 Row Level Filters in UC

**Row-Level Filters (Row-Level Security) in Unity Catalog**

This lesson explains how **Row-Level Filters** (also called **Row-Level Security**) in Unity Catalog allow different users to see different rows from the **same table** based on security rules. Instead of creating multiple tables or manually filtering data in every query, Unity Catalog automatically applies a Boolean function to each row, ensuring users only see the data they are authorized to access.

**1. What is Row-Level Security?**

Row-Level Security (RLS) restricts **which rows** a user can view within a table.

Instead of hiding an entire table, it hides only specific records.

Example:

Customer Table\
\
User A\
↓\
Only Building rows\
\
User B\
↓\
Only Household rows

Every user queries the same table but receives different results based on security rules.

**2. Why Use Row-Level Filters?**

Many organizations need to protect sensitive information.

Examples include:

- Employee salaries

- Customer regions

- Market segments

- Sales territories

- Departments

- Country-specific data

Instead of maintaining multiple copies of the same table, Row-Level Filters dynamically restrict access.

**3. Example Scenario**

The lesson uses the **customer_raw** table.

Without filtering:

Customer Raw\
\
Building\
Household\
Machinery\
Furniture\
Automobile

Everyone sees every market segment.

Desired behavior:

East Data User\
↓\
Building\
\
Data Engineer\
↓\
Household

This is achieved through a row filter.

**4. Shared Compute Permissions**

Before multiple users can test Row-Level Security, they must share the same compute.

Cluster permission levels:

| **Permission** | **Capability**                            |
|----------------|-------------------------------------------|
| Can Manage     | Full cluster management and configuration |
| Can Restart    | Start and stop the cluster                |
| Can Attach To  | Use the cluster only                      |

The lesson grants the Data Engineer group **Can Attach To**, allowing them to run notebooks without modifying or restarting the cluster.

**5. Metadata-Driven Security**

Instead of hardcoding rules, the lesson creates a metadata table.

Example:

Allowed_Market_Segment\
\
User Email\
Market Segment

Sample data:

eastdata@company.com\
Building\
\
dataengineer@company.com\
Household

This table becomes the central source for authorization rules.

**6. Using CURRENT_USER()**

Databricks provides the built-in function:

CURRENT_USER()

It returns the email address of the person executing the query.

Example:

Current User\
\
↓\
\
eastdata@company.com

or

Current User\
\
↓\
\
dataengineer@company.com

The row filter uses this value to determine which rows the user may access.

**7. Security Logic**

The lesson first creates a SQL query that checks whether the current user is authorized for a market segment.

Logic:

Current User\
\
↓\
\
Metadata Table\
\
↓\
\
Allowed?\
\
↓\
\
True / False

If a matching row exists, access is granted. Otherwise, access is denied.

**8. EXISTS Returns a Boolean**

The security function uses the SQL EXISTS operator.

Behavior:

Match Found\
\
↓\
\
TRUE

No match:

No Match\
\
↓\
\
FALSE

This Boolean result is ideal because row filters require a function that returns **TRUE** or **FALSE**.

**9. Creating the Row Filter Function**

The lesson creates a Unity Catalog function.

Characteristics:

- Input: Market Segment

- Output: Boolean

- Language: SQL

Workflow:

Market Segment\
\
↓\
\
Function\
\
↓\
\
TRUE or FALSE

The function consults the metadata table and verifies whether the current user is authorized for the supplied market segment.

**10. Testing the Function**

Example:

Input\
\
↓\
\
Building\
\
↓\
\
TRUE

because the user is authorized.

Another example:

Input\
\
↓\
\
Household\
\
↓\
\
FALSE

because the current user is not authorized.

This verifies the security logic before applying it to the table.

**11. Dynamic Query Filtering**

The Boolean function can be used directly in a WHERE clause.

Workflow:

Customer Row\
\
↓\
\
Market Segment\
\
↓\
\
Boolean Function\
\
↓\
\
TRUE\
\
↓\
\
Row Returned

or

FALSE\
\
↓\
\
Row Hidden

The filter is evaluated for every row in the table.

**12. Dynamic Views**

Instead of modifying the table, the lesson first creates a **dynamic view**.

Flow:

Table\
\
↓\
\
Boolean Function\
\
↓\
\
Filtered View

Users querying the view automatically see only the rows they are permitted to access.

**13. Updating Security Without Changing Code**

Because authorization is stored in the metadata table, security changes require only updating metadata.

Example:

Original permissions:

East Data\
\
↓\
\
Building

After inserting another row:

East Data\
\
↓\
\
Building\
\
Machinery

The same view now returns both market segments without modifying the SQL logic or the function.

**14. Applying a Row Filter to a Table**

After validating the logic, the function is attached directly to the table.

Conceptually:

Customer Raw Table\
\
↓\
\
Row Filter Function\
\
↓\
\
Automatic Security

Once applied, every query against the table automatically enforces the filter.

**15. Automatic Enforcement**

Users no longer need to remember to add WHERE clauses.

Instead:

SELECT \*\
\
↓\
\
Unity Catalog\
\
↓\
\
Row Filter\
\
↓\
\
Filtered Results

The filtering occurs transparently for every query.

**16. User-Specific Results**

After applying the row filter:

**East Data User** sees:

Building\
\
Machinery

**Data Engineer** sees:

Household

Both users query the same table, but Unity Catalog automatically returns different rows based on the current user.

**17. Allow List vs Deny List**

The lesson demonstrates an **allow list**.

Current logic:

EXISTS\
\
↓\
\
Only listed values are visible

Alternative approach:

NOT EXISTS\
\
↓\
\
Listed values are hidden\
\
Everything else remains visible

This provides flexibility depending on whether your security model is based on allowed or denied values.

**18. Architecture**

User\
\
↓\
\
CURRENT_USER()\
\
↓\
\
Metadata Table\
\
↓\
\
Boolean Function\
\
↓\
\
Row Filter\
\
↓\
\
Customer Table\
\
↓\
\
Visible Rows

The metadata-driven approach centralizes authorization and avoids embedding user-specific logic throughout SQL queries.

**19. Benefits of Row-Level Filters**

Advantages include:

- Fine-grained security

- One physical table for all users

- Centralized authorization

- Automatic filtering

- Easy maintenance

- Dynamic behavior

- Integration with Unity Catalog governance

This simplifies administration while improving data security.

**20. Row-Level Filters vs Dynamic Views**

| **Feature**                     | **Dynamic View** | **Row-Level Filter** |
|---------------------------------|------------------|----------------------|
| Security applied in             | View             | Table                |
| Requires querying the view      | Yes              | No                   |
| Automatic for all table queries | No               | Yes                  |
| Uses Boolean security logic     | Yes              | Yes                  |
| Metadata-driven                 | Yes              | Yes                  |

The lesson first builds and validates the logic with a dynamic view, then applies the same Boolean function directly to the table as a row filter.

**Best Practices**

- Store authorization rules in a **metadata table** rather than hardcoding user names or values in SQL.

- Use **CURRENT_USER()** to dynamically identify the person executing the query.

- Implement row filter functions that return **Boolean (TRUE or FALSE)** values, since Unity Catalog row filters require Boolean logic.

- Validate security logic with **dynamic views** before applying the filter directly to production tables.

- Apply row filters at the **table level** when you want automatic enforcement across all queries.

- Choose an **allow-list (EXISTS)** model when only specific values should be visible, or a **deny-list (NOT EXISTS)** model when only certain values should be hidden.

# [README](./../../../README.md)
