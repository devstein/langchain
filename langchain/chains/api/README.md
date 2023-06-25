<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `api` directory is for implementing chains that make API requests and receive responses. It includes files for initializing the API chain, validating API request prompts, generating prompts for user input and responses to API calls, and parsing requests and errors in the API. Additionally, it contains documentation for various API endpoints such as News API, Open Meteo API, Listen Notes API, and The Movie Database (TMDB) search endpoint.

### Files
#### __init__.py
This file contains the initialization code for the API chain, which is responsible for making API calls and summarizing the responses to answer a question.

#### open_meteo_docs.py
This file contains the documentation for the Open Meteo API, including a list of parameters and their descriptions, valid values for the `hourly` parameter, and corresponding weather variables with units and descriptions. The API provides a JSON hourly weather forecast for 7 days and accepts a geographical coordinate and a list of weather variables as input.

#### podcast_docs.py
This file contains the API documentation for searching podcasts or episodes using the Listen Notes API. It includes a table of query parameters, a response schema, and an example of how to use the `page_size` parameter.

#### prompt.py
This file contains a `PromptTemplate` class for generating prompts to build API URLs and summarize API responses. The prompts take in `api_docs`, `question`, `api_url`, and `api_response` as input variables and provide a template for generating the prompt message. The `API_URL_PROMPT_TEMPLATE` generates a prompt to build an API URL based on the given documentation and question, while the `API_RESPONSE_PROMPT_TEMPLATE` generates a prompt to summarize the API response.

#### tmdb_docs.py
This file contains a string variable `TMDB_DOCS` that contains the API documentation for The Movie Database (TMDB) search endpoint. It includes information on query parameters, response schema, and the structure of the JSON object returned by the API.

### Directories
#### openapi
The `openapi` directory is for implementing chains that interact with OpenAPI endpoints using natural language. It includes files for constructing a path, extracting query and request body parameters, and deserializing JSON input. The directory also contains files for generating prompts for user input and responses to API calls, parsing requests and errors in the API, and parsing the response and error tags.

<!--- END SELFDOC --->