# 47 AIBI Genie Space in Databricks

**AI/BI Genie Spaces in Databricks**

This lesson introduces **AI/BI Genie Spaces**, an AI-powered feature in Databricks that allows business users to interact with data using **natural language** instead of writing SQL queries. Genie uses metadata, AI, and SQL generation to make data exploration simple and accessible.

**What is AI/BI Genie?**

- Genie Space is an AI-powered conversational interface for querying data.

- Users ask questions in plain English (natural language).

- Genie automatically:

  - Understands the question.

  - Generates SQL behind the scenes.

  - Executes the SQL on a SQL Warehouse.

  - Returns results with tables and visualizations.

- No SQL knowledge is required for business users.

**Creating a Genie Space**

There are two ways to use Genie:

**1. Enable Genie on an existing AI/BI Dashboard**

- Open an AI/BI Dashboard.

- Select **Edit Draft**.

- Click **Publish**.

- Enable the **Genie** toggle.

- Users can now ask questions directly from the dashboard.

The Genie queries use the same SQL Warehouse configured for the dashboard.

**2. Create a New Genie Space**

Navigate to:

**New → Genie Space**

or

**SQL → Genie**

Then:

1.  Click **New**

2.  Select one or more datasets

3.  Click **Create**

Example datasets:

- Orders

- Customers

These become the knowledge source for Genie.

**How Genie Understands Your Data**

Genie relies heavily on metadata.

It uses:

- Table descriptions

- Column comments

- Dataset names

- Relationships

- Sample values (optional)

This information helps AI understand what users mean.

Example:

Instead of seeing

status = O

Genie can understand

Open Orders

because of the metadata descriptions.

**Configuring a Genie Space**

The Configure page contains several important sections.

**1. Settings**

Here you configure:

- Genie Space name

- SQL Warehouse

Example:

Sales Genie Space

Important:

Genie only supports:

- SQL Warehouse Pro

- SQL Warehouse Serverless

Classic SQL Warehouses are **not supported**.

**2. Dataset Configuration**

Each dataset can be customized.

You can:

- Edit descriptions

- Improve AI understanding

- Override Unity Catalog comments

Example:

Order Status\
\
P = Pending\
F = Fulfilled\
O = Open

Now users can ask:

How many open orders?

Genie knows:

Open = O

without users needing to know database codes.

**3. Example Values**

Genie can sample data values to improve AI responses.

Example:

Customer Name\
State\
Region\
Status

These sample values help AI interpret user questions more accurately.

If sensitive data should not be shared:

Advanced → Disable **Example Values**

This prevents sample data from being sent to the AI assistant while still allowing metadata usage.

**4. Instructions**

You can provide custom instructions that teach Genie organization-specific terminology.

Example:

MK = Customer Market Segment

Now users can ask:

Average order size by MK

instead of typing:

Average order size by Customer Market Segment

This allows Genie to understand abbreviations, business terms, and internal language.

**5. SQL Examples**

You can add example SQL queries.

Benefits:

- Improves AI understanding

- Produces better SQL

- Makes responses more accurate over time

These examples act as guidance for the AI model.

**Asking Questions in Natural Language**

Example prompts include:

How many open orders?

Genie:

- Generates SQL

- Counts records

- Returns the answer

Example:

SELECT COUNT(\*)\
FROM orders\
WHERE status='O'

Users never need to see the SQL unless they choose to.

**Viewing Generated SQL**

Every response includes a **Show Code** option.

This allows users to inspect:

- Generated SQL

- Filters

- Aggregations

- Joins

Useful for:

- Validation

- Learning SQL

- Troubleshooting

The generated SQL can be reviewed before trusting results.

**Example Queries**

**Simple Count**

How many fulfilled orders?

Genie performs:

COUNT(\*)\
WHERE status='F'

**Average**

What is the average order size?

Genie automatically uses:

AVG(order_size)

**Join Multiple Tables**

Average order size by customer market segment

Genie:

- Joins Orders

- Joins Customers

- Groups by Market Segment

- Calculates Average

without requiring users to write any SQL.

**Complex Analytics**

Example:

Year over Year Growth by Market Segment

Genie generates a much more complex SQL query involving:

- Window functions

- Date calculations

- Aggregations

- Grouping

It also creates a visualization automatically.

**Automatic Visualizations**

Genie doesn't only return tables.

It also creates:

- Bar charts

- Pie charts

- Trend charts

- Other visualizations

Users can edit the generated visualization if needed, making exploration more interactive.

**AI Feedback**

After reviewing a response, users can provide feedback.

Example:

Was this answer correct?

Selecting **Yes** helps Genie learn and improve future responses.

**Monitoring**

The Monitoring tab records:

- Questions asked

- Generated SQL

- Users

- Query history

Administrators can understand how Genie is being used and monitor natural language queries across the organization.

**Sharing a Genie Space**

A Genie Space can be shared with:

- Individual users

- User groups

Example:

Business User Group

Permission:

Can Run

This allows business users to access and use the Genie Space without modifying it.

**Required Permissions**

Sharing the Genie Space alone is **not enough**.

Business users also need:

**Dataset Permissions**

- USE CATALOG

- USE SCHEMA

- SELECT

on every dataset used by Genie.

**SQL Warehouse Permissions**

Users must also have:

Can Use

permission on the SQL Warehouse.

Without these permissions, Genie displays an access error.

**Business User Experience**

Once permissions are granted, business users can ask questions such as:

Total pending order sales amount

or

Order status distribution

Genie:

- Generates SQL automatically

- Retrieves the data

- Creates charts

- Returns answers in seconds

This enables self-service analytics without waiting for analysts to build reports.

**Key Takeaways**

- **AI/BI Genie** enables natural language querying of Databricks data.

- Genie uses **metadata** (table descriptions, column comments) to understand business context.

- Dataset descriptions can be customized without changing Unity Catalog metadata.

- **Example values** improve AI accuracy but can be disabled for privacy.

- Custom instructions let Genie understand organization-specific terminology and abbreviations.

- Example SQL queries help Genie generate more accurate SQL.

- Genie automatically generates SQL, executes it, and displays both results and visualizations.

- Users can inspect generated SQL using **Show Code**.

- The **Monitoring** tab tracks usage, prompts, and generated queries.

- Sharing requires both **Genie Space permissions** and access to the underlying datasets and SQL Warehouse.

- Genie empowers business users with self-service analytics by allowing them to query data using everyday language rather than SQL.

# [README](./../../../README.md)
