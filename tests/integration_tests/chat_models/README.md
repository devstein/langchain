<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `chat_models` directory is for testing the functionality of different chatbot models and their wrappers. The directory contains test files for the `ChatAnthropic`, `ChatGooglePalm`, `ChatOpenAI`, and `PromptLayerChatOpenAI` classes, which cover basic functionality, message generation, streaming, and callback handling.

### Files
#### test_anthropic.py
This file contains test functions for the `ChatAnthropic` class in the `langchain.chat_models.anthropic` module. The tests check if a valid call to the anthropic API wrapper returns an `AIMessage` object with a string content, if streaming tokens from anthropic returns an `AIMessage` object with a string content, and if streaming correctly invokes the `on_llm_new_token` callback. Additionally, there is a test function that checks the formatting of chat messages.

#### test_google_palm.py
This file contains test functions for the `ChatGooglePalm` class, which is a wrapper for the Google PaLM Chat API. The tests cover basic functionality, using a system message, generating multiple responses, and async generation. The tests ensure that the responses are instances of the `BaseMessage` class and that the content is a string.

#### test_openai.py
This file contains multiple test functions that verify the functionality of the `ChatOpenAI` wrapper class, including handling human and system messages, generating chat responses, and verifying streaming and model name output.

<!--- END SELFDOC --->