<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `mrkl` directory is for implementing MRKL systems as described in a specific research paper. It includes the implementation of the MRKLChain agent and related classes, a parser for the MRKL agent output, and a module for generating prompts for user input.

### Files
#### __init__.py
This file contains the initialization code for the `langchain/agents/mrkl` directory. It includes a brief description of the purpose of the directory, which is to implement MRKL systems as described in a specific research paper.

#### base.py
This file contains the implementation of the MRKLChain agent and related classes, used for building applications with LLMs through composability. It includes methods for creating prompts, initializing the MRKL chain, and constructing an agent from a language model and tools.

#### output_parser.py
This file defines the `MRKLOutputParser` class, which is responsible for parsing the output of the MRKL agent. It provides a `parse` method that extracts the action and input from the agent's output, and returns an `AgentAction` object. If the output contains a final answer, it returns an `AgentFinish` object instead. The class also defines a `_type` property that identifies it as the output parser for the MRKL agent.

#### prompt.py
This file contains a Python module `prompt` which defines three string constants: `PREFIX`, `FORMAT_INSTRUCTIONS`, and `SUFFIX`. These strings are used to generate a prompt for a user to answer a question using a set of tools. The prompt includes instructions on how to format the answer.

<!--- END SELFDOC --->