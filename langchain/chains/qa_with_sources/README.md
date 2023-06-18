<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `qa_with_sources` directory is for implementing question answering with sources over documents or indexes. It includes an abstract base class for defining the structure of the chain, functions to load different types of chains, and implementations of prompt templates for refining existing answers and answering questions based on context information. It also includes classes for retrieving relevant documents from an index or vector database based on similarity search.

### Files
#### base.py
This file defines an abstract base class `BaseQAWithSourcesChain` for question answering with sources over documents. It includes a chain to combine documents, and defines keys for question, input documents, answer, and sources answer. It also has an option to return the source documents. The file also contains the implementation of the `QAWithSourcesChain` class, which inherits from `BaseQAWithSourcesChain` and defines methods for getting input documents and running the chain to return the answer with its sources.

#### loading.py
This file contains functions to load different types of chains used in question answering with sources tasks. These functions take in a language model and other optional arguments to customize the chain, and return the corresponding chain object.

#### map_reduce_prompt.py
This file (`map_reduce_prompt.py`) contains code for mapping and reducing prompts for the QA_with_sources module. It includes functions for mapping prompts to their corresponding sources and reducing the mapped prompts to a single prompt. The file also provides `PromptTemplate` classes for generating GPT-3 prompts used in the QA with sources pipeline.

#### refine_prompts.py
This file contains the implementation of default prompt templates for refining existing answers and answering questions based on context information. It also includes an example prompt template for displaying content and its source.

#### retrieval.py
This file contains the implementation of a question-answering with sources over an index. It defines a class `RetrievalQAWithSourcesChain` that inherits from `BaseQAWithSourcesChain`. It includes methods to get relevant documents from an index and reduce the number of results based on a token limit.

#### stuff_prompt.py
This file contains a `PromptTemplate` function for generating a prompt with references given extracted parts of a long document and a question. The prompt includes a "SOURCES" part and if the answer is unknown, it is stated as such.

#### vector_db.py
This file contains the implementation of `VectorDBQAWithSourcesChain` class which is used for question-answering with sources over a vector database. It includes methods to get documents based on similarity search using a vector store, and parameters such as `vectorstore`, `k`, `reduce_k_below_max_tokens`, `max_tokens_limit`, and `search_kwargs`. The class also includes a method `_reduce_tokens_below_limit` which reduces the number of results to return from the store based on the tokens limit. Additionally, it has a root validator to raise a deprecation warning and a property to return the chain type.

<!--- END SELFDOC --->