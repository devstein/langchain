<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `chains` directory is for unit testing various chain classes and modules, including `APIChain`, `Chain`, `FakeChain`, `ConstitutionalChain`, `ConversationChain`, `HypotheticalDocumentEmbedder`, `LLMChain`, `LLMBashChain`, `LLMCheckerChain`, `LLMMath`, `LLMSummarizationCheckerChain`, `NatBotChain`, `SequentialChain`, `SimpleSequentialChain`, and `TransformChain`. The tests cover functionality such as parsing, error handling, memory usage, and input/output handling. The directory also includes a subdirectory `query_constructor` for testing LLM-generated structured query parsing.

### Directories
#### query_constructor
The `query_constructor` directory is for unit testing the LLM-generated structured query parsing. It includes tests for parsing invalid grammar, comparison, and operation, as well as nested operations and different types of values such as integers, floats, lists, and strings. It also contains a unit test for the `parse_bool_value` function in the `query_constructor` module.

<!--- END SELFDOC --->