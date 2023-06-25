<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `python` directory is for implementing a Python agent that can be constructed from a BaseLanguageModel and a PythonREPLTool. It contains the implementation of the ZeroShotAgent class, the LLMChain class, and the AgentExecutor class used to execute the agent. Additionally, the directory contains a function `create_python_agent` that constructs the agent. The `prompt.py` file in the directory contains a constant variable `PREFIX` which provides instructions for an agent designed to write and execute Python code to answer questions.

### Files
#### base.py
This file contains the implementation of a Python agent that can be constructed from a BaseLanguageModel and a PythonREPLTool. The agent is created using the ZeroShotAgent class and the LLMChain class, and the AgentExecutor class is used to execute the agent. The file also contains a function `create_python_agent` that constructs the agent.

#### prompt.py
This file contains a constant variable `PREFIX` which is a multi-line string. The string provides instructions for an agent designed to write and execute Python code to answer questions. The instructions include guidelines for using a Python REPL and debugging code.

<!--- END SELFDOC --->