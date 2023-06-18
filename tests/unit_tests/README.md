<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `unit_tests` directory is for testing various modules and classes in the `langchain` codebase. It includes subdirectories for testing different functionalities such as evaluation, examples, LLMS, memory, output parsers, prompts, retrievers, tools, utilities, and vector stores. The tests ensure that the codebase functions correctly and that the different functionalities return the expected output.

### Files
#### __init__.py
This file simply contains a docstring that states that it contains all the unit tests for the codebase.

#### conftest.py
This file contains configuration and a pytest fixture for unit tests. It includes custom command line options for running specific types of tests and support for a custom marker denoting tests that require specific packages to be installed. The pytest fixture checks for required packages and skips tests if they are not installed, with extended tests failing if a required package is missing.

#### test_bash.py
This file contains unit tests for the `BashProcess` utility, which allows running bash commands from Python. The tests include checking the correct functionality of the `pwd` command, handling of incorrect commands, optional returning of shell output on incorrect commands, creation of a directory and files in a temporary directory, and persistent bash terminal using the `pexpect` library. Some tests are skipped on Windows.

#### test_depedencies.py
This file contains unit tests that check the project's dependencies. The tests ensure that only test running infrastructure dependencies are added to the test group and that certain dependencies are present or removed in the correct order.

#### test_document_transformers.py
This file contains unit tests for the `_filter_similar_embeddings` function in the `langchain.document_transformers` module. The tests ensure that the function correctly filters similar embeddings based on cosine similarity and a given threshold.

#### test_formatting.py
This file contains unit tests for the `formatter` function in the `formatting` module. The tests ensure that the function formats strings correctly, raises an error when positional arguments are used, and does not allow extra keyword arguments.

#### test_math_utils.py
This file contains unit tests for math utility functions in the `langchain` codebase. The tests cover functions for calculating cosine similarity between vectors, including tests for edge cases such as empty lists and zero matrices. The tests use `pytest` and `numpy` for testing and assertions.

#### test_sql_database_schema.py
This file contains unit tests for the SQL database schema wrapper. It tests the construction of table info, successful execution of commands, metadata creation, and querying specific data from the database. The tests use DuckDB as SQLite does not support schemas.

#### test_text_splitter.py
This file contains unit tests for the text splitting functionality of the `langchain` library, including splitting text by character count, edge cases, and word length. It also covers the `CharacterTextSplitter` class, which includes tests for splitting text by characters, merging splits with a given separator, and creating documents with and without metadata. Additionally, there is a test for the `split_documents` function in the `CharacterTextSplitter` class, which checks if the function splits a list of `Document` objects into smaller chunks based on the specified parameters and returns the expected output.

### Directories
#### agents
The `agents` directory is for unit tests of various classes and functions related to agents, including tests for the `Agent` and `AgentExecutor` classes, MRKL functionality, public API, `ReActChain` and `ReActDocstoreAgent` classes, serialization of an agent object, `create_sql_agent` function, `Tool` class and its associated utility functions, and `AgentType` enum and `AGENT_TO_CLASS` dictionary.

#### callbacks
The `callbacks` directory is for testing the correct functioning of callbacks. It includes a fake callback handler, unit tests for the `CallbackManager` class and the `OpenAICallbackHandler` class, and a subdirectory for unit tests of the tracers used in LangChain. The purpose of the directory is to ensure that the callbacks are properly registered and called, and that the tracers can properly trace the execution of LangChain and record relevant information.

#### chains
The `chains` directory is for unit testing various chain classes and modules, including `APIChain`, `Chain`, `FakeChain`, `ConstitutionalChain`, `ConversationChain`, `HypotheticalDocumentEmbedder`, `LLMChain`, `LLMBashChain`, `LLMCheckerChain`, `LLMMath`, `LLMSummarizationCheckerChain`, `NatBotChain`, `SequentialChain`, `SimpleSequentialChain`, and `TransformChain`. The tests cover functionality such as parsing, error handling, memory usage, and input/output handling. The directory also includes a subdirectory `query_constructor` for testing LLM-generated structured query parsing.

#### chat_models
The `chat_models` directory is for unit tests of the `ChatGooglePalm` class and its helper function `_messages_to_prompt_dict()`. The tests ensure that the function correctly converts a list of messages into a dictionary format expected by the Google PaLM API, and that the `ChatGooglePalm` class raises appropriate errors when given invalid inputs.

#### client
The `client` directory is for unit tests of the LangChainPlusClient class and related functions, including testing link splitting, API key validation, CSV file uploading, message and prompt handling methods, and the `arun_on_dataset` and `run_llm` methods. It also includes tests for the `runner_utils` module's `_get_messages` and `_get_prompts` functions, as well as the `run_llm` function.

#### data
The `data` directory is for storing files and subdirectories related to data used in unit tests. It includes a `prompt_file.txt` file that contains a template for a question and answer prompt, and a `prompts` directory that stores JSON files defining prompts with input variables.

#### docstore
The `docstore` directory is for unit testing the `DocstoreFn` and `InMemoryDocstore` classes. The tests cover scenarios such as finding a document, adding a new document, and handling errors when adding a document with an existing ID.

#### document_loaders
The `document_loaders` directory is for unit tests and example data related to document loaders for various file formats. It includes tests for loading HTML, CSV, Evernote, Telegram, and YouTube documents, as well as tests for detecting file encodings and parsers used in the Langchain codebase. Additionally, the directory contains sample documents and test data for loading documents with different structures and contents.

#### evaluation
The `evaluation` directory is for unit tests of the `QAEvalChain`, `ContextQAEvalChain`, and `CotQAEvalChain` classes in the `langchain.evaluation.qa.eval_chain` module. The tests use the `FakeLLM` class to simulate an LLM and evaluate example queries and predictions. The tests check that the output of the evaluation contains the expected text.

#### examples
The `examples` directory is for storing example files used in unit tests. This includes an example text file with UTF-8 encoding containing special characters and accents.

#### llms
The `llms` directory is for holding all unit tests for LLM objects. It contains test files for base LLM functionality, LLM callbacks, LLM saving and loading functions, and a utility function for removing stop tokens from input text. It also includes two files with classes for a fake chat model and a fake LLM wrapper used for testing purposes.

#### memory
The `memory` directory is for unit tests of the `CombinedMemory` class and different classes that handle chat message histories. The tests ensure that memory variables can be loaded and saved, and chat messages can be added, cleared, and stored across multiple sessions in different storage mediums.

#### output_parsers
The `output_parsers` directory is for unit tests and modules related to parsing output from various sources, including structured output, regular expressions, and Pydantic models. It contains tests for the `BaseOutputParser` class and its subclasses, as well as tests for specific parsers such as `BooleanOutputParser`, `CommaSeparatedListOutputParser`, `RegexDictParser`, and `PydanticOutputParser`. The directory also includes a test for the `CombiningOutputParser` class, which combines the output of multiple parsers.

#### prompts
The `prompts` directory is for unit tests related to prompt functionality. It contains tests for various classes and functions related to prompt templates, including `ChatPromptTemplate`, `FewShotPromptTemplate`, `FewShotPromptWithTemplates`, `LengthBasedExampleSelector`, `load_prompt`, `PromptTemplate`, and `sorted_values`. The tests cover initialization, formatting, and loading of prompt templates, as well as example selection and sorting.

#### retrievers
The `retrievers` directory is for unit testing different retriever classes and their methods such as `TimeWeightedVectorStoreRetriever`, `ZepRetriever`, and `PineconeTranslator`. The tests ensure that the methods return the expected output and contribute to making the codebase easy to understand and navigate.

#### tools
The `tools` directory is for unit testing various tools in the `langchain` library. It includes tests for the `BaseTool` class and its subclasses, `JsonSpec`, `Zapier`, `PythonREPLTool`, `PythonAstREPLTool`, `RequestsGetTool`, `RequestsPostTool`, `RequestsPatchTool`, `RequestsPutTool`, and `RequestsDeleteTool`. The directory also contains subdirectories for testing file management, OpenAPI specifications, PowerBI tools, and shell commands. The tests ensure that the tools perform their intended functions correctly, handle errors appropriately, and validate inputs and outputs.

#### utilities
The `utilities` directory is for unit tests and utility functions related to GraphQL and loading data from a hub path or URL. It includes tests for the `GraphQLAPIWrapper` class and GraphQL utility functions in `graphql.py`, as well as tests for the `try_load_from_hub` function in `loading.py`.

#### vectorstores
The `vectorstores` directory is for unit tests of the `langchain.vectorstores.utils` module's `maximal_marginal_relevance` and `maximal_marginal_relevance_query_dim` functions. The tests cover different scenarios for the functions and use randomly generated and pre-defined vectors to ensure the functions return the expected output.

<!--- END SELFDOC --->