# ANSWER 14 8

**Question 8**

**What is the main advantage of Deep Clone over CTAS?**

**A. It requires no storage space.** ❌ Incorrect

- Deep Clone creates a full copy.

**B. It copies only metadata.** ❌ Incorrect

- That's closer to a shallow clone.

**C. It preserves metadata, schema, table properties, and data, creating a true replica.** ✅ Correct

Deep Clone copies:

- Data

- Schema

- Metadata

- Properties

- Comments

- Constraints

- Delta transaction history needed for the clone

Think of it as making a complete duplicate.

**D. It automatically updates whenever the source table changes.** ❌ Incorrect

- The clone is independent after creation.

**E. It creates only temporary copies.** ❌ Incorrect

- Deep Clones are permanent tables.

**Memory Trick**

Deep Clone =

Everything

# [README](./../../../README.md)
