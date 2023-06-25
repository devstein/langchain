<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `output_parsers` directory is for parsing the output of an LLM call into various formats. It includes classes for parsing output into boolean values, lists, Pydantic models, and dictionaries using regular expressions. It also includes classes for combining parsers, fixing parsing errors, and retrying parsing with prompts. Additionally, the directory contains files with format instructions and a function for loading output parsers based on configuration.

### Files
#### __init__.py
This file is the package initializer for the `langchain/output_parsers` directory. It imports and exports various output parsers, including `RegexParser`, `StructuredOutputParser`, and `PydanticOutputParser`.

#### boolean.py
This file contains the `BooleanOutputParser` class, which is a subclass of `BaseOutputParser`. It defines a `parse` method that takes in text and returns a boolean value based on whether the text matches the `true_val` or `false_val` attributes of the class. It also has a `_type` property that returns a string identifier for the output parser type.

#### combining.py
This file contains the `CombiningOutputParser` class which allows multiple output parsers to be combined into one. It validates the parsers and provides instructions on how the LLM output should be formatted. It also has a `parse` method to parse the output of an LLM call.

#### fix.py
This file contains the implementation of `OutputFixingParser`, which wraps a parser and tries to fix parsing errors. It uses an LLMChain to generate a new completion when an error occurs and then attempts to parse the new completion. It also provides methods to get format instructions and the type of the parser.

#### format_instructions.py
This file contains two string variables that provide instructions for formatting output in the `langchain/output_parsers` directory. The first variable provides instructions for formatting output as a markdown code snippet, while the second variable provides instructions for formatting output as a JSON instance that conforms to a specific schema.

#### list.py
This file contains the `ListOutputParser` class, which is used to parse the output of an LLM call to a list. It also contains the `CommaSeparatedListOutputParser` class, which is a subclass of `ListOutputParser` and is used to parse comma-separated lists.

#### regex_dict.py
This file contains the implementation of `RegexDictParser` class which is used to parse the output of an LLM call into a dictionary using regular expressions. It defines a `parse` method that takes in the output text and returns a dictionary with the parsed values. The class also has an `output_key_to_format` attribute which is a dictionary mapping output keys to their expected format.

#### retry.py
This file contains the implementation of `RetryOutputParser` and `RetryWithErrorOutputParser`, which are wrappers around other output parsers that try to fix parsing errors by passing the original prompt, completion, and error to another language model. They differ in the information provided to the LLM. The file also contains the implementation of `parse_with_prompt` and `get_format_instructions` methods.

#### structured.py
This file contains a `StructuredOutputParser` class that inherits from `BaseOutputParser`. It defines a method `parse_json_markdown` that takes in a string of JSON and a list of expected keys, and returns the parsed JSON object if all expected keys are present. The class also has a method `get_format_instructions` that returns a string of format instructions based on the `response_schemas` attribute of the class. Additionally, it has a `_type` property that returns the string "structured".

<!--- END SELFDOC --->