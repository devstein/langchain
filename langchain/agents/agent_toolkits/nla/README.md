<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `nla` directory is for implementing natural language interaction with APIs through the `NLATool` and `NLAToolkit` classes in `tool.py` and `toolkit.py`, respectively. These classes provide tools for creating instances of the toolkit and interacting with APIs using natural language.

### Files
#### tool.py
This file contains the implementation of the `NLATool` class, which is a tool for interacting with a single API using natural language. It provides two class methods for creating an instance of the tool, one from an OpenAPI endpoint chain and the other from a specified path and method. The tool can be used to assist with an API via natural language.

#### toolkit.py
This file defines the `NLAToolkit` class, which is a toolkit for interacting with APIs using natural language. It contains a list of API endpoint tools and a method to get the tools for all the API operations. The `_get_http_operation_tools` method returns a list of `NLATool` objects for each API operation.

<!--- END SELFDOC --->