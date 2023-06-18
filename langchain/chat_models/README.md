<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `chat_models` directory is for implementing and providing various chat model classes that can be used to generate chat messages. It includes classes such as `ChatOpenAI`, `AzureChatOpenAI`, `PromptLayerChatOpenAI`, `ChatAnthropic`, and `ChatGooglePalm`. These classes are wrappers around different chat APIs such as OpenAI, Azure OpenAI, Google PaLM, and Anthropic's large language model. The directory also includes an abstract base class `BaseChatModel` and a subclass `SimpleChatModel`.

### Files
#### azure_openai.py
This file contains the `AzureChatOpenAI` class, which is a wrapper around Azure OpenAI Chat Completion API. It inherits from the `ChatOpenAI` class and provides methods for calling the OpenAI API with Azure deployment, creating chat results, and checking for content filters. It requires certain environment variables to be set or passed in the constructor.

#### base.py
This file contains an abstract base class, `BaseChatModel`, which provides a base implementation for chat models. It includes methods for generating responses to messages and managing callbacks. Subclasses of this class can implement the abstract methods for generating chat results.

#### google_palm.py
This file contains a wrapper around Google's PaLM Chat API, including functions to truncate text and convert API responses. It also includes a class for generating chat completions using various decoding methods and temperature values.

#### openai.py
This file contains a class `ChatOpenAI` which is a wrapper around OpenAI Chat large language models. It includes functions to convert a dictionary to a message and vice versa, and a retry decorator for async API calls. The class can be instantiated with any parameters that are valid to be passed to the `openai.create` call.

#### promptlayer_openai.py
This file contains the implementation of `PromptLayerChatOpenAI` class, which is a wrapper around OpenAI Chat large language models and PromptLayer. It allows passing optional parameters such as `pl_tags` and `return_pl_id` to the OpenAI LLM. The `_generate` method calls `ChatOpenAI` generate and then calls PromptLayer API to log the request. The class also includes an asynchronous version of `_generate` called `_agenerate`.

<!--- END SELFDOC --->