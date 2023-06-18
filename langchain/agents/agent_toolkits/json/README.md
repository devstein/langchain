<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `json` directory is for creating and interacting with a JSON agent toolkit. It includes files for initializing the toolkit, creating a JSON agent, defining prompts for interacting with JSON, and implementing a `JsonToolkit` class for interacting with a JSON spec.

### Files
#### __init__.py
This file is the initialization file for the `json` agent toolkit in the `langchain/agents/agent_toolkits` directory.

#### base.py
This file defines a function `create_json_agent` that constructs a JSON agent from a language model and tools. The function creates a prompt for the agent, constructs an LLMChain, and returns an AgentExecutor.

#### prompt.py
This file contains a constant string `JSON_PREFIX` and `JSON_SUFFIX` which are prompts for an agent designed to interact with JSON. The prompts provide instructions on how to interact with the JSON and what tools to use. The prompts also provide guidance on how to handle certain errors and what to do if the question is not related to the JSON.

#### toolkit.py
This file contains the implementation of the `JsonToolkit` class, which is a toolkit for interacting with a JSON spec. It includes methods for getting the tools in the toolkit, such as `JsonListKeysTool` and `JsonGetValueTool`.

<!--- END SELFDOC --->