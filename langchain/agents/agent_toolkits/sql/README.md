<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `sql` directory is for implementing a SQL agent toolkit that can execute SQL queries and interact with a SQL database. It includes files for constructing a SQL agent from a BaseLanguageModel and SQLDatabaseToolkit, defining SQL prefix and suffix instructions, and providing a toolkit for interacting with a SQL database.

### Files
#### prompt.py
This file contains the SQL_PREFIX and SQL_SUFFIX strings, which provide instructions and guidelines for an agent designed to interact with a SQL database. The SQL_PREFIX string outlines the rules and limitations for constructing queries, while the SQL_SUFFIX string provides a prompt for the agent to begin answering a given question.

#### toolkit.py
This file contains the `SQLDatabaseToolkit` class, which is a toolkit for interacting with a SQL database. It includes a `get_tools` method that returns a list of tools for querying and checking the database.

<!--- END SELFDOC --->