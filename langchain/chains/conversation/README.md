<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `conversation` directory is for carrying on a conversation and calling an LLM. It includes memory modules for conversation prompts and defines a default conversation prompt template for an AI chatbot.

### Files
#### __init__.py
This file is the entry point for the `conversation` module and provides a brief description of the module's purpose.

#### base.py
This file contains the `ConversationChain` class, which carries on a conversation and calls an LLM. It also defines the `input_key` and `output_key` properties, and includes a function to validate prompt input variables.

#### memory.py
This file exports various memory modules for conversation prompts, including buffer, buffer window, entity, knowledge graph, and summary memories. It also includes a combined memory module for all of these memories.

#### prompt.py
This file defines a default conversation prompt template for an AI chatbot. It imports prompt templates from `langchain.memory.prompt` and `langchain.prompts.prompt` modules and sets a default template for the conversation history and input. It also exports a list of prompt templates for backwards compatibility.

<!--- END SELFDOC --->