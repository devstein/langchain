<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `sql_database` directory is for interacting with a SQL database and checking the correctness of SQL queries. It contains tools for querying a SQL database, checking the correctness of SQL queries, and providing a checklist for common mistakes to avoid when writing SQL queries.

### Files
#### prompt.py
This file contains a constant string `QUERY_CHECKER` that provides a checklist for common mistakes to avoid when writing SQL queries for the specified dialect.

#### tool.py
This file contains the implementation of classes for interacting with a SQL database and checking the correctness of SQL queries. The `BaseSQLDatabaseTool` class is a base tool for interacting with a SQL database, while the `QuerySQLDataBaseTool` class is a tool for querying a SQL database. The `QueryCheckerTool` class is a tool used to check if a SQL query is correct before executing it, using an LLM chain to predict the correctness of the query.

<!--- END SELFDOC --->