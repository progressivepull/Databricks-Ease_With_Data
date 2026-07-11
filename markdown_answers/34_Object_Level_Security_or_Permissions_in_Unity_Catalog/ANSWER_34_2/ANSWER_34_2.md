# ANSWER 34 2

**Question 2**

**Which of the following correctly represents the Unity Catalog object hierarchy?**

**A. Schema → Catalog → Metastore → Table ❌ Incorrect**

The order is backwards.

**B. Metastore → Catalog → Schema → Tables, Views, Volumes, Functions, and Models ✅ Correct**

Unity Catalog hierarchy:

Metastore

↓

Catalog

↓

Schema

↓

Tables

Views

Volumes

Functions

Models

Each level contains the next level.

Think of it like folders:

Metastore

└── Catalog

└── Schema

├── Table

├── View

├── Volume

├── Function

└── Model

**C. Catalog → Metastore → Schema → Views ❌ Incorrect**

A Catalog belongs inside a Metastore.

**D. Table → Schema → Catalog → Metastore ❌ Incorrect**

This is the reverse order.

**E. Volume → Table → Schema → Catalog ❌ Incorrect**

Volumes are child objects, not parent objects.

**Why B is correct**

The Unity Catalog hierarchy always starts with the **Metastore** and becomes more specific as you move downward.

# [README](./../../../README.md)
