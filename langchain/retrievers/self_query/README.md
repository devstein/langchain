<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `self_query` directory is for implementing retrievers that generate and execute structured queries over their own data source. It includes translator classes for converting internal query language elements to valid filters for Chroma, Pinecone, and Weaviate. The directory also contains the `SelfQueryRetriever` class that wraps around a vector store and uses an LLM to generate the vector store queries.

### Files
#### base.py
This file implements the `SelfQueryRetriever` class, which generates and executes structured queries over its own data source using an LLM to generate the vector store queries. It also includes a function `_get_builtin_translator` that gets the translator class corresponding to the vector store class. The class allows for customization of the search type and keyword arguments.

<!--- END SELFDOC --->