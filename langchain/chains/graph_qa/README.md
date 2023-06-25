<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `graph_qa` directory is for question-answering over a knowledge graph. It includes the `GraphQAChain` class for entity extraction and QA, the `GraphCypherQAChain` class for generating Cypher statements and querying a graph database, and prompts for entity extraction, knowledge triplet questions, and generating Cypher statements.

### Files
#### __init__.py
This file contains a brief description of the `graph_qa` directory, which is focused on question answering over a knowledge graph.

#### base.py
This file defines the `GraphQAChain` class, which is a chain for question-answering against a graph. It includes an entity extraction chain and a QA chain, both of which are LLM chains. The class can be initialized from an LLM and includes input and output keys. Additionally, the file contains a function `_call` that extracts entities from a given question, looks up information and answers the question using a QA chain. It also logs the extracted entities and full context using a callback manager.

#### cypher.py
This file contains the `GraphCypherQAChain` class, which generates Cypher statements from questions and schemas, queries a graph database using the statements, and runs a QA chain on the retrieved context to answer the questions.

#### prompts.py
This file contains prompts for entity extraction, knowledge triplet questions, and generating Cypher statements for querying a graph database. The prompts are defined as templates with input variables and instructions for the user to follow.

<!--- END SELFDOC --->