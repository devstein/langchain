<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `question_answering` directory is for loading various chains and generating prompts to extract relevant text from a long document to answer a given question using a map-reduce process. It also includes prompt templates for refining an existing answer to better answer a question in question answering models and for answering questions based on given context.

### Files
#### __init__.py
This file contains functions for loading various chains used for question answering. These chains include MapRerankDocumentsChain, StuffDocumentsChain, MapReduceDocumentsChain, refine documents chain, and question answering chain. The functions take in a language model, prompt, and other optional arguments to create and configure the chains.

#### map_reduce_prompt.py
This file contains code for generating prompts to extract relevant text from a long document to answer a given question using a map-reduce process. It includes prompt templates for the question and human interaction, and a function that uses a GPT-3 model to generate responses.

#### map_rerank_prompt.py
This file contains a prompt template for generating a question answering prompt. The prompt asks the user to provide an answer and a score between 0 and 100 based on a given context and question. The file also includes an output parser for extracting the answer and score from the user's response.

#### refine_prompts.py
This file contains prompt templates and a prompt selector for refining an existing answer to better answer a question in question answering models. It includes a default text prompt template and a chat prompt template, and the prompt selector chooses between them based on the model type.

#### stuff_prompt.py
This file defines a prompt template and a chat prompt template for answering questions based on given context. It also defines a prompt selector that selects the appropriate prompt based on the model type.

<!--- END SELFDOC --->