<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `sql_database` directory is for interacting with SQL databases using a language model. It includes the `SQLDatabaseChain` class for executing SQL queries with various configuration options, the `SQLDatabaseSequentialChain` class for sequential querying, and prompt templates for constructing SQL queries and selecting relevant tables.

### Files
#### __init__.py
This file contains a brief module-level docstring for the `langchain/chains/sql_database` directory, indicating that it is a chain for interacting with SQL databases.

#### base.py
This file defines the `SQLDatabaseChain` class, which provides a way to execute SQL queries on a database using a language model. It includes various configuration options and can be instantiated with an OpenAI model and a SQL database. Additionally, the file contains the `SQLDatabaseSequentialChain` class, which is a chain for querying SQL databases in a sequential manner, and a base class for SQL databases with methods for returning input and output keys.

#### prompt.py
This file contains various prompt templates for constructing SQL queries and selecting relevant tables to answer input questions. The templates provide guidelines for creating syntactically correct queries, specifying the number of results to query for, the columns to select, and the tables to use. The file also includes a dictionary of SQL prompts for different SQL databases.

<!--- END SELFDOC --->