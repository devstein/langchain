<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `llm_math` directory is for a chain that interprets prompts and executes Python code to perform mathematical operations. It contains files for initializing the directory, defining the `LLMMathChain` class, and generating prompts for math problems.

### Files
#### __init__.py
This file contains the initialization code for the `llm_math` directory, which provides a chain for interpreting prompts and executing Python code to perform mathematical operations. The code in this file is based on a similar implementation found at https://replit.com/@amasad/gptpy?v=1#main.py.

#### base.py
This file defines the `LLMMathChain` class, which is a chain that interprets a prompt and executes Python code to do math. It includes methods for evaluating mathematical expressions and processing LLM output. The class also has an asynchronous function for calling the LLM model and a class method for creating an instance of the LLMMathChain class from a given language model.

#### prompt.py
This file contains the `PROMPT` variable which is a `PromptTemplate` object used to generate prompts for math problems. It takes in a question as an input variable and outputs a single line mathematical expression that solves the problem using Python's numexpr library. The output of running the code and the answer are also included in the prompt.

<!--- END SELFDOC --->