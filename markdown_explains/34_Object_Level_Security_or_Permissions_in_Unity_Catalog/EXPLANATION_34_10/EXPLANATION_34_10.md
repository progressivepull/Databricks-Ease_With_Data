# EXPLANATION 34 10

**Question 10**

**Which approach is recommended for repeatable, automated permission management in Unity Catalog?**

**Correct Answer:** **C. Using SQL GRANT and REVOKE statements**

**Explanation**

The recommended approach for managing Unity Catalog permissions is to use SQL statements such as:

GRANT SELECT ON TABLE sales.orders TO \`analysts\`;

REVOKE SELECT ON TABLE sales.orders FROM \`temporary_user\`;

Using SQL makes permission management:

- Repeatable.

- Automatable.

- Easy to version-control.

- Suitable for CI/CD pipelines and Infrastructure as Code.

**Why the Correct Answer is Correct**

SQL GRANT and REVOKE statements provide a consistent, scriptable method for administering permissions across environments.

**Why the Other Answers Are Wrong**

The other options rely on manual configuration or approaches that are difficult to automate and maintain.

**YouTube Video**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**Direct YouTube Link**\
https://www.youtube.com/watch?v=PyT6S_0RkY0

**YouTube Search**\
https://www.youtube.com/results?search_query=Unity+Catalog+GRANT+REVOKE+permissions

# [README](./../../../README.md)
