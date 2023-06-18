<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `llms` directory is for integration tests of various API wrappers and classes that implement LLMs. These tests cover valid and invalid calls to the APIs, saving/loading LLMs, streaming tokens, error handling, and stop logic. The directory includes tests for API wrappers such as AI21, Aleph Alpha, Anthropic, Anyscale, BananaDev, CerebriumAI, Cohere, ForefrontAI, GooseAI, GPT4All, HuggingFace, LlamaCpp, Modal, NLPCloud, OpenAI, Petals, Pipeline Cloud, PredictionGuard, RWKV, and more. The tests include initializing and running inference on self-hosted Hugging Face pipelines, testing the StochasticAI and Writer API wrappers, and a function for checking LLM object equality.

### Files
#### __init__.py
This file contains all the integration tests for LLM objects.

#### test_anthropic.py
This file contains integration tests for the `Anthropic` API wrapper. It includes tests for valid calls to the wrapper, streaming tokens from the wrapper, and testing that streaming correctly invokes a callback. It also includes tests for async generate and async streaming callbacks.

#### test_anyscale.py
This file contains a test for the Anyscale API wrapper in the langchain.llms.anyscale module. The test checks for a valid call to the Anyscale API and asserts that the output is a string.

#### test_banana.py
This file contains an integration test for the BananaDev API wrapper in the langchain.llms.bananadev module. The test ensures that a valid call to the BananaDev API returns a string output.

#### test_cerebrium.py
This file contains an integration test for the CerebriumAI API wrapper. The test ensures that a valid call to the wrapper returns a string output of no more than 10 characters.

#### test_cohere.py
This file contains integration tests for the Cohere API wrapper. The tests include a valid call to Cohere and saving/loading an LLM using Cohere.

#### test_forefrontai.py
This file contains an integration test for the ForefrontAI API wrapper in the langchain.llms.forefrontai module. The test checks for a valid call to the API and asserts that the output is a string.

#### test_google_palm.py
This file contains integration tests for the Google PaLM Text API wrapper. The first test checks for a valid call to the API, while the second test checks for saving/loading a Google PaLM LLM. These tests require a valid API key to run.

#### test_gooseai.py
This file contains three test functions that test the functionality of the GooseAI API wrapper. The tests include a valid call to GooseAI, a valid call to GooseAI with the fairseq model, and a test of the stop logic on valid configuration.

#### test_gpt4all.py
This file contains an integration test for the GPT4All class in the langchain.llms module. It tests the validity of the GPT4All inference by downloading a pre-trained model and checking if the output is a string.

#### test_huggingface_endpoint.py
This file contains integration tests for the HuggingFace API wrapper in the `langchain.llms.huggingface_endpoint` module. The tests include valid calls to text generation, text2text generation, and summarization models, as well as a test for a valid call that errors. Additionally, it contains a test case for saving and loading a HuggingFaceHub LLM.

#### test_huggingface_hub.py
This file contains integration tests for the HuggingFace API wrapper in the langchain.llms.huggingface_hub module. The tests include valid calls to text generation, text2text generation, and summarization models, as well as a test for a valid call that errors. Additionally, there is a test for saving and loading an HuggingFaceHub LLM.

#### test_huggingface_pipeline.py
This file contains integration tests for the HuggingFace Pipeline wrapper. It tests the valid calls to HuggingFace text generation, text2text generation, and summarization models, as well as saving and loading an HuggingFaceHub LLM. Additionally, it contains a test for initializing a Hugging Face pipeline for text generation with LLMs. The test checks that the pipeline can be successfully initialized and that the output is a string.

#### test_llamacpp.py
This file contains integration tests for the LlamaCpp wrapper, testing both its inference and streaming capabilities. The tests use a downloaded model and a fake callback handler to ensure that the generated text chunks are in the correct format and that the callback is invoked correctly.

#### test_manifest.py
This file contains an integration test for the `ManifestWrapper` class in the `langchain.llms.manifest` module. The test creates a `Manifest` object with a specified client name, then creates a `ManifestWrapper` object with the `Manifest` object and some keyword arguments. The test then calls the `ManifestWrapper` object with a prompt and checks that the output matches the expected value.

#### test_modal.py
This file contains an integration test for the Modal API wrapper in the langchain.llms.modal module. The test ensures that a valid call to the Modal class returns a string output.

#### test_nlpcloud.py
This file contains integration tests for the NLPCloud API wrapper. The tests include a valid call to the API and saving/loading an NLPCloud LLM.

#### test_openai.py
This file contains integration tests for the OpenAI API wrapper. It includes tests for valid calls to OpenAI, testing of model parameters, testing of extra keyword arguments, and testing that the LLM output contains the model name.

#### test_self_hosted_llm.py
This file contains integration tests for initializing and running inference on self-hosted Hugging Face pipelines using different methods. It includes functions to load the pipeline for testing and an inference function.

#### test_stochasticai.py
This file contains a test for the StochasticAI API wrapper in the langchain.llms.stochasticai module. The test checks for a valid call to the StochasticAI function and asserts that the output is a string.

#### test_writer.py
This file contains an integration test for the Writer API wrapper in the langchain.llms module. The test ensures that a valid call to the Writer class returns a string output.

#### utils.py
This file contains a function `assert_llm_equality` that is used for LLM tests. It checks that two LLM objects are of the same type and have the same values for all fields except for "client" and "pipeline".

<!--- END SELFDOC --->