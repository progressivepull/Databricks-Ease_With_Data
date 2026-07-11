# EXPLANATION 43 4

**Question 4**

**Before querying an external database with Lakehouse Federation, what must be created first?**

**Correct Answer:**\
**C. A Connection**

**Why C is Correct**

The setup process is:

Step 1

CREATE CONNECTION

↓

Step 2

CREATE FOREIGN CATALOG

↓

Query Tables

The Connection stores:

- hostname

- port

- authentication

- database connectivity information

The Foreign Catalog then uses that Connection.

**Why the other choices are wrong**

You cannot create a Foreign Catalog until a Connection exists.

**Memory Tip**

**Connection First**

**Individual YouTube Video**

https://www.youtube.com/watch?v=mdw5j0l7K2Y

**YouTube Search**

https://www.youtube.com/results?search_query=CREATE+CONNECTION+Lakehouse+Federation

------------------------------------------------------------------------

# [README](./../../../README.md)
