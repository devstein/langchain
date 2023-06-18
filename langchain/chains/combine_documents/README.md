<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `combine_documents` directory is for combining multiple documents into a single document using different methods such as MapReduce, MapRerank, Refine, and Stuff. It contains abstract base classes, implementation classes, and related functions for each method.

### Files
#### __init__.py
This file serves as the entry point for the `combine_documents` module and provides an overview of the different ways in which documents can be combined.

#### base.py
This file contains the `BaseCombineDocumentsChain` class, which is an abstract base class for chains that combine documents. It also includes a `format_document` function that formats a document into a string based on a prompt template.

#### refine.py
This file contains the implementation of `RefineDocumentsChain` class and related functions, which are used to combine documents by doing a first pass and then refining on more documents using LLM chains. It also defines the configuration for this pydantic object. The file contains private methods for constructing inputs and properties for the `RefineDocumentsChain` class.

#### stuff.py
This file contains the implementation of `StuffDocumentsChain`, a chain that combines documents by stuffing them into context using a specified prompt template. It includes methods to format and join a list of documents into a single string, and to get the prompt length by formatting the prompt. The file also defines the `combine_docs` and `acombine_docs` functions for combining documents and passing them to an LLM for prediction, as well as the `_chain_type` property.

<!--- END SELFDOC --->