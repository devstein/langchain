<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `conversational` directory is for creating conversational agents that can hold a conversation and use tools. It contains files that define the `ConversationalAgent` and `BaseAgent` classes, a module for parsing the output of the agent, and a module that defines text used by the agent to introduce itself and provide instructions.

### Files
#### __init__.py
This file contains the package initializer for the `conversational` module, which defines an agent capable of holding a conversation and using tools.

#### base.py
This file contains the implementation of `ConversationalAgent`, `BaseAgent` class, and a class method `from_llm_and_tools`. These classes provide a template for creating conversational agents, with methods for creating a prompt, validating tools, and constructing an agent from a given language model and tools.

#### output_parser.py
This file contains the implementation of the `ConvoOutputParser` class, which is responsible for parsing the output of the conversational agent. It defines a `parse` method that takes in a string of text and returns either an `AgentAction` or `AgentFinish` object based on the format of the input. It also defines a `_type` property that returns the string "conversational".

#### prompt.py
This file contains a Python module that defines three string variables: PREFIX, FORMAT_INSTRUCTIONS, and SUFFIX. These variables contain text that is used by the conversational agent to introduce itself, provide instructions on how to use its tools, and format the output of its conversations.

<!--- END SELFDOC --->