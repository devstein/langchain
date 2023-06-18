<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `llms` directory is for wrappers and implementations of various large language models APIs, including LlamaCpp, NLPCloud, OpenAI, Petals, PipelineAI, PredictionGuard, Replicate, RWKV, SagemakerEndpoint, SelfHosted, SelfHostedHuggingFaceLLM, StochasticAI, and Writer. These wrappers and implementations provide a way to generate text completions using the respective APIs, with configurable parameters such as model name, sampling temperature, maximum and minimum number of tokens to generate, and more. The directory also includes utility functions for loading LLMs from configuration files, enforcing stop tokens, and streaming results in real-time.

### Files
#### __init__.py
This file contains a list of LLM (large language model) classes and a dictionary mapping string types to their corresponding LLM classes, serving as wrappers on top of large language model APIs.

#### ai21.py
This file contains the implementation of the `AI21` class, which is a wrapper around AI21 large language models. It includes parameters for model selection, sampling temperature, maximum and minimum number of tokens to generate, and penalties for repeated tokens. The class also provides an example of how to use it. Additionally, it defines a Pydantic model for interacting with the AI21 API and contains a function that sends a request to the AI21 API to generate text based on a given prompt, handling various parameters such as stop sequences and default parameters.

#### aleph_alpha.py
This file contains the implementation of the AlephAlpha class, which is a wrapper around Aleph Alpha large language models. It includes parameters for model name, maximum tokens, temperature, top k, top p, presence penalty, frequency penalty, and repetition penalties. The class requires the aleph_alpha_client python package to be installed and the ALEPH_ALPHA_API_KEY environment variable to be set.

#### anthropic.py
This file contains a Pydantic BaseModel and various methods for interacting with Anthropic's large language models, including generating text based on a given prompt. It also includes methods for calling out to Anthropic's completion endpoint asynchronously and returning the resulting generator. Additionally, it defines a function for generating a poem using the anthropic package.

#### anyscale.py
This file contains the implementation of the `Anyscale` class, which is a wrapper around Anyscale Services. It provides a simple interface to use Anyscale for distributed processing. The class takes in the environment variables `ANYSCALE_SERVICE_URL`, `ANYSCALE_SERVICE_ROUTE`, and `ANYSCALE_SERVICE_TOKEN` or they can be passed as named parameters to the constructor.

#### bananadev.py
This file contains a wrapper class implementation for the Banana API, which is a large language model. The class allows passing any valid parameters and holds any model parameters valid for the create call not explicitly specified. It also includes a root validator to build extra kwargs from additional parameters that were passed in. Additionally, it contains a function `_call` that is used to call the Banana endpoint, taking in a prompt, an optional stop list, and an optional callback manager, and returning the response text after running the Banana model.

#### base.py
This file contains the `BaseLLM` class, which is a wrapper for a language model that takes in a prompt and returns a string. It includes methods for updating the cache, generating LLM output, and saving the LLM to a file. It also contains abstract and concrete methods for generating language model outputs from given prompts, both synchronously and asynchronously.

#### cerebriumai.py
This file contains the implementation of the `CerebriumAI` class, which is a wrapper around the CerebriumAI API. It provides a method to send a prompt to the API and return the generated text, while enforcing stop tokens if provided. The class holds any model parameters valid for the `create` call not explicitly specified and has a `root_validator` method that builds extra kwargs from additional parameters that were passed in.

#### cohere.py
This file contains the `Cohere` class, a wrapper around Cohere APIs, with various parameters for tuning text generation. It requires the `cohere` python package to be installed and the `COHERE_API_KEY` environment variable to be set or passed as a named parameter to the constructor.

#### fake.py
This file contains the implementation of a fake LLM wrapper, `FakeListLLM`, used for testing purposes. It includes a `_call` method that returns responses from a list and an `_identifying_params` property that returns a dictionary of identifying parameters.

#### google_palm.py
This file contains the implementation of the `GooglePalm` class, which is a subclass of `BaseLLM` and `BaseModel`. It defines various parameters for running inference, such as `temperature`, `top_p`, `top_k`, and `max_output_tokens`. The class also includes methods for generating text using the Google Palm model and performing input validation. Additionally, the file contains a `root_validator` function to validate the Google API key and check if the required Python package exists.

#### gooseai.py
This file contains a wrapper class around the GooseAI API, allowing interaction with OpenAI large language models. It includes methods for passing valid parameters to the openai.create call, with the API key expected to be set in the environment variable "GOOSEAI_API_KEY".

#### gpt4all.py
This file contains a class called `GPT4All` which is a wrapper around GPT4All language models. It includes configuration parameters for the pre-trained model file, token context window, number of parts to split the model into, seed, and more. The class can be used to generate text based on the pre-trained model.

#### huggingface_endpoint.py
This file contains a Python class that provides an interface to HuggingFaceHub Inference Endpoints for text-generation and text2text-generation tasks. It handles validation of environment variables and API keys, identifying parameters, and error handling for invalid requests.

#### huggingface_hub.py
This file defines a class `HuggingFaceHub` which is a wrapper around HuggingFaceHub models. It supports `text-generation` and `text2text-generation` tasks and requires the `huggingface_hub` python package to be installed. The `HUGGINGFACEHUB_API_TOKEN` environment variable should be set with your API token or passed as a named parameter to the constructor.

#### huggingface_pipeline.py
This file contains a class for a Hugging Face pipeline that provides a wrapper around HuggingFace Pipeline APIs for performing various natural language processing tasks, including `text-generation` and `text2text-generation`. It includes a method `from_model_id` for constructing a pipeline object from a given model ID and task, and a function `_call` for generating text based on a prompt and task, with optional stop tokens.

#### huggingface_text_gen_inference.py
This file contains the implementation of a wrapper class, `HuggingFaceTextGenInference`, around the HuggingFace text generation inference API. It includes options for setting various parameters such as `max_new_tokens`, `top_k`, `top_p`, `typical_p`, `temperature`, `repetition_penalty`, `stop_sequences`, `seed`, `inference_server_url`, `timeout`, and `client`. The class also includes methods such as `_call` and `_llm_type` for calling the text generation with a prompt and returning the type of LLM.

#### llamacpp.py
This file defines the `LlamaCpp` class, which is a Python wrapper around the llama.cpp model. It provides methods for generating text from the model given a prompt, and includes various options for controlling the generation process. The class also includes a validator to ensure that the necessary dependencies are installed.

#### modal.py
This file contains a Python class `Modal` that represents a Modal language model (LLM) and provides a way to interact with large language models. It has methods to get identifying parameters, return the type of LLM, and make a call to the Modal endpoint by sending a prompt and returning the generated text.

#### nlpcloud.py
This file contains the implementation of the `NLPCloud` class, which is a wrapper around NLPCloud APIs. It provides a way to use NLPCloud large language models and requires the `nlpcloud` python package to be installed and the `NLPCLOUD_API_KEY` environment variable to be set with the API key. The class includes methods for setting default parameters, identifying parameters, and making API calls to generate text based on a given prompt.

#### openai.py
This file contains a wrapper around OpenAI APIs, including functions for generating responses to prompts, updating token usage, and handling streaming results. It also includes a retry decorator for OpenAI API calls and a class for initializing the OpenAI object. Additionally, it provides functions for working with OpenAI's GPT models, calculating the number of tokens in a given text, and creating an LLMResult from choices and prompts.

#### petals.py
This file contains a wrapper class called "Petals" around the Petals API, which can be used to generate new tokens for a given input text. It also includes methods for getting default and identifying parameters, returning the type of LLM, and calling the API with a prompt and optional stop tokens.

#### pipelineai.py
This file contains a wrapper class called PipelineAI, which is a subclass of LLM and BaseModel. It provides methods for creating a pipeline using the Pipeline Cloud API, validating environment variables, identifying parameters, and retrieving the result preview.

#### predictionguard.py
This file contains the `PredictionGuard` class, which is a wrapper around Prediction Guard large language models. It has methods to get default and identifying parameters, and a `_call` method to make the API call to the model. It requires the `predictionguard` python package to be installed and the `PREDICTIONGUARD_TOKEN` environment variable to be set with an access token. It validates that the access token and python package exist in the environment.

#### promptlayer_openai.py
This file contains the implementation of the `PromptLayerOpenAI` class, which is a wrapper around OpenAI large language models. It adds two optional parameters to the OpenAI LLM and logs the request using the PromptLayer API. The class includes methods for generating responses synchronously and asynchronously.

#### replicate.py
This file contains a Python wrapper implementation for the Replicate API, which allows for easy interaction with Replicate models. It utilizes the LLM base class and requires the `replicate` package to be installed and the `REPLICATE_API_TOKEN` environment variable to be set. The `Replicate` class takes in a model and additional parameters as input, and handles field name transfers and duplicate value checks.

#### sagemaker_endpoint.py
This file defines a class `SagemakerEndpoint` that handles the interaction with an AWS SageMaker endpoint. It includes a content handler class to transform input and output formats between LLM and the endpoint, as well as optional keyword arguments to pass to the model and endpoint. The class also handles authentication and validation of AWS credentials and Python package existence.

#### self_hosted.py
This file contains functions for running model inference on self-hosted remote hardware. It includes a function for generating text predictions for each document in a batch, and a function for sending a pipeline to a device on the cluster. The file also imports various modules and defines a logger.

#### self_hosted_hugging_face.py
This file contains a wrapper and utility functions for running HuggingFace language models on self-hosted remote hardware. It includes a function for generating text and loading transformers, as well as a Pydantic model for configuring the pipeline. The file also provides documentation and examples for the `SelfHostedHuggingFaceLLM` class, which currently supports `text-generation`, `text2text-generation`, and `summarization` tasks.

#### stochasticai.py
This file contains the `StochasticAI` class, which is a Python wrapper around the StochasticAI large language models. It allows users to generate text by sending prompts to the StochasticAI API and enforcing stop tokens if specified. The class requires the environment variable `STOCHASTICAI_API_KEY` to be set with the user's API key.

#### utils.py
This file contains a utility function `enforce_stop_tokens` that takes a string of text and a list of stop words as input, and returns the text up to the first occurrence of any of the stop words. This function is useful for cutting off text at a certain point, such as when working with natural language processing.

#### writer.py
This file contains a `Writer` class that serves as a wrapper around Writer large language models. It allows for customization of the model's behavior and requires an API key to be set as an environment variable. Additionally, the file contains a `_call` function responsible for calling out to Writer's complete endpoint.

<!--- END SELFDOC --->