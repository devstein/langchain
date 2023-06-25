<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `hyde` directory is for generating hypothetical document embeddings using a base language model and LLM chain. It includes files for defining the `HypotheticalDocumentEmbedder` class, calling the internal LLM chain, and providing prompt templates for various types of passages.

### Files
#### __init__.py
This file contains the docstring for the `langchain/chains/hyde` package, which provides hypothetical document embeddings based on the paper at the provided URL.

#### base.py
This file defines the `HypotheticalDocumentEmbedder` class, which generates hypothetical documents for a given query using a base language model and LLM chain, and then combines their embeddings into a final embedding. It also includes methods to call the internal LLM chain and load/use the LLMChain for a specific prompt key.

#### prompts.py
This file contains a dictionary of prompt templates for various types of passages, including scientific papers, news articles, and financial articles. Each template includes a prompt for the user to write a passage in response to a given question or topic.

<!--- END SELFDOC --->