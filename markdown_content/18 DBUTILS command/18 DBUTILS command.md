# 18 DBUTILS command

**Databricks Utilities (DBUtils)**

This lesson introduces **Databricks Utilities (DBUtils)**, a collection of built-in helper functions that simplify working with files, object storage, notebook parameters, secrets, and notebook execution. DBUtils is widely used in Databricks notebooks for automation and workflow development.

**Key Topics Covered**

**1. What is DBUtils?**

**DBUtils (Databricks Utilities)** is a built-in utility library available in Databricks notebooks.

It helps users:

- Manage files

- Work with cloud storage

- Create notebook parameters

- Access secrets securely

- Execute notebooks from other notebooks

DBUtils is supported only in:

- Python

- Scala

- R

It is **not available directly in SQL notebooks**, although SQL notebooks can work with widgets created in Python.

**2. Viewing Available Utilities**

To see all available DBUtils modules:

dbutils.help()

This lists utility groups such as:

- fs

- widgets

- secrets

- notebook

Some utilities are marked **experimental** and are generally not recommended for production workloads.

**DBUtils File System (FS)**

The **fs** module is one of the most frequently used DBUtils utilities.

It simplifies file management across:

- DBFS

- Azure Data Lake Storage (ADLS)

- Amazon S3

- Local file system

**3. Viewing FS Commands**

To list available file system commands:

dbutils.fs.help()

Common commands include:

- ls

- cp

- mkdirs

- head

- Mount-related commands

**4. Listing Files**

To list directory contents:

dbutils.fs.ls(path)

If no path is provided, DBUtils lists files in the default **DBFS** location.

Supported storage systems include:

- DBFS

- Local files (file:/)

- ADLS (abfss://)

- Amazon S3 (s3://)

**5. Displaying Results**

Wrapping the command with:

display(...)

renders the output in a formatted table, making file exploration easier.

**6. Reading File Contents**

To preview a file:

dbutils.fs.head(path)

This displays the beginning of the file without opening the entire dataset.

It is useful for quickly validating:

- CSV files

- JSON files

- Text files

**7. Creating Directories**

To create folders:

dbutils.fs.mkdirs(path)

The lesson demonstrates creating nested directories inside a Unity Catalog volume.

**8. Copying Files**

Files can be copied using:

dbutils.fs.cp(source, destination)

Examples include copying files:

- Local → Volume

- Volume → Local

- DBFS → ADLS

- ADLS → DBFS

- Between supported storage systems

This command is frequently used in data ingestion pipelines.

**Working with Volumes**

The lesson demonstrates managing Unity Catalog volumes using DBUtils.

Example path:

/Volumes/dev/bronze/managed_volume/

DBUtils can:

- Create folders

- Copy files

- List contents

- Read files

inside managed and external volumes.

**Widgets**

**9. What are Widgets?**

Widgets allow notebooks to accept **runtime input parameters**.

Instead of hardcoding values, users can provide values interactively.

Typical uses include:

- Customer IDs

- Dates

- Environment names

- File paths

Widgets make notebooks reusable.

**10. Viewing Widget Commands**

To list widget utilities:

dbutils.widgets.help()

Available widget types include:

- Text

- Dropdown

- Combobox

**11. Creating a Text Widget**

Example:

dbutils.widgets.text(...)

A text input box appears at the top of the notebook.

The widget specifies:

- Widget name

- Default value

- Display label

**12. Reading Widget Values**

To retrieve the value:

dbutils.widgets.get(...)

Whenever the widget value changes, dependent notebook cells automatically use the updated parameter.

**13. Using Widgets in Python**

Widget values can be assigned to variables:

value = dbutils.widgets.get(...)

These variables can then be used throughout Python code.

**14. Using Widgets in SQL**

Widgets also work inside SQL.

For Databricks Runtime **15.1 and earlier**:

\${widget_name}

For **later runtimes**:

:widget_name

This allows SQL notebooks to execute parameterized queries.

**Secrets**

**15. DBUtils Secrets**

The lesson briefly introduces:

dbutils.secrets.help()

Secrets provide secure access to:

- Passwords

- API Keys

- Connection strings

- Authentication tokens

Secrets are stored in **Secret Scopes**, which may be backed by:

- Databricks Secret Scopes

- Azure Key Vault

The instructor notes that secrets will be covered in detail later in the course.

**Notebook Utilities**

**16. Notebook Commands**

DBUtils also provides notebook utilities.

Listing commands:

dbutils.notebook.help()

Key operations include:

**Run another notebook**

dbutils.notebook.run(...)

This enables one notebook to execute another notebook as part of a workflow.

**Return values**

dbutils.notebook.exit(...)

Allows notebooks to return status values or results to the calling notebook.

These commands are commonly used when building multi-step workflows.

**Major DBUtils Modules**

| **Module**       | **Purpose**                         |
|------------------|-------------------------------------|
| dbutils.fs       | File and storage operations         |
| dbutils.widgets  | Notebook parameters                 |
| dbutils.secrets  | Secure credential access            |
| dbutils.notebook | Execute notebooks and return values |

**Common FS Commands**

| **Command** | **Purpose**             |
|-------------|-------------------------|
| ls()        | List directory contents |
| head()      | Preview file contents   |
| cp()        | Copy files              |
| mkdirs()    | Create directories      |

**Key Takeaways**

- **DBUtils** is a built-in Databricks utility library available in **Python**, **Scala**, and **R** notebooks.

- The **dbutils.fs** module simplifies working with local storage, DBFS, cloud storage, and Unity Catalog volumes through commands such as ls, head, cp, and mkdirs.

- **Widgets** enable notebook parameterization, allowing notebooks to accept runtime inputs and making them reusable for different execution scenarios.

- Widget values can be accessed in both **Python** and **SQL**, with syntax varying slightly depending on the Databricks Runtime version.

- **Secrets** provide a secure mechanism for accessing sensitive information, such as passwords and API keys, without hardcoding credentials in notebooks.

- **Notebook utilities** allow notebooks to call other notebooks (dbutils.notebook.run) and return execution results (dbutils.notebook.exit), supporting modular notebook development and workflow orchestration.

- The built-in help() methods make DBUtils easy to explore and are a valuable reference when learning new utility functions.

# [README](./../../../README.md)
