<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `structured_chat` directory is for implementing a structured chat agent that can parse and respond to user input in a structured format. It includes files for defining the `StructuredChatAgent` class, implementing the `StructuredChatOutputParser` class for parsing agent output, and defining prompts for the agent.

### Files
#### base.py
This file defines the `StructuredChatAgent` class, which contains methods for constructing a scratchpad, validating tools, and defining prefixes for observations and LLM calls. It also imports various modules and classes, including `AgentOutputParser`, `StructuredChatOutputParserWithRetries`, and `BaseTool`. The class is used for creating a Structured Chat agent from a BaseLanguageModel and a sequence of BaseTools.

<!--- END SELFDOC --->