<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `docarray` directory is for implementing vector stores based on DocArray's `DocIndex`. It includes classes for efficient similarity search (`DocArrayHnswSearch`) and exact search (`DocArrayInMemorySearch`). The directory also contains helper functions for describing the schema of `DocIndex`, performing similarity search and relevance scoring on a collection of documents, and selecting documents using maximal marginal relevance.

### Files
#### __init__.py
This file is a Python package that exports two classes, `DocArrayHnswSearch` and `DocArrayInMemorySearch`, from the `hnsw.py` and `in_memory.py` modules, respectively.

#### base.py
This file defines the `DocArrayIndex` class, which is a subclass of `VectorStore` and an abstract base class for vector stores based on DocArray's `DocIndex`. It also contains helper functions for describing the schema of `DocIndex` and performing similarity search and relevance scoring on a collection of documents. Additionally, it includes a method for selecting documents using maximal marginal relevance, optimizing for similarity to the query and diversity among selected documents.

#### hnsw.py
This file contains the implementation of `DocArrayHnswSearch` class, which is a wrapper around Hnswlib store for efficient similarity search. It includes a method for initializing the store, building an HNSW index for a DocArray, and inserting data. The class takes in various arguments such as the embedding function, distance metric, maximum number of vectors, and number of threads, among others, to build the index. The `from_texts` method creates a `DocArrayHnswSearch` store and inserts data, taking in a list of texts, an embedding function, optional metadata, a work directory path, and other keyword arguments.

#### in_memory.py
This file contains a wrapper class `DocArrayInMemorySearch` and a function `from_texts` for creating an in-memory vector store with exact search capabilities. The class provides methods for initializing the store and inserting data, while the function allows for creating a vector store from a list of texts and their embeddings, with optional metadata and a specified search metric.

<!--- END SELFDOC --->