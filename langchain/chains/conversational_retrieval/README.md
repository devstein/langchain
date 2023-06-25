<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `conversational_retrieval` directory is for implementing a conversational retrieval chain that allows for chatting with a vector database. It includes an initialization file, a base class for conversational retrieval chains, and a prompts file for generating prompts.

### Files
#### __init__.py
This file contains the initialization code for the conversational retrieval chain, which allows for chatting with a vector database.

#### base.py
This file defines the `BaseConversationalRetrievalChain` class, which serves as a base class for conversational retrieval chains. It includes methods for retrieving documents based on a question, loading chains from a language model, and reducing the number of tokens in the documents. Additionally, it contains the implementation of the `ConversationalRetrievalChain` class, which is a chain for chatting with an index.

#### prompts.py
This file contains two PromptTemplate objects used for generating prompts in the conversational retrieval module. The first template is used to rephrase a follow-up question to a standalone question, while the second template is used to provide context and a question for a conversational retrieval prompt.

<!--- END SELFDOC --->