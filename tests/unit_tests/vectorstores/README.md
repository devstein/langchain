<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `vectorstores` directory is for unit tests of the `langchain.vectorstores.utils` module's `maximal_marginal_relevance` and `maximal_marginal_relevance_query_dim` functions. The tests cover different scenarios for the functions and use randomly generated and pre-defined vectors to ensure the functions return the expected output.

### Files
#### test_utils.py
This file contains unit tests for the `maximal_marginal_relevance` and `maximal_marginal_relevance_query_dim` functions in the `langchain.vectorstores.utils` module. The tests cover different scenarios for the functions, including when lambda is zero, when lambda is one, and when lambda is a calculated value. The tests use randomly generated and pre-defined vectors to ensure the functions return the expected output. Additionally, the `maximal_marginal_relevance_query_dim` function is tested with random embeddings to ensure consistent results for both 1D and 2D query embeddings.

<!--- END SELFDOC --->