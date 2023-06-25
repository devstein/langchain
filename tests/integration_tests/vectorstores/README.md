<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `vectorstores` directory is for integration tests of various vector store implementations, including Annoy, AtlasDB, Chroma, DeepLake, ElasticSearch, FAISS, LanceDB, Milvus, MyScale, OpenSearch, Pinecone, Qdrant, Redis, Tair, Weaviate, and Zilliz. The tests cover end-to-end construction and search functionality, metadata, scores, filters, and maximum marginal relevance search. The directory also includes fixtures for generating test data and distance metrics, as well as cassettes for custom indexing and querying documents in Elasticsearch, Pinecone vector store, and Weaviate's vector store.

### Files
#### __init__.py
This file is the package initializer for the `vectorstores` directory and contains a brief description of the purpose of the directory.

#### conftest.py
This file contains pytest fixtures for integration tests. It includes `vcr_config` fixture that returns a dictionary with filter_headers options to replace certain headers with dummy values during cassette playback and filters requests to certain hosts. Additionally, it defines `documents` and `texts` fixtures that yield generator objects returning a list of documents and strings respectively. Lastly, it includes the `embedding_openai` fixture that returns an instance of the `OpenAIEmbeddings` class.

#### fake_embeddings.py
This file contains a `FakeEmbeddings` class that provides fake embeddings functionality for testing purposes. It includes methods to embed documents and queries, returning simple embeddings that encode each text as its index and constant query embeddings respectively.

#### test_analyticdb.py
This file contains tests for the `AnalyticDB` class, covering end-to-end construction and search of documents with metadata, scores, and filter match, as well as testing the similarity search functionality.

#### test_annoy.py
This file contains multiple test functions that comprehensively test the functionality of the Annoy vector store. The tests cover end-to-end construction and search, vector similarity, metadata, adding of texts, and serialization of the vector store.

#### test_elasticsearch.py
This file contains integration tests for ElasticSearch functionality in the langchain codebase. It tests end-to-end construction and similarity search with and without metadata using ElasticVectorSearch and FakeEmbeddings. The tests also check the construction of both default and custom ElasticSearch indices using various methods.

#### test_faiss.py
This file contains multiple test functions that comprehensively test the functionality of the FAISS vector store, including end-to-end construction and search, vector similarity, serialization, and handling of invalid input. The tests use the `FakeEmbeddings` class to generate fake embeddings for testing purposes.

#### test_lancedb.py
This file contains two integration tests for the LanceDB vector store. The first test creates a table, adds data to it, and performs a similarity search. The second test adds a new text to the table and performs another similarity search.

#### test_milvus.py
This file contains integration tests for the Milvus vector store implementation. The tests cover end-to-end construction and search, end-to-end construction and search with scores and IDs, and end-to-end construction and MRR search. The tests also cover adding texts and metadata to the store, performing similarity searches, and ensuring that the store is not dropped when specified.

#### test_myscale.py
This file contains three test functions that test the end-to-end construction and search functionality of the MyScale class from the langchain.vectorstores module. The tests use different configurations and input parameters to ensure the correct output is returned.

#### test_opensearch.py
This file contains integration tests for the OpenSearchVectorSearch class, covering end-to-end indexing and search with metadata, custom vector and text field names, and various search types including approximate search and script scoring.

#### test_pgvector.py
This file contains integration tests for the PGVector class, which provides functionality for working with PostgreSQL vectors. The tests cover end-to-end construction and search functionality with and without scores, filtering, and metadata. The tests use a fake embeddings class to test the functionality of the class.

#### test_pinecone.py
This file contains integration tests for the Pinecone vector store, covering various scenarios such as constructing and searching with text data and metadata, adding documents with and without IDs, and testing namespaces. The tests use the OpenAIEmbeddings class for generating embeddings.

#### test_qdrant.py
This file contains integration tests for the Qdrant vector store. The tests cover end-to-end construction and search functionality, including adding new documents to the store and searching for similar documents based on their embeddings.

#### test_weaviate.py
This file contains multiple integration tests for Weaviate vector store. The tests include end-to-end construction and similarity search with metadata, UUIDs, and maximum marginal relevance (MRR) search. It also tests the `max_marginal_relevance_search` and `max_marginal_relevance_search_by_vector` functions using various parameters and asserts that the output is as expected.

#### test_zilliz.py
This file contains test functions that test the end-to-end construction and search functionality of the Zilliz vector store, including similarity search, similarity search with scores and IDs, and maximum marginal relevance search. It also includes tests for adding texts and metadata to a Zilliz document search object and checking the length of the output.

### Directories
#### cassettes
The `cassettes` directory is for storing integration test files for custom indexing and querying documents in Elasticsearch, Pinecone vector store, and Weaviate's vector store. It includes YAML-encoded cassettes for testing various functionalities, such as creating custom indexes, adding documents, and testing search with filters.

#### docarray
The `docarray` directory is for integration tests of the `DocArrayHnswSearch` and `DocArrayInMemorySearch` classes in the `langchain.vectorstores.docarray` module. The tests cover end-to-end construction and similarity search using different parameters and distance metrics.

#### docker-compose
The `docker-compose` directory is for running Elasticsearch and Kibana services, as well as Weaviate, a vector search engine, in containers using docker-compose configuration files.

#### fixtures
The `fixtures` directory is for storing test fixtures related to vector stores. It contains a single file `sharks.txt` which provides information about sharks, including their physical characteristics, classification, behavior, and the threat to their populations due to human activities.

<!--- END SELFDOC --->