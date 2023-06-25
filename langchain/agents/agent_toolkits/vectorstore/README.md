<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `vectorstore` directory is for interacting with and querying vector stores. It contains modules for creating VectorStore agents, routing between vector stores, and providing tools for interacting with vector stores.

### Files
#### __init__.py
This file contains the package initialization code for the `vectorstore` toolkit, which provides functionality for interacting with vector stores.

#### base.py
This file implements a VectorStore agent that is constructed from a BaseLanguageModel and a VectorStoreToolkit. It also contains a function `create_vectorstore_router_agent` that constructs a vectorstore router agent from a BaseLanguageModel and a VectorStoreRouterToolkit. The agents are created using a ZeroShotAgent and an LLMChain, and allow for the execution of various tools.

#### prompt.py
This file contains two string variables, `PREFIX` and `ROUTER_PREFIX`, which provide introductory messages for agents designed to answer questions about sets of documents and agents designed to answer questions in general, respectively.

#### toolkit.py
This file contains the `VectorStoreToolkit` and `VectorStoreRouterToolkit` classes. The former provides tools for interacting with a vector store, including a method for querying the store using a language model. The latter is used for routing between vector stores and returns a list of `VectorStoreQATool` objects, each with a name, description, vector store, and language model.

<!--- END SELFDOC --->