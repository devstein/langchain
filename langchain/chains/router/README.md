<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `router` directory is for routing inputs to one of multiple candidate chains in langchain. It includes base classes and functions for chain routing, as well as specific router chains such as `EmbeddingRouterChain` and `LLMRouterChain`. The directory also contains implementations of multi-route chains such as `MultiPromptChain` and `MultiRetrievalQAChain`, which use LLM router chains to choose amongst prompts and retrieval QA chains respectively.

### Files
#### __init__.py
This file is the initialization file for the `langchain/chains/router` directory. It imports and exports various router chains, including `RouterChain`, `MultiRouteChain`, `MultiPromptChain`, `MultiRetrievalQAChain`, and `LLMRouterChain`.

#### base.py
This file contains the base classes and functions for chain routing in langchain. It defines the `RouterChain` class for determining the destination chain and the `MultiRouteChain` class for routing inputs to one of multiple candidate chains. It also includes a `_call` function that uses the router chain to call the corresponding chain and raises a `ValueError` if the destination chain is invalid and `silent_errors` is not set.

#### embedding_router.py
This file contains the `EmbeddingRouterChain` class, which is a subclass of `RouterChain`. It uses embeddings to route between options and has a convenience constructor that takes names and descriptions of options, creates documents from them, and constructs a vector store from the documents.

#### llm_router.py
This file contains the `LLMRouterChain` class, which defines a router chain that uses an LLM chain to perform routing. It includes a root validator to ensure that the LLM chain prompt has an output parser that converts LLM text output to a dictionary with keys 'destination' and 'next_inputs'. It also has a method to validate outputs, and a `parse` function that takes in a string of text and returns a dictionary with keys "destination" and "next_inputs".

#### multi_prompt.py
This file contains the implementation of `MultiPromptChain`, a multi-route chain that uses an LLM router chain to choose amongst prompts. It allows inputs to be routed to different destinations and has a default chain for unmapped inputs. Additionally, it contains a convenience constructor for instantiating a `MultiPromptChain` from destination prompts.

<!--- END SELFDOC --->