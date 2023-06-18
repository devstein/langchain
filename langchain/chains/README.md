<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `chains` directory is for implementing reusable components, or "chains", that can be linked together to build applications. It includes a variety of chains such as conversational retrieval, summarization, QA generation, and more. The directory contains subdirectories for specific chains such as `llm_math`, `llm_summarization_checker`, `natbot`, `pal`, `qa_generation`, `qa_with_sources`, `query_constructor`, `question_answering`, `retrieval_qa`, `router`, `sql_database`, and `summarize`. Each subdirectory contains files for initializing the directory, defining base classes, loading chains from configuration files or dictionaries, and implementing different types of chains.

### Files
#### __init__.py
This file imports and exports reusable components, such as chains for conversational retrieval, QA generation, and SQL database manipulation.

#### base.py
This file contains the `Chain` class, which is a base interface that all chains should implement. It includes methods for validating and preparing inputs, applying the chain on all inputs in a list, and running the chain as text in, text out or multiple variables, text out. It also includes properties such as `memory`, `callbacks`, `callback_manager`, and `verbose`.

#### llm.py
This file contains the `LLMChain` class which is a chain that formats a prompt and calls an LLM. It has a `prompt` object to use and an `llm` object to run queries against. The class has a `_call` method that generates a response and creates outputs.

#### llm_requests.py
This file contains the `LLMRequestsChain` class, which is a chain that hits a URL and then uses an LLM to parse the results. It includes a `requests_wrapper` attribute for making HTTP requests, and `input_key`, `output_key`, and `requests_key` attributes for specifying the keys used for input, output, and requests results, respectively. Additionally, the file contains a function `_call` that extracts text from an HTML page using the `requests` library and passes it to an LLM model for prediction.

#### loading.py
This file contains functions for loading various chains used in the langchain application, including LLM chains and document embedder chains. The functions parse configuration dictionaries or file paths to load the necessary components, such as LLMs and prompts. Additionally, the file includes a dictionary of chain types and their corresponding loader functions, as well as methods for loading chains from configuration dictionaries or file paths.

#### mapreduce.py
This file implements a map-reduce chain using a language model chain for map and reduce. It includes a `MapReduceChain` class, a `Config` class for pydantic object configuration, and various other classes such as `BaseLanguageModel`, `CallbackManagerForChainRun`, `Callbacks`, `BaseCombineDocumentsChain`, `LLMChain`, `Document`, `BasePromptTemplate`, and `TextSplitter`. The `_call` method splits larger text into smaller chunks and runs the combine documents chain.

#### moderation.py
This file contains an implementation of a moderation class that uses the OpenAI Moderation API to check if a given text violates OpenAI's content policy. It requires the `openai` python package to be installed and the `OPENAI_API_KEY` environment variable to be set with the user's API key. Any valid parameters for the `openai.create` call can be passed in.

#### sequential.py
This file contains the implementation of a `SequentialChain` class that represents a chain pipeline where the outputs of one step feed directly into the next. It includes methods to validate inputs and run the chains in sequence, with the output of the last chain returned.

### Directories
#### api
The `api` directory is for implementing chains that make API requests and receive responses. It includes files for initializing the API chain, validating API request prompts, generating prompts for user input and responses to API calls, and parsing requests and errors in the API. Additionally, it contains documentation for various API endpoints such as News API, Open Meteo API, Listen Notes API, and The Movie Database (TMDB) search endpoint.

#### chat_vector_db
The `chat_vector_db` directory is for storing files related to the chat vector database module. It contains a `prompts.py` file that includes two PromptTemplate objects used for generating prompts in the module. The first template is used to rephrase a follow-up question to be a standalone question, while the second template is used to provide context and a question to be answered.

#### combine_documents
The `combine_documents` directory is for combining multiple documents into a single document using different methods such as MapReduce, MapRerank, Refine, and Stuff. It contains abstract base classes, implementation classes, and related functions for each method.

#### constitutional_ai
The `constitutional_ai` directory is for implementing the `Constitutional AI` method proposed by Bai et al. in 2022. It includes files for defining constitutional principles, generating prompts for few-shot learning, and implementing the `ConstitutionalChain` for critiquing and revising text based on constitutional principles.

#### conversation
The `conversation` directory is for carrying on a conversation and calling an LLM. It includes memory modules for conversation prompts and defines a default conversation prompt template for an AI chatbot.

#### conversational_retrieval
The `conversational_retrieval` directory is for implementing a conversational retrieval chain that allows for chatting with a vector database. It includes an initialization file, a base class for conversational retrieval chains, and a prompts file for generating prompts.

#### flare
The `flare` directory is for implementing the Flare chain, which includes a QuestionGeneratorChain, a response chain, a retriever, and an output parser. It uses OpenAI's language model to generate responses and retrieve low-confidence spans. The directory includes initialization files, implementation of the FlareChain class, and prompt templates.

#### graph_qa
The `graph_qa` directory is for question-answering over a knowledge graph. It includes the `GraphQAChain` class for entity extraction and QA, the `GraphCypherQAChain` class for generating Cypher statements and querying a graph database, and prompts for entity extraction, knowledge triplet questions, and generating Cypher statements.

#### hyde
The `hyde` directory is for generating hypothetical document embeddings using a base language model and LLM chain. It includes files for defining the `HypotheticalDocumentEmbedder` class, calling the internal LLM chain, and providing prompt templates for various types of passages.

#### llm_bash
The `llm_bash` directory is for implementing a chain that interprets prompts and executes bash code to perform bash operations. It includes initialization code, a `LLMBashChain` class for interpreting prompts and executing bash code, and a `BashOutputParser` class for parsing bash output.

#### llm_checker
The `llm_checker` directory is for creating a chain of prompts and assertions to check the validity of a given text using a language model. It includes initialization code, a base class for creating the chain, and prompt templates for creating prompts to check and revise LLMs.

#### llm_math
The `llm_math` directory is for a chain that interprets prompts and executes Python code to perform mathematical operations. It contains files for initializing the directory, defining the `LLMMathChain` class, and generating prompts for math problems.

#### llm_summarization_checker
The `llm_summarization_checker` directory is for checking the accuracy of text generation by splitting it into a list of facts, checking their truthfulness, and rewriting the text to make it more accurate. It contains an initialization file, a base file defining the `LLMSummarizationCheckerChain` class, and a `prompts` directory for storing prompts related to fact-checking and summarization.

#### natbot
The `natbot` directory is for implementing a GPT-3 driven browser through composability. It includes a base implementation for the NatBot chain, a `Crawler` class for retrieving information about a webpage's elements, and a prompt template and module for a natural language bot that controls a browser.

#### pal
The `pal` directory is for implementing Program-Aided Language Models through the `PALChain` base class, with methods for input and output keys, calling the chain, and loading PAL from math and colored object prompts. It also contains modules for solving simple math problems and a colored object prompt.

#### qa_generation
The `qa_generation` directory is for generating questions and answers from a given text using a language model. It contains a `base.py` file that defines the `QAGenerationChain` class, which generates questions and answers using a language model and a prompt template. It also contains a `prompt.py` file that provides a prompt for generating a question and answer pair in a specific JSON format.

#### qa_with_sources
The `qa_with_sources` directory is for implementing question answering with sources over documents or indexes. It includes an abstract base class for defining the structure of the chain, functions to load different types of chains, and implementations of prompt templates for refining existing answers and answering questions based on context information. It also includes classes for retrieving relevant documents from an index or vector database based on similarity search.

#### query_constructor
The `query_constructor` directory is for constructing structured queries using a query language parser and a prompt module. It includes files for parsing user input into a query object, defining the internal representation of a structured query language, generating a prompt for constructing a query, and defining a model for attribute information.

#### question_answering
The `question_answering` directory is for loading various chains and generating prompts to extract relevant text from a long document to answer a given question using a map-reduce process. It also includes prompt templates for refining an existing answer to better answer a question in question answering models and for answering questions based on given context.

#### retrieval_qa
The `retrieval_qa` directory is for building retrieval-based question-answering systems against a vector database. It contains an initialization file, a file with multiple classes for building QA systems, and a file defining a `PromptTemplate` class for generating prompts.

#### router
The `router` directory is for routing inputs to one of multiple candidate chains in langchain. It includes base classes and functions for chain routing, as well as specific router chains such as `EmbeddingRouterChain` and `LLMRouterChain`. The directory also contains implementations of multi-route chains such as `MultiPromptChain` and `MultiRetrievalQAChain`, which use LLM router chains to choose amongst prompts and retrieval QA chains respectively.

#### sql_database
The `sql_database` directory is for interacting with SQL databases using a language model. It includes the `SQLDatabaseChain` class for executing SQL queries with various configuration options, the `SQLDatabaseSequentialChain` class for sequential querying, and prompt templates for constructing SQL queries and selecting relevant tables.

#### summarize
The `summarize` directory is for summarizing documents using a given language model. It contains functions for loading different types of chains for summarizing documents, as well as prompt templates for generating prompts to write a concise summary of a given text input. The available chain types are "stuff", "map_reduce", and "refine".

<!--- END SELFDOC --->