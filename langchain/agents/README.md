<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `agents` directory is for creating and executing agents, loading and initializing agents, and working with conversational and structured chat agents. It includes subdirectories for different types of agents, such as conversational, structured chat, and MRKL agents, as well as toolkits for different agents, such as CSV, file management, and Python. The directory also contains files for defining agent types, validating tools, and exporting various agents and agent-related tools.

### Files
#### agent.py
This file contains an abstract base class and several subclasses for agents, which are responsible for executing a sequence of actions defined in a toolchain. The `Agent` class includes methods for looking up tools, deciding what action to take based on input, and returning input and output keys. It also includes a method that iteratively executes the actions in the toolchain until a stopping condition is met, and a method that runs text through the agent and returns the agent's response.

#### agent_types.py
This file defines an `AgentType` enum class with several predefined agent types as string values. These agent types are used to identify and differentiate between different types of agents used in the langchain application.

#### load_tools.py
This file contains functions that define and load various tools used by the langchain agents, including search engines, APIs, and tools for making HTTP requests and running language models. The tools are loaded based on their name and can be either base tools, LLM tools, extra LLM tools, or extra optional tools. A dictionary of optional tools is also defined, and a warning is issued for the use of the "requests" tool. Additionally, a function is provided to retrieve a list of all possible tool names.

#### loading.py
This file contains functions for loading agents from a configuration dictionary, a language model, and a list of tools. It includes methods for loading agents from LangChainHub or from the local file system, and for loading agents from a JSON or YAML file. The loaded agent is returned as a `BaseSingleActionAgent`.

### Directories
#### agent_toolkits
The `agent_toolkits` directory is for providing a collection of toolkits for different agents, including CSV, file management, Gmail, Jira, JSON, NLA, OpenAPI, Pandas, PlayWright browser automation, PowerBI, Python, Spark, Spark SQL, SQL database, VectorStore, and Zapier. Each subdirectory contains files for initializing the toolkit, creating an agent, providing prompts and instructions, and defining the tools in the toolkit.

#### chat
The `chat` directory is for implementing the chat agent functionality. It contains files that define the `ChatAgent` class, the `ChatOutputParser` class, and constants used in the chat agent's prompt message. The `ChatAgent` class has methods for constructing a scratchpad, defining prefixes for observations and LLM calls, and creating prompts and validating tools. The `ChatOutputParser` class is responsible for parsing the output of the chat agent.

#### conversational
The `conversational` directory is for creating conversational agents that can hold a conversation and use tools. It contains files that define the `ConversationalAgent` and `BaseAgent` classes, a module for parsing the output of the agent, and a module that defines text used by the agent to introduce itself and provide instructions.

#### conversational_chat
The `conversational_chat` directory is for implementing a conversational chat agent that can hold a conversation and use tools. It includes files for defining the `ConversationalChatAgent` class, implementing the `ConvoOutputParser` class for parsing agent output, and defining string constants used in the agent.

#### mrkl
The `mrkl` directory is for implementing MRKL systems as described in a specific research paper. It includes the implementation of the MRKLChain agent and related classes, a parser for the MRKL agent output, and a module for generating prompts for user input.

#### react
The `react` directory is for implementing the ReAct paper from https://arxiv.org/pdf/2210.03629.pdf. It contains files for interacting with the ReAct chain, including searching and looking up terms in a document store, defining default prompts, and validating required tools. It also includes prompt templates for generating prompts for the TextWorld game and for interacting with Wikipedia.

#### self_ask_with_search
The `self_ask_with_search` directory is for implementing self-asking functionality with search in LangChain agents. It contains files for initializing the directory, defining classes for self-asking with search, parsing the output of the self-ask agent, and providing a default template for a prompt that asks a question and provides follow-up questions to arrive at a final answer.

#### structured_chat
The `structured_chat` directory is for implementing a structured chat agent that can parse and respond to user input in a structured format. It includes files for defining the `StructuredChatAgent` class, implementing the `StructuredChatOutputParser` class for parsing agent output, and defining prompts for the agent.

<!--- END SELFDOC --->