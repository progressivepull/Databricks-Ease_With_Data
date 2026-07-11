# EXPLANATION 48 5

**Question 5**

**What is the purpose of the Sparse Checkout feature?**

**Correct Answer:**\
**B. To clone only selected folders from a repository, reducing the local workspace size**

**Why B is Correct**

Large repositories can contain thousands of files.

Sparse Checkout allows you to clone only the folders you actually need.

Example:

Repository

│

├── ETL

├── ML

├── Dashboards

├── Tests

└── Documentation

Clone only:

ETL/

Benefits include:

- Faster cloning

- Less disk usage

- Simpler workspace navigation

Git Folders includes configuration for sparse checkout.

**Why the other choices are wrong**

Sparse Checkout does not:

- compress Git history

- remove commits

- improve SQL performance

**Memory Tip**

**Sparse = Partial Clone**

**Individual YouTube Video**

[<u>YouTube video link</u>](https://www.youtube.com/watch?v=Jk0LED7Fsh4)

**YouTube Search**

https://www.youtube.com/results?search_query=Git+Sparse+Checkout

# [README](./../../../README.md)
