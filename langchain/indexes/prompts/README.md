<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `prompts` directory is for providing prompt templates and implementations for constructing indexes. It includes prompts for entity extraction, entity summarization, and knowledge triplet extraction.

### Files
#### __init__.py
This file contains a brief module-level documentation for the `langchain/indexes/prompts` directory, which provides relevant prompts for constructing indexes.

#### entity_extraction.py
This file contains the implementation of a prompt for entity extraction. The prompt provides an AI assistant with a conversation history and the last line of conversation between an AI and a human. The AI assistant is expected to extract all proper nouns from the last line of conversation and return them as a single comma-separated list.

#### entity_summarization.py
This file contains the `ENTITY_SUMMARIZATION_PROMPT` which is a default prompt template for entity summarization. It provides instructions for an AI assistant to update the summary of a provided entity based on the last line of conversation with a human. The prompt includes the conversation history, the entity to summarize, the existing summary, and the last line of conversation.

#### knowledge_triplet_extraction.py
This file contains the `KNOWLEDGE_TRIPLE_EXTRACTION_PROMPT` which is a prompt template for extracting knowledge triples from text. The template includes examples of what a knowledge triple is and how to extract them from text. The `PromptTemplate` takes in an input variable `text` and outputs the extracted knowledge triples.

<!--- END SELFDOC --->