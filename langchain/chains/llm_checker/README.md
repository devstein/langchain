<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `llm_checker` directory is for creating a chain of prompts and assertions to check the validity of a given text using a language model. It includes initialization code, a base class for creating the chain, and prompt templates for creating prompts to check and revise LLMs.

### Files
#### __init__.py
This file contains the initialization code for the `llm_checker` directory, which includes a chain that attempts to verify assumptions before answering a question. The code is heavily borrowed from the `fact-checker` repository on GitHub.

#### base.py
This file defines the `LLMCheckerChain` class, which is used to create a chain of prompts and assertions to check the validity of a given text using a language model. It includes methods for validating inputs, returning input and output keys, and calling the chain with inputs and a callback manager. The class also has a private method for returning the type of chain it is, and a public method for checking the correctness of a given question.

#### prompt.py
This file contains PromptTemplates for creating prompts to check and revise LLMs. It includes prompts for creating a draft answer, listing assumptions made when producing a statement, checking the truth of assertions, and revising an answer based on assertions and checks.

<!--- END SELFDOC --->