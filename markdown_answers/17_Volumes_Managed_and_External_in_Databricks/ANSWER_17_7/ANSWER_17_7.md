# ANSWER 17 7

**Question 7**

**What path format is used to access files stored in Unity Catalog volumes?**

**A. /dbfs/catalog/schema/file** ❌ Incorrect

- DBFS paths use /dbfs/.

- Unity Catalog Volumes use /Volumes/.

**B. /mnt/catalog/schema/volume/file** ❌ Incorrect

- /mnt refers to traditional mounts.

**C. /Volumes/catalog/schema/volume/path/file** ✅ Correct

Example:

/Volumes/main/files/images/logo.png

Breakdown:

Volumes\
↓\
Catalog\
↓\
Schema\
↓\
Volume\
↓\
Folders\
↓\
Files

**D. /storage/catalog/schema/file** ❌ Incorrect

- Invalid path.

**E. /unity/catalog/schema/file** ❌ Incorrect

- Invalid path.

------------------------------------------------------------------------

**Memory Trick**

Volumes always begin with:

/Volumes/

------------------------------------------------------------------------

# [README](./../../../README.md)
