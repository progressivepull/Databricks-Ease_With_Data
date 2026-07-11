# ANSWER 36 2

**Question 2**

**Why are Row-Level Filters preferred over maintaining multiple copies of the same table?**

**A. They permanently delete unauthorized rows. ❌ Incorrect**

- Unauthorized rows are **never deleted**.

- They are simply hidden from users who lack permission.

------------------------------------------------------------------------

**B. They dynamically restrict access based on security rules while allowing all users to query a single physical table. ✅ Correct**

Instead of:

Sales_East

Sales_West

Sales_North

Sales_South

You have:

Sales

Unity Catalog applies filters automatically.

Benefits:

- one copy of the data

- easier maintenance

- no synchronization problems

- consistent governance

------------------------------------------------------------------------

**C. They require every query to include a custom WHERE clause. ❌ Incorrect**

- That's exactly what Row-Level Filters eliminate.

- Users write normal SQL.

Instead of:

WHERE region='East'

Unity Catalog automatically adds the filtering logic behind the scenes.

------------------------------------------------------------------------

**D. They eliminate the need for Unity Catalog. ❌ Incorrect**

- Row-Level Filters are a **Unity Catalog feature**.

------------------------------------------------------------------------

**E. They convert tables into views automatically. ❌ Incorrect**

- Tables remain tables.

------------------------------------------------------------------------

**Why B is correct**

Row-Level Filters allow many users to securely share one physical table while automatically seeing only authorized rows.

------------------------------------------------------------------------

# [README](./../../../README.md)
