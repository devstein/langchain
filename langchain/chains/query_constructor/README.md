<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `query_constructor` directory is for constructing structured queries using a query language parser and a prompt module. It includes files for parsing user input into a query object, defining the internal representation of a structured query language, generating a prompt for constructing a query, and defining a model for attribute information.

### Files
#### base.py
This file defines a class `StructuredQueryOutputParser` that parses a string of text and returns a structured representation of the query language. It also includes helper functions for formatting attribute information and getting a prompt with allowed comparators and operators. Additionally, it contains a function `load_query_constructor_chain` that loads a language model chain for constructing queries.

#### ir.py
This file defines the internal representation of a structured query language. It includes classes for defining a visitor interface, expressions, operators, comparators, and filtering directives. It also includes classes for defining comparisons, operations, and structured queries.

#### parser.py
This file `parser.py` contains a Lark grammar for parsing a query string into an intermediate representation (IR) of filter directives, comparisons, and operations. The `QueryTransformer` class is used to transform the parsed Lark tree into the IR. The `allowed_comparators` and `allowed_operators` arguments can be used to restrict the set of comparators and operators that can be used in the query string.

<!--- END SELFDOC --->