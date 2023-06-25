<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `agent_toolkits` directory is for providing a collection of toolkits for different agents, including CSV, file management, Gmail, Jira, JSON, NLA, OpenAPI, Pandas, PlayWright browser automation, PowerBI, Python, Spark, Spark SQL, SQL database, VectorStore, and Zapier. Each subdirectory contains files for initializing the toolkit, creating an agent, providing prompts and instructions, and defining the tools in the toolkit.

### Files
#### __init__.py
This file imports various toolkits for different services such as Gmail, Jira, and SQL, and provides functions to create agents for these services.

### Directories
#### csv
The `csv` directory is for implementing a CSV toolkit that includes a `base.py` file containing a function to create a CSV agent by loading the CSV file into a Pandas dataframe and using a Pandas agent, and an `__init__.py` file with a brief description of the CSV toolkit.

#### file_management
The `file_management` directory is for providing a set of tools for interacting with the local filesystem. The `toolkit.py` file contains the `FileManagementToolkit` class, which offers a range of tools for copying, deleting, searching, moving, reading, and writing files, relative to a specified root directory. The `__init__.py` file imports the `FileManagementToolkit` class from `toolkit.py` and makes it available for use.

#### gmail
The `gmail` directory is for a toolkit that provides functionality for interacting with Gmail. It includes a `__init__.py` initialization file and a `toolkit.py` file that defines the `GmailToolkit` class and its associated tools.

#### jira
The `jira` directory is for a Jira Toolkit that extends the `BaseToolkit` class. It contains an initialization file and a `toolkit.py` file that defines a `JiraToolkit` class with methods to create an instance and get the tools in the toolkit.

#### json
The `json` directory is for creating and interacting with a JSON agent toolkit. It includes files for initializing the toolkit, creating a JSON agent, defining prompts for interacting with JSON, and implementing a `JsonToolkit` class for interacting with a JSON spec.

#### nla
The `nla` directory is for implementing natural language interaction with APIs through the `NLATool` and `NLAToolkit` classes in `tool.py` and `toolkit.py`, respectively. These classes provide tools for creating instances of the toolkit and interacting with APIs using natural language.

#### openapi
The `openapi` directory is for creating agents that interact with OpenAPI APIs through a hierarchical planning approach. It includes files for defining an OpenAPI spec agent, making HTTP requests, parsing responses, orchestrating API requests, and creating prompt templates for planning a sequence of API calls. Additionally, it contains functions for simplifying and substituting references in an OpenAPI specification.

#### pandas
The `pandas` directory is for creating and using a Pandas toolkit in the langchain/agents/agent_toolkits directory. It includes an entry point file, a base file with a function to construct a pandas agent, and a prompt file with a string prompt for users to answer questions about a pandas dataframe.

#### playwright
The `playwright` directory is for a browser automation toolkit called Playwright. It includes an initialization file and a `toolkit.py` file that defines the `PlayWrightBrowserToolkit` class with various tools for web browser automation.

#### powerbi
The `powerbi` directory is for constructing Power BI agents and toolkits that interact with a Power BI dataset. It includes files for initializing the agent toolkit, creating a Power BI agent, constructing a conversational chat agent, providing prompts and instructions for the agent, and a toolkit for interacting with the dataset.

#### python
The `python` directory is for implementing a Python agent that can be constructed from a BaseLanguageModel and a PythonREPLTool. It contains the implementation of the ZeroShotAgent class, the LLMChain class, and the AgentExecutor class used to execute the agent. Additionally, the directory contains a function `create_python_agent` that constructs the agent. The `prompt.py` file in the directory contains a constant variable `PREFIX` which provides instructions for an agent designed to write and execute Python code to answer questions.

#### spark
The `spark` directory is for creating and working with Spark agents in the Langchain application. It contains an entry point file, a base file for creating Spark agents, and a prompt file for prompting users with instructions and questions when working with a Spark dataframe.

#### spark_sql
The `spark_sql` directory is for implementing the Spark SQL agent toolkit, which includes the `AgentExecutor` abstract class implementation, the `SparkSQLToolkit` class for interacting with Spark SQL, and the SQL_PREFIX and SQL_SUFFIX strings used in the toolkit.

#### sql
The `sql` directory is for implementing a SQL agent toolkit that can execute SQL queries and interact with a SQL database. It includes files for constructing a SQL agent from a BaseLanguageModel and SQLDatabaseToolkit, defining SQL prefix and suffix instructions, and providing a toolkit for interacting with a SQL database.

#### vectorstore
The `vectorstore` directory is for interacting with and querying vector stores. It contains modules for creating VectorStore agents, routing between vector stores, and providing tools for interacting with vector stores.

#### zapier
The `zapier` directory is for the Zapier Toolkit, which contains the `ZapierToolkit` class and its methods for creating a toolkit from a `ZapierNLAWrapper` and returning the tools in the toolkit. It also contains an initialization file.

<!--- END SELFDOC --->