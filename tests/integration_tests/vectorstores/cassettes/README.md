<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `cassettes` directory is for storing integration test files for custom indexing and querying documents in Elasticsearch, Pinecone vector store, and Weaviate's vector store. It includes YAML-encoded cassettes for testing various functionalities, such as creating custom indexes, adding documents, and testing search with filters.

### Directories
#### test_elasticsearch
The `test_elasticsearch` directory is for storing integration test files related to custom indexing and querying documents in Elasticsearch. It includes YAML files with request bodies and cassettes for testing the creation of custom indexes from documents and adding documents to them.

#### test_pinecone
The `test_pinecone` directory is for storing YAML-encoded cassettes that contain integration tests for various functions in the Pinecone vector store, including `test_from_texts`, `test_from_texts_with_metadatas`, and `test_from_texts_with_scores`. These tests involve sending requests to the OpenAI API and verifying the responses, as well as testing the functionality of creating a Pinecone index from a list of texts with associated scores.

#### test_weaviate
The `test_weaviate` directory is for testing various functionalities of Weaviate's vector store, including max marginal relevance search, similarity search with and without metadata, and search with filters. The tests are written in YAML format and include requests, responses, headers, and status codes.

<!--- END SELFDOC --->