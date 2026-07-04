# EXPLANATION 15 2

**Question 2**

**Which other names are commonly used for the MERGE operation?**

**Correct Answer:**\
✅ **UPSERT and Slowly Changing Dimension (SCD) Type 1**

**Explanation**

**UPSERT**

UPSERT means:

- **UP**date existing rows

- In**SERT** new rows

MERGE performs exactly this behavior.

**SCD Type 1**

Slowly Changing Dimension (SCD) Type 1 overwrites existing values.

Example:

Old Address

123 Main Street

New Address

456 Oak Street

MERGE simply replaces the old value.

No history is kept.

**Memory Trick**

MERGE\
\
↓\
\
UPSERT\
\
↓\
\
SCD Type 1

**YouTube**

**SCD Type 1 Using MERGE**

https://www.youtube.com/results?search_query=Delta+Lake+SCD+Type+1

# [README](./../../../README.md)
