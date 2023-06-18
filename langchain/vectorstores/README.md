<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `vectorstores` directory is for implementing various vector stores and their wrappers, including Annoy, AtlasDB, Chroma, DeepLake, ElasticSearch, FAISS, LanceDB, Milvus, MyScale, OpenSearch, PGVector, Pinecone, Qdrant, Redis, Supabase, Tair, Weaviate, and Zilliz. It also includes a base class for a vector store and a utility function for maximal marginal relevance. Additionally, the `docarray` subdirectory contains classes and functions for implementing vector stores based on DocArray's `DocIndex`.

### Files
#### __init__.py
This file contains the imports for all the vector stores available in the langchain repository.

#### analyticdb.py
This file contains an implementation of `AnalyticDB`, a `VectorStore` that uses AnalyticDB, a distributed full PostgresSQL syntax cloud-native database. It provides methods for initializing a `VectorStore` from texts and embeddings, running similarity search with distance, and adding texts to the vectorstore using the AnalyticDB backend.

#### atlas.py
This file contains the implementation of `AtlasDB`, a vector store that provides methods for creating and managing Atlas projects, adding texts and embeddings to a project, creating an index, and running similarity search. It can be created from raw documents using the `from_texts` or `from_documents` method, and requires an embedding function for text similarity search.

#### base.py
This file defines an abstract class `VectorStore` which serves as an interface for vector stores. It defines methods to add texts and documents to the vector store. The `add_texts` method takes an iterable of strings and an optional list of metadata associated with the texts, and returns a list of ids from adding the texts into the vector store. The `add_documents` method takes a list of `Document` objects and returns a list of IDs of the added texts.

#### chroma.py
This file contains the implementation of a Chroma vectorstore, which can be created from a list of texts or documents and supports the addition of metadata and document IDs. It includes methods for querying and adding texts to the collection, running similarity search with Chroma, and selecting documents using the maximal marginal relevance algorithm.

#### deeplake.py
This file contains a function `vector_search` that performs a naive search for nearest neighbors using a specified distance metric and returns the indices and distances of the nearest neighbors. The function takes in a query embedding, data vectors, distance metric, and k value as inputs.

#### elastic_vector_search.py
This file contains a wrapper around Elasticsearch vector database, providing a common interface for all vector database implementations. It includes classes for connecting to an Elasticsearch instance, adding texts to an Elasticsearch index for embeddings, and performing similarity search using Elasticsearch. The ElasticVectorSearch class provides a user-friendly interface to search for documents most similar to a given query, using Elasticsearch to create a new index for the embeddings and adding the documents to the newly created Elasticsearch index.

#### faiss.py
This file contains a wrapper around the FAISS vector database. It includes a function to import FAISS, which raises an error if the package is not installed. The wrapper provides a way to load FAISS with no AVX2 optimization for compatibility with other devices.

#### lancedb.py
This file implements a wrapper class called `LanceDB` around the LanceDB vector database, providing methods to add texts and search for similar texts. It also includes a `from_texts` class method to create a `LanceDB` instance from a list of texts, an embedding, and optional metadata.

#### milvus.py
This file contains a Python class for interacting with a Milvus vector database. It includes methods for creating a connection to the Milvus server, initializing the vector store, inserting data, performing similarity searches, and reordering results based on maximal marginal relevance. It also allows for customization of various parameters such as collection name, connection arguments, consistency level, index parameters, and search parameters.

#### myscale.py
This file contains a wrapper around the MyScale vector database, including a `MyScaleSettings` class for configuring the client and a `VectorStore` class for interacting with the database. It provides methods for adding, deleting, and querying vectors, and supports complex queries with multiple conditions, constraints, and sub-queries.

#### opensearch_vector_search.py
This file contains a class for performing similarity search with OpenSearch, including support for approximate search, script scoring, and painless scripting. It also includes functions for ingesting embeddings into an OpenSearch index and generating search queries for approximate, script scoring, or painless scripting searches.

#### pgvector.py
This file contains the implementation of `PGVector`, a `VectorStore` that uses Postgres and pgvector. It includes methods for initializing the store, creating, deleting, and getting collections, adding texts to the vectorstore with optional metadata, and performing similarity searches on PostgreSQL databases using vector embeddings.

#### pinecone.py
This file contains the implementation of a wrapper around Pinecone vector database, which is a subclass of the VectorStore abstract class. It provides an interface to interact with Pinecone's vector database using the Pinecone client python package.

#### redis.py
This file contains a Redis class and functions for interacting with a Redis-based vector store. It includes methods for creating and dropping a Redis index, adding documents to the vector store, and performing similarity search on indexed documents.

#### supabase.py
This file defines the `SupabaseVectorStore` class, which is a `VectorStore` for a Supabase postgres database. It assumes that the `pgvector` extension is installed and a `match_documents` function is available. It also provides instructions on how to modify the `match_documents` function to use `max_marginal_relevance_search`.

#### weaviate.py
This file contains a wrapper around the Weaviate vector database, including functions for creating a client, defining a schema, and performing similarity searches. It also provides a user-friendly interface for constructing a Weaviate wrapper from raw documents.

#### zilliz.py
This file defines a Python class called `Zilliz` that extends the `Milvus` class and represents a vector store. It contains methods for creating an index on the collection using either a default AutoIndex or an HNSW based index, adding texts and their corresponding metadata to the vector store, and initializing the vector store with various parameters such as embedding function, collection name, connection arguments, consistency level, index parameters, and search parameters.

### Directories
#### docarray
The `docarray` directory is for implementing vector stores based on DocArray's `DocIndex`. It includes classes for efficient similarity search (`DocArrayHnswSearch`) and exact search (`DocArrayInMemorySearch`). The directory also contains helper functions for describing the schema of `DocIndex`, performing similarity search and relevance scoring on a collection of documents, and selecting documents using maximal marginal relevance.

<!--- END SELFDOC --->