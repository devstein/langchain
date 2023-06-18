<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `react` directory is for implementing the ReAct paper from https://arxiv.org/pdf/2210.03629.pdf. It contains files for interacting with the ReAct chain, including searching and looking up terms in a document store, defining default prompts, and validating required tools. It also includes prompt templates for generating prompts for the TextWorld game and for interacting with Wikipedia.

### Files
#### __init__.py
This file is the initialization file for the `langchain/agents/react` directory. It implements the ReAct paper from https://arxiv.org/pdf/2210.03629.pdf.

#### base.py
This file contains the implementation of various classes for the ReAct chain, including the `ReActDocstoreAgent`, `DocstoreExplorer`, `BaseAgent`, `ReActTextWorldAgent`, and `ReActChain`. These classes provide functionality for interacting with the ReAct chain, including searching and looking up terms in a document store, defining default prompts, and validating required tools.

#### output_parser.py
This file contains the implementation of the ReActOutputParser class, which is a subclass of AgentOutputParser. It defines a parse method that takes in a string of text and returns either an AgentAction or an AgentFinish object depending on the contents of the text. The class also has a private property _type that returns the string "react".

#### textworld_prompt.py
This file defines the `TEXTWORLD_PROMPT` variable, which is a `PromptTemplate` object used for generating prompts for the TextWorld game. It contains a list of example prompts and a suffix, which is appended to the end of each prompt. The prompts are generated using the `from_examples` method of the `PromptTemplate` class.

#### wiki_prompt.py
This file imports the `PromptTemplate` class from `langchain/prompts/prompt.py` module, but does not define any new functionality.

<!--- END SELFDOC --->