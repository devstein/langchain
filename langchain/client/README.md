<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `client` directory is for interacting with the LangChain+ API through a client class (`LangChainPlusClient`) defined in `langchain.py`. It contains methods for uploading data, creating and reading datasets, and running language models or chains on a dataset. The directory also includes Pydantic models for examples and datasets, a model for query parameters, and utility functions for running LLMs/Chains over datasets.

### Files
#### __init__.py
This file exports the `LangChainPlusClient` class from the `langchain` module, making it available for use in other parts of the codebase.

#### langchain.py
This file defines the `LangChainPlusClient` class, which is a client for interacting with the LangChain+ API. It contains various methods for interacting with the API, including uploading data, reading and listing runs and sessions, creating and reading datasets, and running a language model or chain on a dataset. The class uses the `retry` decorator to retry API calls up to three times if they fail.

#### models.py
This file contains Pydantic models for examples and datasets. It also includes a model for query parameters used in the GET /runs endpoint.

#### runner_utils.py
This file contains utility functions for running LLMs/Chains over datasets, including functions for getting prompts and messages from inputs and running LLMs/Chains synchronously or asynchronously. It also includes functions for processing examples and storing traces to a specified session name. The file supports both BaseLLM and BaseChatModel types of language models and allows for tracing runs.

<!--- END SELFDOC --->