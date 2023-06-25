<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `utilities` directory is for various utility classes and functions that provide wrappers and shims for various APIs and services, including Apify, Arxiv, AWS Lambda, Bing Search, DuckDuckGo Search, Google APIs, GraphQL, Wolfram Alpha, SerpAPI, Searx Search, Wikipedia, OpenWeatherMap, Python REPL, PowerBI, Spark SQL, and Metaphor Search. These utilities provide easy-to-use interfaces for conducting searches, fetching data, and interacting with APIs and services. Additionally, it contains a Python class and utility functions for interacting with the Zapier NLA API, including methods for validating the API key, creating a session with the API, listing exposed actions associated with the current user, executing an action, and previewing the parameters guessed by the AI before executing the action.

### Files
#### __init__.py
This file exports utility classes and functions for various APIs and services, including Apify, Arxiv, AWS Lambda, Bing Search, DuckDuckGo Search, Google APIs, GraphQL, Wolfram Alpha, SerpAPI, Searx Search, Wikipedia, OpenWeatherMap, Python REPL, PowerBI, Spark SQL, and Metaphor Search.

#### apify.py
This file provides a Pydantic BaseModel wrapper around the Apify API, as well as functions to run an Actor on the Apify platform and fetch records from the Actor run's default dataset. It includes optional memory limit and timeout parameters for the run. Additionally, it contains a function that runs an Apify actor with specified input and parameters, and returns a loader that fetches records from the actor's default dataset.

#### arxiv.py
This file contains a wrapper around the ArxivAPI that allows for conducting searches and fetching document summaries. It uses the `arxiv` python package and limits the document content by doc_content_chars_max. The wrapper returns the document summaries of the top-k results.

#### awslambda.py
This file contains a Python class `LambdaWrapper` which is a wrapper for the AWS Lambda SDK. It provides a method `run` to invoke a Lambda function and parse the result. The class uses `pydantic` for validation and `boto3` to interact with AWS Lambda.

#### duckduckgo_search.py
This file contains a wrapper function for the DuckDuckGo Search API that allows users to run queries and receive concatenated results. It includes default parameters for the search, and can be used to return metadata about the search results. Additionally, it contains a validation function to ensure that the necessary python package is installed. The function returns a list of dictionaries containing the snippet, title, and link of the search results, and can handle cases where no results are found.

#### google_places_api.py
This file contains a Python class `GooglePlacesAPIWrapper` which is a wrapper around the Google Places API. It allows for running a search on Google Places API and returning all the results on the input query by default, but you can use the `top_k_results` argument to limit the number of results. Additionally, it includes functions for fetching and formatting place details.

#### google_search.py
This file provides a utility for performing Google searches and parsing the results using the Google Search API. It includes a Pydantic BaseModel class and a Python function that takes a query and number of results as input and returns a list of dictionaries containing metadata about the results. Instructions on how to install necessary libraries and create an API key are also included.

#### google_serper.py
This file contains the `GoogleSerperAPIWrapper` class, which is a wrapper around the Serper.dev Google Search API. It allows you to run a query through Google Search and returns the results. You can create a free API key at https://serper.dev.

#### jira.py
This file contains a Jira API wrapper that provides a set of operations including JQL query, getting projects, creating an issue, and a catch-all Jira API call. It also validates that the API key and Python package exist in the environment. Additionally, it contains a function for connecting to a JIRA instance using the `atlassian` Python library and a method for parsing Jira issues.

#### loading.py
This file contains a function `try_load_from_hub` that loads configuration from a remote hub. It returns `None` if the path is not a hub path and raises a `ValueError` if the file type is not supported or if the file is not found. The function uses the `requests` library to download the file and a loader function to load the configuration.

#### metaphor_search.py
This file provides a utility for searching the Metaphor Search API and returning metadata about the search results, including title, URL, author, and estimated date created. It includes a wrapper for the API that validates the API key and endpoint, as well as an asynchronous method for performing the search.

#### openweathermap.py
This file contains a PyOWM wrapper for calling the OpenWeatherMap API and formatting weather information for a given location. It includes a `run` function that takes a location string as input and returns a formatted string with information such as temperature, rain, heat index, and cloud cover. The file also validates that the API key exists in the environment.

#### powerbi.py
This file contains a wrapper around a Power BI endpoint. It creates a PowerBI engine from a dataset ID and credential or token, and allows for authentication using either the credential or a supplied token. The `PowerBIDataset` class also includes functionality for fixing table names.

#### searx_search.py
This file contains a Python module for querying the Searx search engine API. It provides a `SearxSearchWrapper` class with a `run` method that takes a query string and optional parameters such as the search engine to use, and returns the top search result. It also includes instructions on how to use the wrapper and notes on potential rate limiting for public Searx instances.

#### serpapi.py
This file contains a Python wrapper around SerpAPI, providing both synchronous and asynchronous methods for making calls to the search engine. It includes functions for parsing the raw results and requires the `google-search-results` python package to be installed and the `SERPAPI_API_KEY` environment variable to be set or passed as a named parameter to the constructor.

#### spark_sql.py
This file defines a `SparkSQL` class that provides a way to interact with Spark SQL. It allows the user to specify a SparkSession, catalog, schema, and tables to include or ignore. It also provides a list of usable tables.

#### wikipedia.py
This file provides a wrapper around the WikipediaAPI that allows for conducting searches and fetching page summaries. It returns the page summaries of the top-k results and limits the Document content by doc_content_chars_max. Additionally, it includes functions for formatting page summaries and creating Document objects with metadata and content from Wikipedia pages.

#### zapier.py
This file contains a Python class and utility functions for interacting with the Zapier NLA API. It includes methods for validating the API key, creating a session with the API, listing exposed actions associated with the current user, executing an action, and previewing the parameters guessed by the AI before executing the action. Additionally, the class provides methods for returning stringified versions of JSON data for inserting back into an LLM.

<!--- END SELFDOC --->