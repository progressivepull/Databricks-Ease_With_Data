# EXPLANATION 17 6

**Question 6**

**Which DBUtils command is used to copy files into a Unity Catalog volume?**

**Correct Answer:**\
✅ **dbutils.fs.cp()**

**Explanation**

Example:

dbutils.fs.cp(\
"/tmp/report.csv",\
"/Volumes/main/files/report.csv"\
)

The command copies:

Source File\
\
↓\
\
Destination Volume

Useful for:

- Uploading files

- ETL

- Data ingestion

- Moving test data

**YouTube**

**DBUtils File Copy**

https://www.youtube.com/results?search_query=DBUtils+fs+cp

# [README](./../../../README.md)
