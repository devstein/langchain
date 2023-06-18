<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `document_compressors` directory is for compressing retrieved documents using various techniques such as LLM chains, Cohere API's `rerank` function, and embeddings. It contains modules such as `__init__.py`, `base.py`, `chain_extract.py`, `chain_extract_prompt.py`, `chain_filter.py`, `chain_filter_prompt.py`, `cohere_rerank.py`, and `embeddings_filter.py`. These modules provide classes and functions for compressing documents based on their relevance to a query context.

### Files
#### base.py
This file defines an abstract base class `BaseDocumentCompressor` and a concrete class `DocumentCompressorPipeline` that implements the `BaseDocumentCompressor` interface. It also contains an async function `acompress_documents` that compresses retrieved documents based on a query context using a pipeline of transformers.

#### chain_extract.py
This file contains the implementation of `LLMChainExtractor`, a class that uses an LLM chain to extract relevant parts of documents. It provides methods to compress page content of raw documents synchronously and asynchronously. The class can be initialized from an LLM using the `from_llm` method.

#### chain_extract_prompt.py
This file contains a Python module `chain_extract_prompt` that defines a `prompt_template` string. The string is a template for a prompt that asks users to extract relevant parts of a given context to answer a question. If none of the context is relevant, a specified string is returned.

#### chain_filter.py
This file implements `LLMChainFilter`, a filter that uses an LLM to compress documents based on their relevance to a query. It provides a `compress_documents` method to filter down documents and a `from_llm` class method to create an instance of `LLMChainFilter` with an `llm_chain` attribute.

#### chain_filter_prompt.py
This file contains a prompt template for a question and context, which asks the user to determine if the context is relevant to the question or not.

#### cohere_rerank.py
This file implements `CohereRerank`, a class that inherits from `BaseDocumentCompressor` and provides a method to compress documents using the Cohere API for re-ranking. It requires a Cohere API key to be set in the environment variable `COHERE_API_KEY`. The `compress_documents` method takes a list of `Document` objects and a query string, and returns a list of compressed `Document` objects with added metadata.

#### embeddings_filter.py
This file implements `EmbeddingsFilter`, a document compressor that filters out irrelevant documents based on their similarity to a query using embeddings. It includes a similarity function and a k value to specify the number of relevant documents to return. The file also contains the `compress_documents` function for filtering documents based on their embeddings and an unimplemented `acompress_documents` function.

<!--- END SELFDOC --->