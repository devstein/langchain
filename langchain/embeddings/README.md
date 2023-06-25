<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `embeddings` directory is for implementing and providing wrappers for various embedding models. It includes classes and functions for generating embeddings using different APIs such as Aleph Alpha, Cohere, Google PaLM, HuggingFace, Jina, LlamaCpp, OpenAI, Sagemaker, and TensorflowHub. It also includes an abstract base class `Embeddings` that serves as an interface for embedding models.

### Files
#### __init__.py
This file contains imports for all the available embedding modules in the `langchain/embeddings` directory and defines the `__all__` list of available embeddings. It also includes a deprecated class `HypotheticalDocumentEmbedder` with a warning message to use the updated class from `langchain.chains` instead.

#### aleph_alpha.py
This file contains a Pydantic BaseModel wrapper for Aleph Alpha's Asymmetric Embeddings, providing an endpoint to embed documents and queries with optimized models. It includes optional parameters for customization.

#### base.py
This file defines an abstract base class `Embeddings` which serves as an interface for embedding models. It contains two abstract methods `embed_documents` and `embed_query` which must be implemented by any class that inherits from `Embeddings`. The `embed_documents` method takes a list of strings and returns a list of lists of floats, while the `embed_query` method takes a string and returns a list of floats.

#### cohere.py
This file contains a wrapper around Cohere embedding models, including a class `CohereEmbeddings` and a method `embed_documents` that calls out to Cohere's embedding endpoint. It provides functions to generate embeddings for text and requires the `cohere` python package to be installed and the `COHERE_API_KEY` environment variable to be set.

#### google_palm.py
This file contains a wrapper around Google's PaLM Embeddings APIs. It defines a `GooglePalmEmbeddings` class that inherits from `BaseModel` and `Embeddings`. The class has methods to embed documents and query text using the Google PaLM model.

#### huggingface.py
This file contains the `HuggingFaceEmbeddings` class, which is a wrapper around HuggingFace embedding models. It allows for the use of the `sentence_transformers` python package and provides key word arguments to pass to the model. The class provides methods to compute document and query embeddings.

#### huggingface_hub.py
This file provides a Pydantic model for a wrapper around HuggingFace Hub embedding models, allowing for easy embedding of documents and queries. It includes validation for the API token and Python package, and supports various tasks.

#### jina.py
This file contains a wrapper around Jina embedding models. It defines a `JinaEmbeddings` class that inherits from `BaseModel` and `Embeddings`. It also includes a `validate_environment` method that validates the existence of an auth token in the environment and sets up the client.

#### openai.py
This file provides a wrapper for OpenAI embedding models, including functions for retrying embedding calls and handling large input text. It also includes instructions for using the library with Microsoft Azure endpoints and a Pydantic model for OpenAI embeddings.

#### sagemaker_endpoint.py
This file contains the `SagemakerEndpointEmbeddings` class, which provides a wrapper around custom Sagemaker Inference Endpoints for computing document and query embeddings. It includes methods for input and output transformation and uses the Sagemaker InvokeEndpoint API to make predictions.

#### self_hosted.py
This file contains the implementation of the `SelfHostedEmbeddings` and `SelfHostedHFEmbeddings` classes, which allow for running custom and HuggingFace transformer embedding models on self-hosted remote hardware. The classes include methods for computing document and query embeddings, as well as a configuration object and an inference function.

#### self_hosted_hugging_face.py
This file contains classes and functions for running HuggingFace embedding models on self-hosted remote hardware, including support for various hardware and the ability to embed documents. It provides an easy-to-use wrapper for computing embeddings using a self-hosted HuggingFace instruct model.

#### tensorflow_hub.py
This file implements a wrapper around TensorflowHub embedding models, providing methods to compute document and query embeddings. The default model used is the multilingual Universal Sentence Encoder.

<!--- END SELFDOC --->