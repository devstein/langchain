<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `openapi` directory is for implementing chains that interact with OpenAPI endpoints using natural language. It includes files for constructing a path, extracting query and request body parameters, and deserializing JSON input. The directory also contains files for generating prompts for user input and responses to API calls, parsing requests and errors in the API, and parsing the response and error tags.

### Files
#### chain.py
This file defines the `OpenAPIEndpointChain` class, which is a chain that interacts with an OpenAPI endpoint using natural language. It includes methods for constructing a path, extracting query and request body parameters, and deserializing JSON input. The class also has an `api_request_chain` and an optional `api_response_chain`, as well as a `param_mapping` property that maps parameter names to parameter values. The file also contains methods for creating an `OpenAPIEndpointChain` object from a specified URL, HTTP method, and language model, as well as from an operation and a specification.

#### prompts.py
This file contains the `REQUEST_TEMPLATE` and `RESPONSE_TEMPLATE` strings used for generating prompts for user input and responses to API calls. The `REQUEST_TEMPLATE` string provides instructions for providing JSON arguments conforming to a provided schema, while the `RESPONSE_TEMPLATE` string provides instructions for responding to API responses with a human-understandable synthesis or error message. Both templates include markdown code blocks for formatting.

#### requests_chain.py
This file contains the implementation of the `APIRequesterChain` class, which is responsible for parsing requests and errors in the API. It also defines the `APIRequesterOutputParser` class, which is used to parse the request and error tags.

#### response_chain.py
This file contains the implementation of the `APIResponderChain` class, which is a subclass of `LLMChain`. It provides a `parse` method to parse the response and error tags and a `from_llm` method to get the response parser. The `APIResponderOutputParser` class is also defined in this file, which is used to parse the response and error tags.

<!--- END SELFDOC --->