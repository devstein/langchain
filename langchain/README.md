<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `langchain` directory is for building applications with LLMs through composability. It contains various modules and classes for handling chained inputs, caching, math utilities, document transformers, and formatting. Additionally, it includes subdirectories for creating and executing agents, implementing callback handlers, defining reusable components, and providing chat model classes. The directory also contains a Docker Compose configuration file for running the Langchain application locally and a directory for managing the Langchain CLI tool and its related configuration files. Other subdirectories include `client` for interacting with the LangChain+ API, `docstore` for implementing and providing different types of document stores, `embeddings` for implementing and providing wrappers for various embedding models, `evaluation` for evaluating and generating functionality related to language models, `experimental` for implementing and testing new features and functionalities, `graphs` for creating and manipulating graphs using NetworkX and Neo4j, `indexes` for creating and managing indexes for text data, `llms` for wrappers and implementations of various large language models APIs, `memory` for storing various classes and modules related to conversation memory, `output_parsers` for parsing the output of an LLM call into various formats, `prompts` for creating and formatting prompt templates for LLMs, `retrievers` for implementing various retrievers that retrieve relevant documents based on a query, and `tools` for providing a collection of tools for various tasks such as file management, web scraping, API operations, querying, and searching from different sources. Additionally, it includes the `utilities` directory for various utility classes and functions that provide wrappers and shims for various APIs and services, and the `vectorstores` directory for implementing various vector stores and their wrappers.

### Files
#### __init__.py
This file is the main entry point into the package and imports various modules and classes from the `langchain` directory, including agents, chains, docstore, llms, prompts, sql_database, utilities, and vectorstores. It also sets the package version and defines some variables for backwards compatibility.

#### base_language.py
This file contains an abstract base class, `BaseLanguageModel`, for language models. It includes methods for generating prompts, predicting text, and getting the number of tokens in a given text.

#### cache.py
This file defines a `BaseCache` abstract class and an `InMemoryCache` class that implements it. The `InMemoryCache` class stores data in memory and provides methods to look up and update the cache based on a prompt and an `llm_string`.

#### input.py
This file contains functions for handling chained inputs, including getting a color mapping for items and printing colored text with highlighting.

#### math_utils.py
This file contains a function `cosine_similarity` which calculates the row-wise cosine similarity between two equal-width matrices. It takes in two matrices as input and returns a numpy array of the calculated similarities.

#### model_laboratory.py
This file contains the `ModelLaboratory` class, which allows for experimenting with and comparing different LLMChain models. It includes methods for initializing with chains or LLMs, checking the validity of the input, and comparing the models by running them on input text.

#### python.py
This file provides backwards compatibility for the `PythonREPL` class by importing it from `langchain.utilities.python`.

#### requests.py
This file provides a lightweight wrapper around the `requests` library with async support, including methods for GET, POST, PATCH, PUT, and DELETE requests. It also includes an asynchronous version of the GET method and handles authentication.

#### schema.py
This file defines various classes and interfaces for defining the schema of the data used in the langchain project, including different types of messages, LLM results, prompt values, memory, and chat message history. It also includes classes for parsing the output of a language model and transforming documents, as well as providing an interface for storing and retrieving messages in a JSON file.

#### serpapi.py
This file provides backwards compatibility for the `SerpAPIWrapper` class by importing it from `langchain.utilities.serpapi`.

#### server.py
This file contains a script to run the langchain server locally using docker-compose. The script pulls the necessary images and starts the server using the docker-compose.yaml file.

#### sql_database.py
This file contains the `SQLDatabase` class, which provides methods for interacting with a SQL database, including creating an engine from a database URI or Databricks connection, getting usable table names, and retrieving information about tables. It also includes support for views and metadata reflection, and follows best practices for table descriptions. If an error occurs, appropriate errors are raised or error messages are returned.

#### text_splitter.py
This file contains multiple classes that implement different methods for splitting incoming text into smaller chunks. These methods include splitting based on characters, tokens, specific separators, NLTK, Spacy, Markdown headings, and Python syntax. The `TextSplitter` class is used as an interface for all of these methods.

#### utils.py
This file contains utility functions for the langchain codebase, including functions for getting values from a dictionary or environment variable, validating mutually exclusive keyword arguments, stringifying data, raising errors with response text, and mocking out `datetime.now()` in unit tests.

### Directories
#### agents
The `agents` directory is for creating and executing agents, loading and initializing agents, and working with conversational and structured chat agents. It includes subdirectories for different types of agents, such as conversational, structured chat, and MRKL agents, as well as toolkits for different agents, such as CSV, file management, and Python. The directory also contains files for defining agent types, validating tools, and exporting various agents and agent-related tools.

#### callbacks
The `callbacks` directory is for implementing callback handlers that listen to events in LangChain and perform various actions, such as logging metrics to external platforms, printing messages to standard output, and streaming LLM tokens. It includes callback handlers for OpenAI, stdout, AIM, Wandb, MLflow, ClearML, Comet, WhyLabs, and async iterators, as well as a callback manager for handling multiple callback handlers. The directory also contains utility functions and classes for handling metadata and associated function states for callbacks.

#### chains
The `chains` directory is for implementing reusable components, or "chains", that can be linked together to build applications. It includes a variety of chains such as conversational retrieval, summarization, QA generation, and more. The directory contains subdirectories for specific chains such as `llm_math`, `llm_summarization_checker`, `natbot`, `pal`, `qa_generation`, `qa_with_sources`, `query_constructor`, `question_answering`, `retrieval_qa`, `router`, `sql_database`, and `summarize`. Each subdirectory contains files for initializing the directory, defining base classes, loading chains from configuration files or dictionaries, and implementing different types of chains.

#### chat_models
The `chat_models` directory is for implementing and providing various chat model classes that can be used to generate chat messages. It includes classes such as `ChatOpenAI`, `AzureChatOpenAI`, `PromptLayerChatOpenAI`, `ChatAnthropic`, and `ChatGooglePalm`. These classes are wrappers around different chat APIs such as OpenAI, Azure OpenAI, Google PaLM, and Anthropic's large language model. The directory also includes an abstract base class `BaseChatModel` and a subclass `SimpleChatModel`.

#### cli
The `cli` directory is for managing the Langchain CLI tool and its related configuration files. It includes Docker Compose configuration files for setting up services, a main entry point for the CLI tool, and a directory for storing configuration files such as `nginx.conf`.

#### client
The `client` directory is for interacting with the LangChain+ API through a client class (`LangChainPlusClient`) defined in `langchain.py`. It contains methods for uploading data, creating and reading datasets, and running language models or chains on a dataset. The directory also includes Pydantic models for examples and datasets, a model for query parameters, and utility functions for running LLMs/Chains over datasets.

#### docstore
The `docstore` directory is for implementing and providing different types of document stores. It includes an in-memory document store, a Wikipedia API wrapper, and a class for providing a Langchain Docstore via arbitrary lookup function. It also defines an abstract base class and a mixin class for accessing and adding documents to a document store. The `Document` class from the `langchain.schema` module is also exported from this directory.

#### document_loaders
The `document_loaders` directory is for loading various types of documents from different sources. It includes loaders for specific file types such as EPub, Evernote, Facebook chat, Figma, Google Drive, Gutenberg, Hacker News, HTML, Hugging Face datasets, iFixit, images, IMSDb, JSON, Markdown, Mastodon toots, MediaWiki dump XML files, Modern Treasury API endpoint, Notion pages and databases, Obsidian files, Open Office ODT files, OneDrive files, PDF files, PowerPoint files, Psychic.dev platform, Python files, ReadTheDocs documentation directory dump, Reddit posts, Roam directory dump, rich text files, S3 directory, S3 file, sitemap, and Slack directory dump. Additionally, it contains loaders for loading data from APIs such as Spreedly, Stripe, and Twitter, and for loading data from URLs using Playwright, Selenium, and urllib. The directory also includes loaders for loading data from local files such as WhatsApp messages, Word documents, and YouTube transcripts. Finally, the directory contains subdirectories for loading blobs and parsing various document formats.

#### embeddings
The `embeddings` directory is for implementing and providing wrappers for various embedding models. It includes classes and functions for generating embeddings using different APIs such as Aleph Alpha, Cohere, Google PaLM, HuggingFace, Jina, LlamaCpp, OpenAI, Sagemaker, and TensorflowHub. It also includes an abstract base class `Embeddings` that serves as an interface for embedding models.

#### evaluation
The `evaluation` directory is for evaluating and generating functionality related to language models. It includes loading datasets, evaluating ReAct style agents, evaluating and generating question answering functionality, and providing prompt templates for grading student answers.

#### experimental
The `experimental` directory is for implementing and testing new features and functionalities in LangChain. It includes directories for autonomous and generative agents, implementing language models and generators, defining a pipeline for executing a series of steps, and providing instructions and code examples for enabling tracing in LangChain applications, creating and running chains on datasets, and evaluating agents using datasets.

#### graphs
The `graphs` directory is for creating and manipulating graphs using NetworkX and Neo4j. It includes an initialization file that imports and exports the necessary classes, as well as a NetworkX wrapper file that provides functions for parsing knowledge triples, extracting entities, adding and deleting triples, retrieving information about entities, writing the graph to a GML file, and clearing the graph.

#### indexes
The `indexes` directory is for creating and managing indexes for text data. It includes implementations for creating graph and vector store indexes, as well as prompt templates for entity extraction, entity summarization, and knowledge triplet extraction.

#### llms
The `llms` directory is for wrappers and implementations of various large language models APIs, including LlamaCpp, NLPCloud, OpenAI, Petals, PipelineAI, PredictionGuard, Replicate, RWKV, SagemakerEndpoint, SelfHosted, SelfHostedHuggingFaceLLM, StochasticAI, and Writer. These wrappers and implementations provide a way to generate text completions using the respective APIs, with configurable parameters such as model name, sampling temperature, maximum and minimum number of tokens to generate, and more. The directory also includes utility functions for loading LLMs from configuration files, enforcing stop tokens, and streaming results in real-time.

#### memory
The `memory` directory is for storing various classes and modules related to conversation memory in the `langchain` package. It includes classes for storing conversation history, entities, knowledge graphs, and summaries, as well as implementations for different types of memory, such as read-only memory, Motorhead memory, and simple memory. Additionally, it contains prompt templates, validators, and utility functions for formatting and managing memory variables.

#### output_parsers
The `output_parsers` directory is for parsing the output of an LLM call into various formats. It includes classes for parsing output into boolean values, lists, Pydantic models, and dictionaries using regular expressions. It also includes classes for combining parsers, fixing parsing errors, and retrying parsing with prompts. Additionally, the directory contains files with format instructions and a function for loading output parsers based on configuration.

#### prompts
The `prompts` directory is for creating and formatting prompt templates for LLMs. It includes classes for string prompts, chat prompts, and few-shot prompts, as well as functions for loading prompts and prompt templates from a configuration dictionary or file system. The `example_selector` subdirectory contains classes for selecting examples to include in prompts based on length, ngram overlap score, and semantic similarity.

#### retrievers
The `retrievers` directory is for implementing various retrievers that retrieve relevant documents based on a query. It includes classes for retrieving documents from sources such as Arxiv, Databerry, Metal, Vespa, and Wikipedia, as well as classes for compressing documents using various techniques. The directory also contains classes for implementing KNN, SVM, and TF-IDF retrievers, and a time-weighted retriever. Additionally, there are translator classes for converting internal query language elements to valid filters for Chroma, Pinecone, and Weaviate, and a `SelfQueryRetriever` class that wraps around a vector store and uses an LLM to generate the vector store queries.

#### tools
The `tools` directory is for providing a collection of tools for various tasks such as file management, web scraping, API operations, querying, and searching from different sources. It includes subdirectories for specific tools such as interacting with APIs, managing files and directories, and interacting with a web browser. Additionally, it contains tools for interacting with databases, generating images from text prompts, and running shell commands.

#### utilities
The `utilities` directory is for various utility classes and functions that provide wrappers and shims for various APIs and services, including Apify, Arxiv, AWS Lambda, Bing Search, DuckDuckGo Search, Google APIs, GraphQL, Wolfram Alpha, SerpAPI, Searx Search, Wikipedia, OpenWeatherMap, Python REPL, PowerBI, Spark SQL, and Metaphor Search. These utilities provide easy-to-use interfaces for conducting searches, fetching data, and interacting with APIs and services. Additionally, it contains a Python class and utility functions for interacting with the Zapier NLA API, including methods for validating the API key, creating a session with the API, listing exposed actions associated with the current user, executing an action, and previewing the parameters guessed by the AI before executing the action.

#### vectorstores
The `vectorstores` directory is for implementing various vector stores and their wrappers, including Annoy, AtlasDB, Chroma, DeepLake, ElasticSearch, FAISS, LanceDB, Milvus, MyScale, OpenSearch, PGVector, Pinecone, Qdrant, Redis, Supabase, Tair, Weaviate, and Zilliz. It also includes a base class for a vector store and a utility function for maximal marginal relevance. Additionally, the `docarray` subdirectory contains classes and functions for implementing vector stores based on DocArray's `DocIndex`.

<!--- END SELFDOC --->