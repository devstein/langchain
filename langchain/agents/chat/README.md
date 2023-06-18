<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `chat` directory is for implementing the chat agent functionality. It contains files that define the `ChatAgent` class, the `ChatOutputParser` class, and constants used in the chat agent's prompt message. The `ChatAgent` class has methods for constructing a scratchpad, defining prefixes for observations and LLM calls, and creating prompts and validating tools. The `ChatOutputParser` class is responsible for parsing the output of the chat agent.

### Files
#### base.py
This file defines the `ChatAgent` class, which contains methods for constructing a scratchpad, defining prefixes for observations and LLM calls, and getting the default output parser. It also imports various modules and classes from other files in the `langchain/agents/chat` directory. Additionally, it has a method for creating prompts and validating tools, as well as a property that raises a ValueError.

#### output_parser.py
This file contains the implementation of the `ChatOutputParser` class, which is responsible for parsing the output of the chat agent. It provides a `parse` method that takes in a string of text and returns either an `AgentAction` or an `AgentFinish` object, depending on the content of the text. The class also defines a constant `FINAL_ANSWER_ACTION` and a `get_format_instructions` method.

#### prompt.py
This file contains a Python module that defines three constants: PREFIX, FORMAT_INSTRUCTIONS, and SUFFIX. These constants are used to provide instructions and guidelines for using the tools available in the chat agent. The instructions include specifying a JSON blob with an action and action_input key, and always using the exact characters "Final Answer" when responding.

<!--- END SELFDOC --->