<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `memory` directory is for storing various classes and modules related to conversation memory in the `langchain` package. It includes classes for storing conversation history, entities, knowledge graphs, and summaries, as well as implementations for different types of memory, such as read-only memory, Motorhead memory, and simple memory. Additionally, it contains prompt templates, validators, and utility functions for formatting and managing memory variables.

### Files
#### __init__.py
This file imports and lists memory-related classes and modules within the `langchain.memory` package.

#### combined.py
This file contains the implementation of `CombinedMemory` class, which allows for combining multiple memories' data together. It provides a `memory_variables` property that returns all the memory variables from linked memories and has validators to check for repeated memory variables and input keys. Additionally, it includes functions to load and save variables from sub-memories, as well as clear context from a session for every memory.

#### entity.py
This file defines abstract and concrete classes for storing and managing entities, including an in-memory implementation and a Redis-backed implementation with default TTL. It also includes an entity extractor and summarizer to memory, as well as methods for loading memory variables and saving context to the conversation buffer. Additionally, it provides functionality for caching and predicting entity summaries through an entity cache and store.

#### kg.py
This file contains the `ConversationKGMemory` class, which integrates with an external knowledge graph to store and retrieve information about knowledge triples in a conversation. It includes methods for retrieving the history buffer and managing conversation memory.

#### motorhead_memory.py
This file contains the implementation of `MotorheadMemory` class, which is a chat memory that connects to a Motorhead server. It provides methods to initialize the memory, load memory variables, and save context. It inherits from `BaseChatMemory` and uses the `requests` library to interact with the Motorhead server.

#### summary.py
This file contains a class that summarizes conversations and stores the summary in memory. It also provides methods to validate input variables, save context, and clear the memory contents.

#### summary_buffer.py
This file contains the `ConversationSummaryBufferMemory` class, which implements a summary buffer for chat conversations. It provides methods to save context from a conversation to the buffer, prune the buffer if it exceeds a maximum token limit, and clear the memory contents. The class also has a `validate_prompt_input_variables` method that validates that prompt input variables are consistent.

#### token_buffer.py
This file contains the `ConversationTokenBufferMemory` class, which is a buffer for storing conversation memory. It has methods for loading and saving memory variables, and for pruning the buffer if it exceeds a maximum token limit.

#### utils.py
This file contains a function `get_prompt_input_key` that takes in a dictionary of inputs and a list of memory variables, and returns a string representing the key for the input that will be used to format the prompt. The function raises a `ValueError` if there is not exactly one input key that is not a memory variable or the string "stop".

#### vectorstore.py
This file contains a vector store implementation for storing and retrieving conversation context. It includes methods for formatting, saving, and clearing context from a conversation buffer.

### Directories
#### chat_message_histories
The `chat_message_histories` directory is for storing various implementations of chat message history classes. These classes include Cassandra, Cosmos DB, DynamoDB, file-based, Firestore, PostgreSQL, Redis, SQL, and Zep. Each file contains the implementation of the respective class, including functions to interact with the database or file system to store and retrieve chat messages, as well as methods to clear session memory.

<!--- END SELFDOC --->