<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `self_ask_with_search` directory is for implementing self-asking functionality with search in LangChain agents. It contains files for initializing the directory, defining classes for self-asking with search, parsing the output of the self-ask agent, and providing a default template for a prompt that asks a question and provides follow-up questions to arrive at a final answer.

### Files
#### base.py
This file defines the `SelfAskWithSearchAgent` and `SelfAskWithSearchChain` classes for performing self-asking with search. It imports and uses several modules such as `Agent`, `AgentExecutor`, `AgentOutputParser`, `BaseLanguageModel`, `BasePromptTemplate`, `BaseTool`, `GoogleSerperAPIWrapper`, `SerpAPIWrapper`, `SelfAskOutputParser`, `PROMPT`, `Tool`, and `validate_tools_single_input`. The classes are initialized with a language model and a search chain, and provide methods for creating prompts and validating tools.

#### output_parser.py
This file contains the implementation of the `SelfAskOutputParser` class, which is responsible for parsing the output of the `SelfAskWithSearchAgent`. The `parse` method takes in a string of text and returns either an `AgentAction` or an `AgentFinish` object depending on the contents of the text. If the text contains an intermediate answer, an `AgentAction` object is returned, otherwise an `AgentFinish` object is returned with the final answer.

#### prompt.py
This file contains a default template for a prompt that asks a question and provides follow-up questions to arrive at a final answer. The template includes examples of questions and follow-up questions with their intermediate answers. The `PromptTemplate` class takes in input variables and the default template to generate a prompt.

<!--- END SELFDOC --->