<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `prompts` directory is for creating and formatting prompt templates for LLMs. It includes classes for string prompts, chat prompts, and few-shot prompts, as well as functions for loading prompts and prompt templates from a configuration dictionary or file system. The `example_selector` subdirectory contains classes for selecting examples to include in prompts based on length, ngram overlap score, and semantic similarity.

### Files
#### __init__.py
This file imports and exports various prompt template classes from other files in the `langchain/prompts` directory, including `BasePromptTemplate`, `StringPromptTemplate`, `FewShotPromptTemplate`, and `Prompt`.

#### base.py
This file defines the `BasePrompt` schema and contains utility functions for formatting prompts using either f-strings or jinja2. It also includes a function for validating jinja2 templates.

#### chat.py
This file contains various message prompt templates for chat applications, including abstract base classes and subclasses. It also includes a class for representing a list of messages and methods for formatting chat messages and input variables into a chat prompt.

#### few_shot.py
This file contains the `FewShotPromptTemplate` class, which is a prompt template that contains few shot examples. It allows for either a list of examples or an `ExampleSelector` to be provided, and formats them using an individual example prompt template. The file also includes a validator to ensure that only one of `examples` and `example_selector` is provided.

#### loading.py
This file contains functions for loading prompts and prompt templates from a configuration dictionary or file system. It includes a dictionary to map prompt types to their respective loaders and can load prompts in JSON, YAML, or Python format.

#### prompt.py
This file contains the `PromptTemplate` class, which represents a prompt for an LLM and includes expected input variables, the prompt template, and the format of the prompt template. It has class methods for generating a prompt template from examples or loading a prompt from a file, and a root validator method for consistency checking. There is also a backwards compatibility alias for `PromptTemplate` called `Prompt`.

### Directories
#### example_selector
The `example_selector` directory is for selecting examples to include in prompts. It contains implementation files for three classes: `LengthBasedExampleSelector`, `SemanticSimilarityExampleSelector`, and `MaxMarginalRelevanceExampleSelector`. It also includes an abstract base class `BaseExampleSelector` and implementation files for `NGramOverlapExampleSelector` and `SemanticSimilarityExampleSelector` classes. These classes use different algorithms to select and order examples based on length, ngram overlap score, and semantic similarity.

<!--- END SELFDOC --->