<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `openapi` directory is for creating agents that interact with OpenAPI APIs through a hierarchical planning approach. It includes files for defining an OpenAPI spec agent, making HTTP requests, parsing responses, orchestrating API requests, and creating prompt templates for planning a sequence of API calls. Additionally, it contains functions for simplifying and substituting references in an OpenAPI specification.

### Files
#### base.py
This file defines an OpenAPI spec agent that can be created using the `create_openapi_agent` function. The agent is constructed from a BaseLanguageModel and OpenAPIToolkit, and includes a ZeroShotAgent prompt and an LLMChain. The file imports several modules, including `OpenAPIToolkit`, `ZeroShotAgent`, `BaseLanguageModel`, `BaseCallbackManager`, and `LLMChain`. Optional parameters such as input variables, maximum iterations, and maximum execution time can be passed to the `create_openapi_agent` function.

#### planner.py
This file contains the implementation of an agent that interacts with OpenAPI APIs through a hierarchical planning approach. It includes functions and classes for making HTTP requests, parsing responses, and orchestrating API requests based on the provided OpenAPI specification. Additionally, it contains functions for creating an API controller agent and an API orchestrator agent.

#### planner_prompt.py
This file contains a prompt template for a planner that plans a sequence of API calls to assist with user queries against an API. It includes instructions for generating a plan of API calls, examples of user queries and their corresponding plans, and prompts for extracting information from API responses. The plan will be passed to an API controller that can format it into web requests and return the responses.

#### prompt.py
This file contains the `prompt` module which provides a tool for agents to answer questions about the openapi spec for the API. The tool guides the agent through the process of finding the base URL, relevant paths, and required parameters needed to make a request to answer the question. The module also includes example inputs and a description of how to use the tool.

<!--- END SELFDOC --->