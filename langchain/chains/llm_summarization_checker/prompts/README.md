<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `prompts` directory is for storing prompts for various tasks related to fact-checking and summarization. These prompts include creating a bulleted list of facts, checking the truthfulness of facts, revising a summary, and checking if all assertions are true.

### Files
#### are_all_true_prompt.txt
This file contains a prompt for a function that takes in a string of checked assertions labeled as true or false and returns "True" if all assertions are true and "False" if any assertion is false. The file includes examples of input and output.

#### check_facts.txt
This file contains a prompt for a fact-checking task. The prompt provides a list of facts and requires the user to determine whether each fact is true or false about the subject, with an option to output "Undetermined" if unsure. If the fact is false, the user is required to explain why.

#### create_facts.txt
This file contains a prompt for creating a bulleted list of facts from a given text. The text is provided in a specific format and the output should also be formatted as a bulleted list.

#### revise_summary.txt
This file contains a prompt for revising a summary based on checked assertions. It includes a list of checked assertions labeled as true or false, an original summary, and instructions to use the checked assertions to rewrite the summary to be completely true.

<!--- END SELFDOC --->