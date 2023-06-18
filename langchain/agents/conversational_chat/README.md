<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `conversational_chat` directory is for implementing a conversational chat agent that can hold a conversation and use tools. It includes files for defining the `ConversationalChatAgent` class, implementing the `ConvoOutputParser` class for parsing agent output, and defining string constants used in the agent.

### Files
#### __init__.py
This file contains a brief description of the `conversational_chat` agent, which is designed to hold a conversation and use tools.

#### base.py
This file defines the `ConversationalChatAgent` class, which includes an output parser, a default output parser, and methods to validate tools. It also contains methods for creating a prompt template and constructing a scratchpad for the agent to continue its thought process. Additionally, it includes a `from_llm_and_tools` method that constructs an agent from a BaseLanguageModel and a sequence of BaseTools, with optional parameters for a BaseCallbackManager, AgentOutputParser, system and human messages, and input variables.

#### output_parser.py
This file contains the implementation of `ConvoOutputParser`, a class that inherits from `AgentOutputParser` and provides methods to parse and format the output of a conversational chat agent. The `parse` method cleans the output text and extracts the action and action input from a JSON response, returning either an `AgentAction` or `AgentFinish` object.

<!--- END SELFDOC --->