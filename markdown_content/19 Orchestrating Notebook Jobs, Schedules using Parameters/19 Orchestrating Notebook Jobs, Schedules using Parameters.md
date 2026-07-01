# 19 Orchestrating Notebook Jobs, Schedules using Parameters

**Orchestrating Notebook Jobs, Schedules, and Parameters in Databricks**

This lesson demonstrates how to **parameterize Databricks notebooks using DBUtils widgets**, execute one notebook from another using **dbutils.notebook.run()**, pass parameters between notebooks, return values to the calling notebook, and schedule notebooks as recurring jobs. These techniques form the foundation of Databricks **workflows and job orchestration**.

**Key Topics Covered**

**1. Notebook Orchestration**

The lesson introduces a simple workflow consisting of two notebooks:

**Child Notebook**

Write Employee Data

Responsibilities:

- Read employee data

- Accept a department parameter

- Filter records

- Write a Delta table

- Return the number of records written

**Parent Notebook**

Run Write Employee Data

Responsibilities:

- Pass parameters

- Execute the child notebook

- Receive the returned result

This parent-child architecture is commonly used in production ETL pipelines.

**2. Reading Input Data**

The child notebook first previews a CSV file using:

dbutils.fs.head(path)

It then loads the employee dataset with Spark:

spark.read.csv(...)

The dataset includes:

- Employee information

- Department

- Active Record flag

**3. Parameterizing the Child Notebook**

The child notebook creates a widget:

dbutils.widgets.text(...)

The widget accepts:

Department

Users—or another notebook—can provide this value at runtime.

**4. Reading Widget Values**

The widget value is retrieved using:

dbutils.widgets.get(...)

The department value is stored in a Python variable for later filtering.

**5. Filtering the Data**

The notebook filters records using:

- Department supplied through the widget

- Active Record = 1

The department comparison converts the input to uppercase to make filtering case-insensitive.

**6. Writing Dynamic Delta Tables**

After filtering:

The notebook counts the records.

If records exist:

- Writes a Delta table

- Uses **Overwrite** mode

The table name is built dynamically:

dev.branch.dept\_\<department\>

Examples:

dev.branch.dept_sales

dev.branch.dept_office

Each department therefore receives its own Delta table.

**7. Conditional Processing**

The notebook checks:

count \> 0

If data exists:

- Write table

- Display table

- Print success message

Otherwise:

- Print "No data"

This prevents empty tables from being created.

**8. Returning Values to the Parent Notebook**

The child notebook returns the record count using:

dbutils.notebook.exit(...)

The returned value becomes available to the notebook that invoked it.

**Parent Notebook**

**9. Running Another Notebook**

The parent notebook executes the child using:

dbutils.notebook.run(...)

The method requires:

- Notebook path

- Timeout

- Parameter dictionary

Example parameters:

Department = Sales

This launches the child notebook as a Databricks job.

**10. Passing Parameters**

Parameters are passed using a Python dictionary.

Example:

{\
"DEPT": "Sales"\
}

Multiple parameters can be supplied if needed.

**11. Job Execution**

While the child notebook runs:

Databricks displays:

- Notebook execution status

- Job details

- Cluster information

- Spark UI

- Logs

- Parameters used

- Execution duration

This provides visibility into notebook execution.

**12. Receiving Returned Values**

The parent notebook captures the exit value:

count = dbutils.notebook.run(...)

The returned record count can then be used for:

- Logging

- Conditional logic

- Triggering additional notebooks

- Notifications

The lesson demonstrates:

- Sales → 51 records

- Office → 200 records

**13. Dynamic Processing**

By simply changing the parameter:

Sales

to

Office

the same child notebook:

- Filters different data

- Creates a different Delta table

- Returns a different count

No code modifications are required.

**Scheduling Notebook Jobs**

**14. Creating Scheduled Jobs**

Databricks notebooks can be scheduled directly from the notebook interface.

Scheduling options include:

- Daily

- Weekly

- Custom intervals

Users choose:

- Existing cluster

- New job cluster

**15. Passing Parameters During Scheduling**

Scheduled jobs can also receive widget parameters.

Example:

Department = Sales

This allows the same notebook to execute automatically for different business scenarios.

**16. Notifications**

Job scheduling supports notifications for:

- Success

- Failure

- Job start

These notifications assist with monitoring production pipelines.

**17. Advanced Scheduling**

Advanced scheduling options include:

- Time Zone selection

- Cron expressions

Cron syntax enables highly customized execution schedules beyond simple daily or weekly intervals.

**Workflow Architecture**

Parent Notebook\
│\
▼\
dbutils.notebook.run()\
│\
▼\
Child Notebook\
│\
├── Read widget parameter\
├── Read CSV\
├── Filter data\
├── Write Delta table\
└── Return record count\
│\
▼\
Parent Notebook receives result

**Job Flow**

Scheduler\
│\
▼\
Parent Notebook\
│\
▼\
Child Notebook\
│\
▼\
Delta Table

**Key DBUtils Commands Used**

| **Command**             | **Purpose**                     |
|-------------------------|---------------------------------|
| dbutils.widgets.text()  | Create notebook input parameter |
| dbutils.widgets.get()   | Read parameter value            |
| dbutils.notebook.run()  | Execute another notebook        |
| dbutils.notebook.exit() | Return value to caller          |
| dbutils.fs.head()       | Preview input file              |

**Key Takeaways**

- **Notebook parameterization** using **DBUtils widgets** allows notebooks to accept dynamic runtime inputs, making them reusable for different scenarios.

- **Parent-child notebook orchestration** is achieved with dbutils.notebook.run(), enabling one notebook to execute another as part of a workflow while passing parameters through a dictionary.

- The child notebook can process data dynamically, such as filtering employee records by department, writing department-specific Delta tables, and returning results to the parent notebook with dbutils.notebook.exit().

- The parent notebook can capture returned values and use them for logging, decision-making, or triggering additional processing steps.

- Databricks automatically tracks notebook job execution, providing visibility into execution status, cluster details, logs, runtime, and parameters.

- Notebooks can be scheduled as recurring **Databricks Jobs**, with configurable frequencies, widget parameters, notifications, time zones, and **Cron expressions**, making them suitable for production workflow automation.

# [README](./../../../README.md)
