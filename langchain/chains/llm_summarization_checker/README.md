<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `llm_summarization_checker` directory is for checking the accuracy of text generation by splitting it into a list of facts, checking their truthfulness, and rewriting the text to make it more accurate. It contains an initialization file, a base file defining the `LLMSummarizationCheckerChain` class, and a `prompts` directory for storing prompts related to fact-checking and summarization.

### Files
#### __init__.py
This file contains the `llm_summarization_checker` package's initialization code. The package provides a chain that verifies the accuracy of text generation by splitting it into a list of facts, checking their truthfulness, and rewriting the text to make it more accurate. The chain repeats this process until it reaches a "true" output or hits the maximum number of tries.

#### base.py
This file defines the `LLMSummarizationCheckerChain` class for checking the summarization of a given input text using a Language Model. It contains methods for creating and checking assertions, revising summaries, and checking if all assertions are true. It also contains a `_load_sequential_chain` function for creating a sequential chain of LLMChain objects for summarization checking.

### Directories
#### prompts
The `prompts` directory is for storing prompts for various tasks related to fact-checking and summarization. These prompts include creating a bulleted list of facts, checking the truthfulness of facts, revising a summary, and checking if all assertions are true.

<!--- END SELFDOC --->