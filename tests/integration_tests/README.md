<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `integration_tests` directory is for testing the integration of the `langchain` codebase with external APIs and services, including utilities and vector stores. The tests cover various functionality and APIs, ensuring that the wrappers and utilities return the expected results for various queries and handle edge cases correctly. The directory includes fixtures for generating test data and distance metrics, as well as cassettes for custom indexing and querying documents in Elasticsearch, Pinecone vector store, and Weaviate's vector store.

### Files
#### conftest.py
This file contains fixtures for the integration tests. It defines a fixture for the test directory and a fixture for the VCR cassette directory. It also loads the .env file if it exists.

#### test_document_transformers.py
This file contains integration tests for the `EmbeddingsRedundantFilter` class in the `document_transformers` module. The tests use the `OpenAIEmbeddings` class to create embeddings and check if the filter correctly removes redundant documents.

#### test_nlp_text_splitters.py
This file contains integration tests for the NLTK and Spacy based sentence splitters in the `langchain.text_splitter` module. The tests include checking for invalid arguments and testing the functionality of the splitters by splitting a text into sentences and comparing the output with the expected output.

#### test_pdf_pagesplitter.py
This file contains an integration test for the PDF page splitter functionality. The test loads a PDF file, splits it into pages, and checks that the page metadata is correctly set. It also tests the similarity search functionality using FAISS and OpenAI embeddings.

#### test_schema.py
This file contains integration tests for the `_get_token_ids_default_method` function in `base_language.py`. The tests check that the function returns the correct token IDs for various inputs, including empty strings and strings with special characters.

#### test_text_splitter.py
This file contains integration tests for the `CharacterTextSplitter` and `TokenTextSplitter` classes in the `langchain.text_splitter` module. The tests ensure that the text splitters work as expected, including proper type checking and correct splitting of text into chunks based on specified parameters.

### Directories
#### agent
The `agent` directory is for integration tests of the `langchain.agents` module. It includes tests for creating a Pandas DataFrame agent and a PowerBI agent.

#### cache
The `cache` directory is for holding integration tests for Cache objects, including tests for the default caching behavior of the GPTCache class and integration tests for Redis cache functionality.

#### callbacks
The `callbacks` directory is for integration tests of the `callbacks` module in the `langchain` repository. The tests include verifying the functionality of the `LANGCHAIN_SESSION` environment variable and testing the `get_openai_callback` function with the OpenAI language model.

#### chains
The `chains` directory is for integration tests of different chain classes such as Graph Database Chain, PALChain, ReActChain, SelfAskWithSearchChain, and SQLDatabaseChain. These tests cover the functionality of the chains and their ability to generate answers to prompts and questions.

#### chat_models
The `chat_models` directory is for testing the functionality of different chatbot models and their wrappers. The directory contains test files for the `ChatAnthropic`, `ChatGooglePalm`, `ChatOpenAI`, and `PromptLayerChatOpenAI` classes, which cover basic functionality, message generation, streaming, and callback handling.

#### document_loaders
The `document_loaders` directory is for integration tests of various document loaders in the `langchain` codebase. The tests cover different loaders, including ArxivLoader, BigQueryLoader, BiliBiliLoader, BlockchainDocumentLoader, ConfluenceLoader, DataFrameLoader, DuckDBLoader, OutlookMessageLoader, FacebookChatLoader, FigmaFileLoader, GitbookLoader, IFixitLoader, JSONLoader, MastodonLoader, ModernTreasuryLoader, UnstructuredODTLoader, various PDF loaders, PythonLoader, SitemapLoader, SlackLoader, SpreedlyLoader, StripeLoader, UnstructuredAPIFileLoader, UnstructuredAPIFileIOLoader, UnstructuredURLLoader, Playwright URLLoader, and WhatsAppChatLoader. The tests ensure that the loaders can successfully load documents and extract metadata and content.

Additional Summary:
The `document_loaders` directory also includes a `parsers` subdirectory for testing various PDF parsers, including PyMuPDF, PyPDF, PDFMiner, PyPDFium2, and PDFPlumber, to ensure that they can correctly load and parse a PDF document.

#### embeddings
The `embeddings` directory is for integration tests of various embedding classes and their functionality. It includes tests for embedding documents and queries, as well as similarity search using embeddings. The directory contains tests for classes such as CohereEmbeddings, Google PaLM embeddings, HuggingFaceEmbeddings, HuggingFaceHubEmbeddings, Jina embeddings, LlamaCppEmbeddings, OpenAI embeddings, SelfHostedEmbeddings, sentence_transformer embeddings, and TensorflowHubEmbeddings.

#### examples
The `examples` directory is for storing various example files, including HTML, JSON, and XML files, as well as sample chat conversations from Facebook and WhatsApp. These files are used for testing and demonstration purposes.

#### llms
The `llms` directory is for integration tests of various API wrappers and classes that implement LLMs. These tests cover valid and invalid calls to the APIs, saving/loading LLMs, streaming tokens, error handling, and stop logic. The directory includes tests for API wrappers such as AI21, Aleph Alpha, Anthropic, Anyscale, BananaDev, CerebriumAI, Cohere, ForefrontAI, GooseAI, GPT4All, HuggingFace, LlamaCpp, Modal, NLPCloud, OpenAI, Petals, Pipeline Cloud, PredictionGuard, RWKV, and more. The tests include initializing and running inference on self-hosted Hugging Face pipelines, testing the StochasticAI and Writer API wrappers, and a function for checking LLM object equality.

#### memory
The `memory` directory is for integration tests of different message stores with the `ConversationBufferMemory` class from the `langchain.memory` module. The tests add messages to the message stores, retrieve them, and check if they are in the expected format. Finally, the tests clear the message history to prepare for the next test run. The message stores tested include Cassandra, Azure Cosmos DB, Firestore, MongoDB, and Redis.

#### prompts
The `prompts` directory is for integration tests of the `NGramOverlapExampleSelector` class, which tests its ability to select examples based on ngram overlap scores, add new examples, and set the threshold to 0.0. It also includes tests for cases where the threshold is greater than 1.0 and for the accuracy of the `ngram_overlap_score` function.

#### retrievers
The `retrievers` directory is for integration tests of various classes related to document retrieval, including ArxivRetriever, AzureCognitiveSearchRetriever, ContextualCompressionRetriever, TFIDFRetriever, WeaviateHybridSearchRetriever, and WikipediaRetriever. The tests ensure that the retrievers can successfully retrieve relevant documents for a given query, both synchronously and asynchronously, and that they behave correctly when given invalid queries.

#### utilities
The `utilities` directory is for integration tests of various API wrappers and utilities used in the `langchain` codebase, including Arxiv, DuckDuckGoSearch, GoogleSearch, GoogleSerper, JIRA, OpenWeatherMap, PowerBI, SerpAPI, Wikipedia, and Wolfram Alpha. The tests ensure that the wrappers and utilities return the expected results for various queries and handle edge cases correctly.

#### vectorstores
The `vectorstores` directory is for integration tests of various vector store implementations, including Annoy, AtlasDB, Chroma, DeepLake, ElasticSearch, FAISS, LanceDB, Milvus, MyScale, OpenSearch, Pinecone, Qdrant, Redis, Tair, Weaviate, and Zilliz. The tests cover end-to-end construction and search functionality, metadata, scores, filters, and maximum marginal relevance search. The directory also includes fixtures for generating test data and distance metrics, as well as cassettes for custom indexing and querying documents in Elasticsearch, Pinecone vector store, and Weaviate's vector store.

<!--- END SELFDOC --->