# ANSWER 14 9

**Question 9**

**Which statement correctly describes a Shallow Clone?**

**A. It immediately copies all physical data files.** ❌ Incorrect

- That is a Deep Clone.

**B. It copies metadata while initially referencing the original table's data files.** ✅ Correct

Initially:

Original Data Files\
\
↑\
\
Shallow Clone

The clone shares the original files.

Advantages:

- Fast

- Minimal storage

- Quick testing

**C. It permanently synchronizes with all future changes in the source table.** ❌ Incorrect

- It is not a continuously synchronized replica.

**D. It cannot be queried until data is copied.** ❌ Incorrect

- It is immediately queryable.

**E. It deletes the original table after cloning.** ❌ Incorrect

- The source table remains unchanged.

**Memory Trick**

Shallow Clone =

Shares Data

Deep Clone =

Copies Data

# [README](./../../../README.md)
