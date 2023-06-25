<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `summarize` directory is for summarizing documents using a given language model. It contains functions for loading different types of chains for summarizing documents, as well as prompt templates for generating prompts to write a concise summary of a given text input. The available chain types are "stuff", "map_reduce", and "refine".

### Files
#### __init__.py
This file contains functions for loading different types of chains for summarizing documents using a given language model. The available chain types are "stuff", "map_reduce", and "refine". These functions take in various parameters such as prompts and verbosity, and return the corresponding chain object.

#### map_reduce_prompt.py
This file defines a `PromptTemplate` object that generates a prompt for summarizing text. The prompt asks the user to provide a concise summary of a given text.

#### refine_prompts.py
This file contains the implementation of two PromptTemplate objects: `REFINE_PROMPT` and `PROMPT`. `REFINE_PROMPT` is a prompt for refining an existing summary with additional context, while `PROMPT` is a prompt for writing a concise summary of a given text.

#### stuff_prompt.py
This file defines a `PromptTemplate` class and a `PROMPT` object that prompts the user to write a concise summary of a given text input. The `PromptTemplate` class is imported from `langchain.prompts`.

<!--- END SELFDOC --->