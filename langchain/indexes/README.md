<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `indexes` directory is for creating and managing indexes for text data. It includes implementations for creating graph and vector store indexes, as well as prompt templates for entity extraction, entity summarization, and knowledge triplet extraction.

### Files
#### __init__.py
This file is the initializer for the `indexes` directory. It imports and exports the `GraphIndexCreator` and `VectorstoreIndexCreator` classes from their respective files.

#### graph.py
This file contains the implementation of `GraphIndexCreator`, a class that creates a graph index from text using the `NetworkxEntityGraph` class. It uses the `LLMChain` class to extract knowledge triplets from the text and adds them to the graph.

#### vectorstore.py
This file contains a `VectorStore` class that creates a vector store index from documents or loaders using `Chroma` and `OpenAIEmbeddings` classes. It provides methods for querying the vector store with or without sources. The file imports various modules such as pydantic, langchain, and typing.

### Directories
#### prompts
The `prompts` directory is for providing prompt templates and implementations for constructing indexes. It includes prompts for entity extraction, entity summarization, and knowledge triplet extraction.

<!--- END SELFDOC --->