<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `flare` directory is for implementing the Flare chain, which includes a QuestionGeneratorChain, a response chain, a retriever, and an output parser. It uses OpenAI's language model to generate responses and retrieve low-confidence spans. The directory includes initialization files, implementation of the FlareChain class, and prompt templates.

### Files
#### __init__.py
This file is the initialization file for the Flare chain, which is adapted from the FLARE repository.

#### base.py
This file contains the implementation of the FlareChain class, which includes a QuestionGeneratorChain, a response chain, a retriever, and an output parser. It uses OpenAI's language model to generate responses and retrieve low-confidence spans. The file also includes functions for generating responses to user input and extracting tokens and log probabilities.

#### prompts.py
This file contains the `FinishedOutputParser` class which is used to parse the output of a language model. It also contains two prompt templates: `PROMPT` and `QUESTION_GENERATOR_PROMPT` which are used to generate prompts for the user.

<!--- END SELFDOC --->