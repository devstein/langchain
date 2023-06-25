<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `natbot` directory is for implementing a GPT-3 driven browser through composability. It includes a base implementation for the NatBot chain, a `Crawler` class for retrieving information about a webpage's elements, and a prompt template and module for a natural language bot that controls a browser.

### Files
#### __init__.py
This file contains a brief description of the `natbot` directory and its purpose, which is to implement a GPT-3 driven browser. It also mentions that the implementation is heavily influenced by a similar project on GitHub.

#### base.py
This file contains the implementation of the `NatBotChain` class, which provides a base implementation for the NatBot chain. It includes methods to load the chain from a default LLMChain or from a given LLM, as well as a method to execute the chain and return the next browser command to run. Additionally, it contains a root validator that raises a warning if the `llm` attribute is used directly.

#### crawler.py
This file (`crawler.py`) defines a `Crawler` class that uses Playwright to retrieve information about a webpage's elements. It includes methods for loading a page, checking if elements are in the viewport, and maintaining a blacklist.

#### prompt.py
This file contains a prompt template and module for a natural language bot that controls a browser. It provides a list of available commands, a simplified format for interactive elements, and allows users to interact with a browser through the command line to achieve a specific objective. The `PromptTemplate` class creates a prompt for user input based on the current browser content, objective, current URL, and previous command.

<!--- END SELFDOC --->