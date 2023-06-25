<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `retrieval_qa` directory is for building retrieval-based question-answering systems against a vector database. It contains an initialization file, a file with multiple classes for building QA systems, and a file defining a `PromptTemplate` class for generating prompts.

### Files
#### __init__.py
This file contains the initialization code for the retrieval_qa directory, which is a chain used for question-answering against a vector database.

#### base.py
This file contains multiple classes for building retrieval-based question-answering systems, including the `BaseRetrievalQA`, `RetrievalQA`, and `VectorDBQA` classes. These classes provide methods for retrieving relevant documents and running the QA system on input queries. The `VectorDBQA` class is deprecated in favor of `RetrievalQA`.

#### prompt.py
This file defines a `PromptTemplate` class that generates a prompt for a question-answering task. The prompt includes a context section and a question section, and is generated using a template string. The `PromptTemplate` class takes in a template string and a list of input variables, and generates a prompt by substituting the input variables into the template string.

<!--- END SELFDOC --->