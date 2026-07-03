# ANSWER 17 10

**Question 10**

**What happens when an External Volume is dropped?**

**A. Both metadata and files are permanently deleted.** ❌ Incorrect

- External Volumes never delete customer-owned files.

**B. Only the metadata is removed, while the files remain in external storage.** ✅ Correct

Example:

ADLS\
\
Images\
\
Videos\
\
PDFs

Drop Volume:

DROP VOLUME media;

Result:

Metadata:

❌ Removed

Files:

✅ Still exist

The files remain because the storage belongs to the customer.

**C. The files are moved into a Managed Volume.** ❌ Incorrect

- Unity Catalog never moves customer files automatically.

**D. Unity Catalog automatically recreates the volume.** ❌ Incorrect

- Recreation must be done manually.

**E. The storage credential is deleted along with the volume.** ❌ Incorrect

- Storage Credentials are independent objects and remain available.

------------------------------------------------------------------------

**Memory Trick**

Managed Volume

↓

Drop

↓

Files deleted

External Volume

↓

Drop

↓

Files stay

------------------------------------------------------------------------

**Summary Table**

| **Concept** | **Remember This** |
|----|----|
| Purpose of Volumes | Governed storage for structured, semi-structured, and unstructured files |
| Prerequisites | **Unity Catalog enabled + Databricks Runtime 13.3 LTS or later** |
| Location in hierarchy | **Metastore → Catalog → Schema → Volume** (alongside tables, views, and functions) |
| Managed Volume | Unity Catalog automatically manages the storage location |
| Create folders | dbutils.fs.mkdirs() |
| Copy files | dbutils.fs.cp() |
| Volume path format | /Volumes/catalog/schema/volume/path/file |
| External Volume requirement | A LOCATION pointing to external cloud storage |
| Drop Managed Volume | Deletes both metadata and the stored files |
| Drop External Volume | Deletes only the metadata; files remain in the external storage location |

# [README](./../../../README.md)
