<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `tools` directory is for providing a collection of tools for various tasks such as file management, web scraping, API operations, querying, and searching from different sources. It includes subdirectories for specific tools such as interacting with APIs, managing files and directories, and interacting with a web browser. Additionally, it contains tools for interacting with databases, generating images from text prompts, and running shell commands.

### Files
#### __init__.py
This file serves as the core toolkit implementation and initialization file for the `langchain/tools` directory, providing various tools for file management, web scraping, API operations, querying, and searching from sources such as Wikipedia, Wolfram Alpha, and YouTube.

#### base.py
This file contains a base class for LangChain tools, including methods for parsing tool input and running the tool. It also includes functions and decorators for creating tools from functions, as well as a Pydantic model for input validation and callbacks.

#### ifttt.py
This file contains the implementation of `IFTTTWebhook`, a tool for connecting to IFTTT services through webhooks. It includes instructions for creating and configuring a webhook, and provides a `BaseTool` class for managing callbacks. The tool sends a JSON event to a specified URL synchronously using the `requests` library.

#### plugin.py
This file defines the `AIPlugin` and `AIPluginTool` classes, which provide a standardized interface for running AI plugins with input validation and callback management. It also includes a method for generating the OpenAPI specification for a given plugin URL.

### Directories
#### arxiv
The `arxiv` directory is for a toolkit that provides a wrapper around the Arxiv API. It includes the `ArxivQueryRun` class, which adds the capability to search using the Arxiv API, and methods for running the tool synchronously and asynchronously.

#### bing_search
The `bing_search` directory is for interacting with the Bing Search API through the `BingSearchRun` and `BingSearchResults` classes, which are implemented in the `tool.py` file and exported in the `__init__.py` file.

#### ddg_search
The `ddg_search` directory is for querying the DuckDuckGo search API using the `DuckDuckGoSearchRun` class from the `tool` module. It also contains tools for processing the search results.

#### file_management
The `file_management` directory is for managing files and directories in a specified folder. It includes tools for copying, deleting, searching, listing, moving, reading, and writing files. The directory also contains a mixin class for file system tools and a function for validating relative paths.

#### gmail
The `gmail` directory is for Gmail tools used to create, search, and retrieve email messages and threads. It includes files for initializing the directory, defining a base class for Gmail tools, creating a draft email, fetching an email by message ID, searching for email messages or threads, and utility functions for working with the Gmail API.

#### google_places
The `google_places` directory is for adding the capability to query the Google Places API through the implementation of the `GooglePlacesTool` class in `tool.py`. It also includes an `__init__.py` file for convenient importing of the `GooglePlacesTool` class.

#### google_search
The `google_search` directory is for tools related to querying the Google Search API. It contains the `__init__.py` initialization file and the `tool.py` file, which includes the `GoogleSearchResults` and `GoogleSearchRun` classes for returning query results.

#### google_serper
The `google_serper` directory is for a package that provides a toolkit for the Serer.dev Google Search API. It includes an implementation of a tool called `GoogleSerperRun` that allows the user to query the API and returns a string of the query results.

#### graphql
The `graphql` directory is for tools that enable interaction with a GraphQL API. It contains a `tool.py` file that implements the `BaseGraphQLTool` class, which provides a base tool for querying a GraphQL API.

#### human
The `human` directory is for a tool that allows users to request human input through a prompt. The tool is implemented in `tool.py` and exports the `HumanInputRun` class through `__init__.py`. The tool provides a default print and input function, which can be customized. It does not support asynchronous operations.

#### interaction
The `interaction` directory is for providing tools for interacting with the user through the command line. It includes a tool for asking the user for input and a recommended function for interacting with the user.

#### jira
The `jira` directory is for interacting with the Atlassian Jira API through command-line tools and a `JiraAction` class that allows agents to perform operations on a Jira instance. It contains prompts for creating a Jira issue, fetching projects, and searching for issues using JQL query strings.

#### json
The `json` directory is for interacting with and manipulating JSON specs. It contains a `tool.py` file with classes and methods for parsing and manipulating JSON specs, including getting values and listing keys at a given path, creating a `JsonSpec` object from a file, and running the tools asynchronously or synchronously.

#### metaphor_search
The `metaphor_search` directory is for a tool called `MetaphorSearchResults` which is a wrapper around the Metaphor Search API. It can be used to query the API and get back JSON results. The tool can be run synchronously or asynchronously.

#### openapi
The `openapi` directory is for working with OpenAPI specifications. It includes utility functions and Pydantic models for parsing and retrieving information from OpenAPI files.

#### openweathermap
The `openweathermap` directory is for a toolkit that provides a tool for querying the OpenWeatherMap API. It includes an initializer file and a tool file that allows fetching current weather information for a specified location synchronously or asynchronously.

#### playwright
The `playwright` directory is for interacting with a web browser using Playwright. It includes tools for navigation, element extraction, clicking, and scraping hyperlinks and text from web pages. The directory contains several classes and functions, including a `BaseBrowserTool` class that serves as a base class for browser tools, and input schemas for each tool. The directory also includes a `utils.py` file with utility functions for the Playwright browser tools.

#### powerbi
The `powerbi` directory is for tools that interact with a PowerBI dataset. It includes files for writing DAX queries and a tool for querying a Power BI dataset by taking a detailed question as input and outputting a result.

#### python
The `python` directory is for implementing a Python REPL tool with input validation and sanitization, as well as default dictionaries for global and local variables. It includes two classes, `PythonREPLTool` and `PythonAstREPLTool`, which inherit from `BaseTool`. The former runs Python code synchronously, while the latter is not yet implemented.

#### requests
The `requests` directory is for providing tools for making HTTP requests to an API endpoint using the `requests` library. It includes a variety of tools for making different types of requests, such as GET, POST, PATCH, PUT, and DELETE, with both synchronous and asynchronous methods available.

#### scenexplain
The `scenexplain` directory is for a SceneXplain API toolkit that provides a tool for explaining images. It includes the `__init__.py` file with a brief description of the toolkit and the `tool.py` file that defines the `SceneXplainTool` class, which generates a detailed caption for an image using the `SceneXplainAPIWrapper`.

#### searx_search
The `searx_search` directory is for implementing tools to query a Searx instance and return the results in a JSON array format. The `tool.py` file includes the `SearxSearchRun` and `SearxSearchResults` tools, which use the `SearxSearchWrapper` to perform the search. It also contains an async function `_arun` that takes a query and an optional callback manager as input and returns a string.

#### shell
The `shell` directory is for a tool that allows running shell commands with synchronous and asynchronous options. It includes an `__init__.py` file that exports the `ShellTool` class from the `tool.py` file.

#### spark_sql
The `spark_sql` directory is for providing tools for interacting with Spark SQL databases. It contains files such as `__init__.py` for module initialization, `prompt.py` for a prompt to double check queries, and `tool.py` for multiple tools to query, retrieve metadata, and check the correctness of Spark SQL queries.

#### sql_database
The `sql_database` directory is for interacting with a SQL database and checking the correctness of SQL queries. It contains tools for querying a SQL database, checking the correctness of SQL queries, and providing a checklist for common mistakes to avoid when writing SQL queries.

#### steamship_image_generation
The `steamship_image_generation` directory is for generating images from a text-prompt using Steamship. It contains the `__init__.py` initialization file, the `tool.py` file with the `SteamshipImageGenerationTool` class, and the `utils.py` file with the `make_image_public` function.

#### vectorstore
The `vectorstore` directory is for tools related to interacting with vectorstores, including a base class and a `VectorStoreQATool` class for the VectorDBQA chain. It also includes the `VectorStoreQAWithSourcesTool` class for answering questions about a topic and its sources, with synchronous and asynchronous methods available.

#### wikipedia
The `wikipedia` directory is for a toolkit that provides a wrapper around the Wikipedia API. It includes an initialization file and a tool file that allows for searching for general information about various subjects.

#### wolfram_alpha
The `wolfram_alpha` directory is for a toolkit that provides a wrapper around the Wolfram Alpha API. It includes an initialization file and a tool module that allows for querying various topics and returning results obtained from the API.

#### youtube
The `youtube` directory is for searching YouTube videos related to a person and returning a specified number of video URLs. It contains the `search.py` file, which includes the `YouTubeSearchTool` class that utilizes the `youtube_search` library to perform the search.

#### zapier
The `zapier` directory is for tools related to using the Zapier Natural Language Actions API. It includes the `__init__.py` file for importing the `ZapierNLAListActions` and `ZapierNLARunAction` classes, the `prompt.py` file for providing a prompt for user input, and the `tool.py` file for executing specific actions and returning a list of exposed actions.

<!--- END SELFDOC --->