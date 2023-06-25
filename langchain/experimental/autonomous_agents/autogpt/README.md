<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `autogpt` directory is for implementing an autonomous agent that interacts with the Auto-GPT model. It contains files for defining the `AutoGPT` agent, its memory, output parser, prompt, and prompt generator.

### Files
#### prompt.py
This file defines the `AutoGPTPrompt` class, which represents a prompt for a chatbot and has a method to construct a full prompt by concatenating a prompt start, a list of goals, and a prompt generated by the `get_prompt` function from `prompt_generator.py`. The class also inherits from `BaseChatPromptTemplate`.

#### prompt_generator.py
This file contains the `PromptGenerator` class, which generates custom prompt strings for autonomous agents based on constraints, commands, resources, and performance evaluations. It includes methods to add constraints, tools, and resources, and a response format dictionary that specifies the format of the generated prompt.

<!--- END SELFDOC --->