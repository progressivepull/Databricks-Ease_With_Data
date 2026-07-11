# 37 Column Level Masking in UC

**Column-Level Masking in Unity Catalog**

This lesson explains **Column-Level Masking** in Unity Catalog, a security feature that hides or masks sensitive values in specific columns while still allowing authorized users to view the original data. Unlike Row-Level Security, which filters rows, Column-Level Masking protects **individual column values** based on user identity or group membership. The lesson demonstrates two implementation methods: a **custom metadata table** and the built-in **is_member()** function.

------------------------------------------------------------------------

**1. What is Column-Level Masking?**

Column-Level Masking dynamically hides sensitive column values without removing the column itself.

Instead of deleting or permanently redacting data, Unity Catalog decides at query time what each user is allowed to see.

Example:

Customer Table\
\
Phone Number\
\
User A (Admin)\
↓\
555-123-4567\
\
User B\
↓\
\*\*\*-\*\*\*-\*\*\*\*

The same table returns different column values depending on the user.

------------------------------------------------------------------------

**2. Why Use Column Masking?**

Many organizations must protect **Personally Identifiable Information (PII)** while still storing it.

Common examples:

- Social Security Numbers

- Aadhaar Numbers

- Phone Numbers

- Email Addresses

- Credit Card Numbers

- Bank Accounts

Authorized users (such as HR or Administrators) should see the original values, while other users should only see masked values.

------------------------------------------------------------------------

**3. Row-Level Security vs Column-Level Masking**

| **Feature** | **Row-Level Security**       | **Column-Level Masking** |
|-------------|------------------------------|--------------------------|
| Protects    | Rows                         | Columns                  |
| Hides       | Entire records               | Individual values        |
| Returns     | Fewer rows                   | Same rows, masked values |
| Example     | Hide all Household customers | Hide Phone Number column |

Row filters determine **which records** a user sees, while column masking determines **what values** within those records are visible.

------------------------------------------------------------------------

**4. Example Scenario**

The lesson masks the **C_PHONE** column in the customer_raw table.

Requirements:

- **Admin** users should see the real phone number.

- **Regular users** should see:

\*\*\*-\*\*\*-\*\*\*\*

The rest of the row remains visible.

------------------------------------------------------------------------

**5. Method 1 – Metadata-Driven Security**

The first approach uses a metadata table.

Example:

User_Groups\
\
User Email\
Group

Sample data:

eastdata@company.com\
Admin\
\
dataengineer@company.com\
User

This metadata drives the masking logic without hardcoding user names into the function.

------------------------------------------------------------------------

**6. Using CURRENT_USER()**

The built-in SQL function:

CURRENT_USER()

returns the email address of the person executing the query.

Workflow:

CURRENT_USER()\
\
↓\
\
Metadata Table\
\
↓\
\
Determine Group\
\
↓\
\
Apply Mask

This enables dynamic masking based on the logged-in user.

------------------------------------------------------------------------

**7. Masking Logic**

The lesson first develops the SQL logic before wrapping it in a function.

Logic:

Current User\
\
↓\
\
Find Group\
\
↓\
\
Admin?\
\
↓\
\
Yes → Return Phone Number\
\
No → Return "\*\*\*-\*\*\*-\*\*\*\*"

This logic becomes the core of the masking function.

------------------------------------------------------------------------

**8. CASE Expression**

The masking decision is implemented using a SQL CASE statement.

Conceptually:

CASE\
\
Admin\
\
↓\
\
Actual Value\
\
Else\
\
↓\
\
Masked Value

The function returns a **string**, not a Boolean.

------------------------------------------------------------------------

**9. Creating the Masking Function**

The masking function is registered in Unity Catalog.

Characteristics:

- Input: Phone Number

- Output: String

- Language: SQL

Possible outputs:

555-123-4567

or

\*\*\*-\*\*\*-\*\*\*\*

depending on the user.

------------------------------------------------------------------------

**10. Testing the Function**

When executed as an Admin:

Input:

8823456789

Output:

8823456789

When executed as a regular user:

Input:

8823456789

Output:

\*\*\*-\*\*\*-\*\*\*\*

The same function returns different results for different users.

------------------------------------------------------------------------

**11. Applying a Mask to a Table**

After validating the function, it is attached to the C_PHONE column.

Conceptually:

Customer Raw\
\
↓\
\
C_PHONE\
\
↓\
\
Mask Function\
\
↓\
\
Protected Column

Every query against that table now automatically applies the masking logic.

------------------------------------------------------------------------

**12. Automatic Masking**

Once the mask is applied:

SELECT \*\
\
↓\
\
Unity Catalog\
\
↓\
\
Mask Function\
\
↓\
\
Protected Results

Users no longer need to remember special queries—the masking happens automatically.

------------------------------------------------------------------------

**13. Different Users See Different Values**

After the mask is applied:

**Admin**

Customer\
\
Phone\
\
555-123-4567

**Data Engineer**

Customer\
\
Phone\
\
\*\*\*-\*\*\*-\*\*\*\*

Both users query the same table but receive different column values.

------------------------------------------------------------------------

**14. Removing a Mask**

Masks can be removed without dropping the table.

Conceptually:

Table\
\
↓\
\
Drop Mask\
\
↓\
\
Original Values Restored

After removing the mask, all users again see the original phone numbers (subject to other permissions).

------------------------------------------------------------------------

**15. Method 2 – Using is_member()**

Instead of maintaining a metadata table, Databricks provides the built-in function:

is_member()

This function checks whether the current user belongs to a specified group.

Example:

is_member("admins")\
\
↓\
\
TRUE

or

FALSE

This eliminates the need to maintain a custom user-to-group mapping table.

------------------------------------------------------------------------

**16. Group-Based Masking**

The second masking function uses group membership directly.

Workflow:

Current User\
\
↓\
\
is_member("admins")\
\
↓\
\
TRUE\
\
↓\
\
Show Phone\
\
FALSE\
\
↓\
\
Mask Phone

This approach is simpler and integrates directly with Databricks or identity-provider groups.

------------------------------------------------------------------------

**17. Metadata vs is_member()**

| **Feature**          | **Metadata Table** | **is_member()** |
|----------------------|--------------------|-----------------|
| Custom mapping       | Yes                | No              |
| Requires maintenance | Yes                | No              |
| Uses groups          | Optional           | Yes             |
| Dynamic              | Yes                | Yes             |
| Simplicity           | More complex       | Simpler         |

Both methods produce the same masking behavior but differ in how authorization is determined.

------------------------------------------------------------------------

**18. Architecture**

User\
\
↓\
\
CURRENT_USER()\
\
or\
\
is_member()\
\
↓\
\
Mask Function\
\
↓\
\
Customer Table\
\
↓\
\
Phone Column\
\
↓\
\
Original or Masked Value

Unity Catalog evaluates the masking function automatically whenever the protected column is queried.

------------------------------------------------------------------------

**19. Relationship to Unity Catalog Security**

The lesson completes the Unity Catalog security model introduced in previous lessons:

- **Object-Level Security** → Controls access to catalogs, schemas, tables, and other objects.

- **Row-Level Security** → Controls which rows are visible.

- **Column-Level Masking** → Controls which column values are visible.

Together, these features provide layered, fine-grained governance over data access.

------------------------------------------------------------------------

**Best Practices**

- Use **Column-Level Masking** for PII and other sensitive fields that must remain stored but should not be visible to every user.

- Prefer the built-in **is_member()** function when access decisions align with existing Databricks or identity-provider groups, since it avoids maintaining custom metadata tables.

- Use a **metadata-driven approach** when masking rules require custom business logic beyond simple group membership.

- Return the **same data type** from the masking function as the protected column (for example, a string for phone numbers).

- Combine **Object-Level Security**, **Row-Level Security**, and **Column-Level Masking** to build a comprehensive, layered security model in Unity Catalog.

# [README](./../../../README.md)
