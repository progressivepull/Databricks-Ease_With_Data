# 17 Volumes - Managed & External in Databricks

**Volumes – Managed and External in Databricks**

This lesson introduces **Volumes** in Unity Catalog, which provide governed storage for **structured**, **semi-structured**, and **unstructured** files. It explains the differences between **Managed Volumes** and **External Volumes**, demonstrates how to create and use them, and shows how they integrate with Unity Catalog security and governance.

**Key Topics Covered**

**1. What Are Volumes?**

Until now, the course has focused on storing **tabular data** using Delta tables.

Volumes extend Unity Catalog by allowing organizations to store:

- Structured files

- Semi-structured files

- Unstructured files

Examples include:

- CSV files

- JSON files

- Images

- PDFs

- Documents

- Machine Learning datasets

Unlike Delta tables, volumes store files directly rather than relational table data.

**2. Requirements for Using Volumes**

To use Volumes, the following are required:

- **Unity Catalog enabled**

- **Databricks Runtime 13.3 LTS or later**

Volumes are fully governed by Unity Catalog permissions.

**3. Position in the Unity Catalog Hierarchy**

Volumes are siblings of tables within the Unity Catalog object model.

Metastore\
│\
Catalog\
│\
Schema\
├─────────────┐\
│ │\
Tables Volumes

Because volumes exist inside a catalog and schema, Unity Catalog can manage access permissions for their files.

**Managed Volumes**

**4. Creating a Managed Volume**

A managed volume is created using:

CREATE VOLUME dev.bronze.managed_volume;

Characteristics:

- No storage location specified

- Unity Catalog determines storage automatically

- Storage follows the managed location hierarchy:

Schema → Catalog → Metastore

**5. Viewing Volume Metadata**

Using:

DESCRIBE VOLUME

the lesson displays:

- Catalog

- Schema

- Owner

- Storage location

- Volume type

The managed volume is stored in Unity Catalog's managed storage location.

**Working with Files**

**6. Downloading a Sample File**

The lesson downloads an employee CSV file using Linux shell commands:

wget

The downloaded file is later copied into the volume.

**7. Using DBUtils**

The instructor demonstrates **DBUtils**, a Databricks utility library used for file operations.

Examples include:

- Creating folders

- Copying files

- Listing files

- Managing file systems

DBUtils will be covered in more detail later in the course.

**8. Creating Directories**

Using:

dbutils.fs.mkdirs()

a folder is created inside the managed volume.

Volumes are referenced using the path format:

/Volumes/catalog/schema/volume/

Example:

/Volumes/dev/bronze/managed_volume/files

**9. Copying Files**

The CSV file is copied into the managed volume using:

dbutils.fs.cp()

This copies the file from the local notebook environment into Unity Catalog storage.

**10. Reading Files from a Volume**

Files stored in a volume can be queried directly.

Example:

SELECT \*\
FROM csv.\`/Volumes/...\`

The lesson successfully reads the CSV stored inside the managed volume.

**External Volumes**

**11. Creating External Storage**

Before creating an external volume, the instructor creates:

- Azure Storage directory

- External Location

- Storage Credential

These were introduced in earlier Unity Catalog lessons.

**12. Creating an External Volume**

An external volume is created using:

CREATE EXTERNAL VOLUME

Unlike managed volumes, an external volume requires:

LOCATION '\<external path\>'

The data remains in customer-managed Azure Data Lake Storage.

**13. Working with External Volumes**

The same operations are demonstrated:

- Create folders

- Copy files

- Read files

The CSV file appears both:

- Inside Databricks Catalog Explorer

- Inside Azure Storage

This confirms that the external volume references customer-managed storage.

**Reading Files**

Both managed and external volumes are accessed using:

/Volumes/catalog/schema/volume/path/file

The same syntax works regardless of where the files are physically stored.

**Dropping Volumes**

**14. Managed Volume Behavior**

When executing:

DROP VOLUME managed_volume;

Databricks removes:

- Volume metadata

- Stored files

The managed volume and its contents are permanently deleted.

**15. External Volume Behavior**

When executing:

DROP VOLUME external_volume;

Databricks removes:

- Volume metadata

However:

- Files remain in Azure Storage.

Recreating the volume immediately restores access to the existing files.

**Managed vs. External Volumes**

| **Feature**                         | **Managed Volume** | **External Volume** |
|-------------------------------------|--------------------|---------------------|
| Metadata managed by Unity Catalog   | ✔                  | ✔                   |
| Files managed by Unity Catalog      | ✔                  | ✘                   |
| User specifies storage location     | ✘                  | ✔                   |
| Data deleted when volume is dropped | ✔                  | ✘                   |
| Files remain after DROP             | ✘                  | ✔                   |

**Volume Path Format**

Volumes use the following standard path:

/Volumes/\
catalog/\
schema/\
volume/\
folders/\
files

Example:

/Volumes/dev/bronze/managed_volume/files/emp.csv

**Key Takeaways**

- **Volumes** provide Unity Catalog–governed storage for **structured**, **semi-structured**, and **unstructured** files, complementing Delta tables for non-tabular data.

- Volumes require **Unity Catalog** and **Databricks Runtime 13.3 LTS or later**.

- **Managed Volumes** store files in Unity Catalog's managed storage based on the schema, catalog, or metastore managed location.

- **External Volumes** reference files stored in customer-managed cloud storage through **Storage Credentials** and **External Locations**.

- **DBUtils** provides convenient file system operations such as creating directories (mkdirs) and copying files (cp) within volumes.

- Files in both managed and external volumes are accessed using the standardized /Volumes/catalog/schema/volume/... path.

- Dropping a **Managed Volume** deletes both its metadata and stored files, whereas dropping an **External Volume** removes only the metadata, leaving the files intact in external storage and allowing the volume to be recreated later.

# [README](./../../../README.md)
