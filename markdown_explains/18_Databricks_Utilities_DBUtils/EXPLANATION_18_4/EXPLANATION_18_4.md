# EXPLANATION 18 4

**Question 3**

**Which DBUtils module is primarily used for file and storage operations?**

**Correct Answer: C. dbutils.fs**

**Explanation**

The **fs** stands for **File System**.

This module manages files stored in:

- DBFS

- Unity Catalog Volumes

- Azure Data Lake

- Amazon S3

- Google Cloud Storage

Common commands:

dbutils.fs.ls()\
\
dbutils.fs.cp()\
\
dbutils.fs.mv()\
\
dbutils.fs.rm()\
\
dbutils.fs.mkdirs()\
\
dbutils.fs.head()

------------------------------------------------------------------------

**Example**

List files

dbutils.fs.ls("/Volumes/catalog/schema/files/")

Copy file

dbutils.fs.cp(\
"/source/file.csv",\
"/target/file.csv")

------------------------------------------------------------------------

**Think of dbutils.fs as**

Windows File Explorer

or

Linux terminal

ls\
cp\
mv\
rm\
mkdir

inside Databricks.

------------------------------------------------------------------------

**YouTube**

- <https://www.youtube.com/watch?v=zMUiDYgqlq0>

# [README](./../../../README.md)
