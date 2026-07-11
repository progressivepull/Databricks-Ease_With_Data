# ANSWER 25 6

**Question 6**

**Which Auto Loader feature allows you to specify data types for only selected columns while automatically inferring the rest?**

**A. Schema Merge ❌ Incorrect**

Schema Merge allows schemas to evolve.

It doesn't override selected column types.

------------------------------------------------------------------------

**B. Schema Validation ❌ Incorrect**

Not an Auto Loader feature.

**C. Schema Hints ✅ Correct**

Example:

Incoming CSV:

CustomerID,Age,Salary

You specify:

.option(

"cloudFiles.schemaHints",

"CustomerID STRING"

)

Result:

| **Column** | **Type** |
|------------|----------|
| CustomerID | STRING   |
| Age        | inferred |
| Salary     | inferred |

Only selected columns are overridden.

------------------------------------------------------------------------

**D. Schema Registry ❌ Incorrect**

Used in systems like Kafka.

Not Auto Loader.

------------------------------------------------------------------------

**E. Schema Override ❌ Incorrect**

Not an Auto Loader option.

------------------------------------------------------------------------

**Why C is correct**

Schema Hints let you control specific columns while Auto Loader infers the remainder.

------------------------------------------------------------------------

# [README](./../../../README.md)
