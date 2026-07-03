# ANSWER 15 7

**Question 7**

**What is the primary difference between a hard delete and a soft delete?**

**A. Hard delete uses UPDATE, while soft delete uses INSERT.** ❌ Incorrect

- Hard delete uses DELETE.

- Soft delete often uses UPDATE.

**B. Hard delete preserves history, while soft delete removes it permanently.** ❌ Incorrect

- This is exactly backwards.

**C. Hard delete permanently removes records, while soft delete marks them inactive and preserves history.** ✅ Correct

Hard Delete:

Customer\
\
↓\
\
DELETE\
\
↓\
\
Gone

Soft Delete:

Customer\
\
↓\
\
IS_ACTIVE = FALSE\
\
↓\
\
Still Exists

Advantages:

- Audit history

- Compliance

- Easier recovery

- Historical reporting

**D. Hard delete works only on Delta tables, while soft delete works only on Parquet tables.** ❌ Incorrect

- Both techniques work on many storage formats.

**E. There is no functional difference between them.** ❌ Incorrect

- They are very different.

**Memory Trick**

Hard Delete

↓

Remove Record

Soft Delete

↓

Hide Record

------------------------------------------------------------------------

# [README](./../../../README.md)
