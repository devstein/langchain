<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `retrievers` directory is for implementing various retrievers that retrieve relevant documents based on a query. It includes classes for retrieving documents from sources such as Arxiv, Databerry, Metal, Vespa, and Wikipedia, as well as classes for compressing documents using various techniques. The directory also contains classes for implementing KNN, SVM, and TF-IDF retrievers, and a time-weighted retriever. Additionally, there are translator classes for converting internal query language elements to valid filters for Chroma, Pinecone, and Weaviate, and a `SelfQueryRetriever` class that wraps around a vector store and uses an LLM to generate the vector store queries.

### Files
#### __init__.py
This file contains the imports for all retriever classes in the `langchain/retrievers` directory and defines the `__all__` list of retriever class names.

#### arxiv.py
This file contains the implementation of `ArxivRetriever` class, which is a wrapper for `ArxivAPIWrapper`. It provides a `get_relevant_documents` method that returns a list of relevant documents based on the given query. It also includes an async method `aget_relevant_documents`, which is not yet implemented.

#### chatgpt_plugin_retriever.py
This file contains the implementation of `ChatGPTPluginRetriever` class, which is a retriever that uses a ChatGPT plugin to retrieve relevant documents. It sends a query to the plugin and returns a list of `Document` objects containing the retrieved documents' content and metadata. It supports both synchronous and asynchronous requests.

#### elastic_search_bm25.py
This file implements a wrapper around Elasticsearch using BM25 as a retrieval method, providing a way to connect to an Elasticsearch instance that requires login credentials. It also includes methods for creating an Elasticsearch client instance and adding texts to the retriever and returning their ids. Additionally, it defines a class with two methods for retrieving relevant documents using ElasticSearch's BM25 algorithm.

#### knn.py
This file implements a KNN (K-Nearest Neighbors) retriever that finds the k most similar documents to a given query using embeddings and L2 norm. It also includes multithreading to speed up the index creation and a relevancy threshold to filter out dissimilar documents. Additionally, it has a method for asynchronous document retrieval, but it is not implemented.

#### llama_index.py
This file contains the implementation of `LlamaIndexRetriever` and `LlamaIndexGraphRetriever` classes, which provide a method `get_relevant_documents` to retrieve relevant documents for a given query using LlamaIndex data structure and graph data structure, respectively. It also defines a synchronous function `get_relevant_documents` that takes a query string and returns a list of `Document` objects.

#### metal.py
This file contains the implementation of the MetalRetriever class, which is a subclass of BaseRetriever. It uses the Metal SDK to search for relevant documents based on a given query and returns them as a list of Document objects. It also includes an async method, aget_relevant_documents, which is not implemented.

#### svm.py
This file implements an SVM retriever that creates an index of embeddings for a set of texts and uses an SVM model to rank the similarity of a query with the indexed documents. It also includes code for ensuring the query is in the first index and normalizing similarities, as well as an unimplemented async function for retrieving relevant documents.

#### tfidf.py
This file contains the implementation of a TF-IDF Retriever, which is a search engine based on the Term Frequency-Inverse Document Frequency algorithm. It includes a method to create a retriever from a list of texts, and a method to get the most relevant documents to a given query based on cosine similarity.

#### time_weighted_retriever.py
This file contains the implementation of a retriever that combines embedding similarity with recency in retrieving values. It uses a vector store to store documents and determine salience, and a memory stream of documents to search through. The retriever combines the similarity search with recency by using an exponential decay factor.

#### vespa_retriever.py
This file contains the `VespaRetriever` class, which is a wrapper for retrieving relevant documents from Vespa search engine. It includes methods for querying Vespa and getting relevant documents based on a query, with options for filtering and specifying parameters such as the Vespa app URL, content field, number of documents to return, metadata fields, and sources.

#### weaviate_hybrid_search.py
This file implements a Weaviate hybrid search retriever that allows for adding data objects to the index and retrieving relevant documents based on a query and optional filter.

#### wikipedia.py
This file contains the `WikipediaRetriever` class, which is a wrapper for the `WikipediaAPIWrapper` class. It provides a `get_relevant_documents()` method that returns a list of relevant documents based on a given query string. The class also includes an async method `aget_relevant_documents()`, which is not implemented.

#### zep.py
This file implements a retriever for the Zep long-term memory store, allowing users to search their long-term chat history. It includes an async function that takes a query string and returns a list of relevant documents using the Zep search engine. The function uses the `zep_python` library to create a `SearchPayload` object and sends it to the Zep search engine using the `zep_client.asearch_memory` method.

#### zilliz.py
This file contains the implementation of the ZillizRetriever class, which is a subclass of the BaseRetriever class. It provides a way to add text to the Zilliz store and retrieve relevant documents based on a query using the Zilliz library.

### Directories
#### document_compressors
The `document_compressors` directory is for compressing retrieved documents using various techniques such as LLM chains, Cohere API's `rerank` function, and embeddings. It contains modules such as `__init__.py`, `base.py`, `chain_extract.py`, `chain_extract_prompt.py`, `chain_filter.py`, `chain_filter_prompt.py`, `cohere_rerank.py`, and `embeddings_filter.py`. These modules provide classes and functions for compressing documents based on their relevance to a query context.

#### self_query
The `self_query` directory is for implementing retrievers that generate and execute structured queries over their own data source. It includes translator classes for converting internal query language elements to valid filters for Chroma, Pinecone, and Weaviate. The directory also contains the `SelfQueryRetriever` class that wraps around a vector store and uses an LLM to generate the vector store queries.

<!--- END SELFDOC --->