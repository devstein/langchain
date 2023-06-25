<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `callbacks` directory is for implementing callback handlers that listen to events in LangChain and perform various actions, such as logging metrics to external platforms, printing messages to standard output, and streaming LLM tokens. It includes callback handlers for OpenAI, stdout, AIM, Wandb, MLflow, ClearML, Comet, WhyLabs, and async iterators, as well as a callback manager for handling multiple callback handlers. The directory also contains utility functions and classes for handling metadata and associated function states for callbacks.

### Files
#### aim_callback.py
This file contains various implementations of the `AimCallback` class and related callback functions for tracking LLM and chain events using the AIM library. It includes methods to set up the callback, track LLM starts and system parameters, and flush the tracker.

#### arize_callback.py
This file contains the `ArizeCallbackHandler` class, which is a callback handler that logs prompt-response pairs to the Arize platform and generates embeddings for them. It also records token usage and other necessary data during LLM execution.

#### base.py
This file defines mixins, classes, and functions to handle callbacks related to the Language Model and Chain processes in LangChain. It includes methods to run code at different stages of the processes, such as when a tool finishes running or when an error occurs. It also provides a base class for callback handlers and a manager class to handle multiple callback handlers.

#### clearml_callback.py
This file contains the implementation of `ClearMLCallback`, a callback handler that logs to ClearML and provides methods for analyzing text and saving models. It can be configured with various parameters and updates response dictionaries with relevant information.

#### comet_ml_callback.py
This file defines a callback handler for logging experiments to Comet.ml. It imports the `comet_ml` package and defines a function to get an experiment object with the specified workspace and project name.

#### manager.py
This file contains various classes and methods for managing callbacks in LangChain. It includes classes for managing callbacks for synchronous and asynchronous runs, LLM runs, chain runs, and tool runs. It also includes a `CallbackManager` class with methods for handling events during the execution of the LLM. Additionally, it contains a `configure` method for configuring the callback manager and a generic event handler for `CallbackManager`.

#### mlflow_callback.py
This file contains the `MLflowCallback` class, which provides a callback for logging LangChain's training and evaluation metrics to MLflow. It includes methods for flushing the tracker, creating a session analysis dataframe, and saving LangChain assets as MLflow artifacts.

#### openai_info.py
This file contains a callback handler that tracks OpenAI token usage and cost for a given model. It includes methods to calculate the cost of tokens and track the total number of tokens used, successful requests, and total cost.

#### stdout.py
This file contains the implementation of a callback handler that prints messages to standard output when certain events occur, such as entering or finishing a chain. It defines a `StdOutCallbackHandler` class that inherits from `BaseCallbackHandler` and overrides several of its methods.

#### streaming_aiter.py
This file contains the implementation of an async iterator callback handler that listens for new tokens from the LLM model and returns an async iterator that yields tokens from a queue until the LLM model is done generating tokens.

#### streaming_stdout.py
This file contains a callback handler class, `StreamingStdOutCallbackHandler`, which writes the LLM token to stdout when a new token is available, and includes methods for handling errors and events during the running of the LLM. It also defines two callback functions, `on_text` and `on_agent_finish`, for running on arbitrary text and at the end of an agent, respectively.

#### streaming_stdout_final_only.py
This file contains the `FinalStreamingStdOutCallbackHandler` class, which is a callback handler for streaming in agents that only streams the final output of the agent. It remembers the last n tokens and checks if they match the `answer_prefix_tokens` list, and if they do, it starts printing tokens from that point onwards.

#### streamlit.py
This file contains a class called `StreamlitCallbackHandler` that logs various events during the execution of an agent to Streamlit. The events include prompts, new LLM tokens, entering and finishing a chain, and tool start logs in specified colors. The displayed text is formatted to render correctly in Streamlit.

#### utils.py
This file contains utility functions and a class for handling metadata and associated function states for callbacks, as well as functions for flattening nested dictionaries, hashing strings, and loading json files to strings. It also includes attributes and lists for tracking the number of times certain methods have been called and whether to ignore certain types of callbacks.

#### wandb_callback.py
This file contains a module for the `wandb_callback` which provides a callback handler for logging experiment metrics to Weights and Biases. It includes methods for logging data during different stages of a chain's execution, generating complexity metrics and visualization files, and flushing the tracker and resetting the session.

#### whylabs_callback.py
This file contains the implementation of the `WhyLabsCallbackHandler` class, which is a callback handler for the WhyLabs platform. It logs the input prompts and the generated text to the configured WhyLabs logger. The class provides methods to close the logger and to enter and exit the context.

### Directories
#### tracers
The `tracers` directory is for implementing tracers that record and persist information about LLM, chain, tool, and chat model runs. It includes an abstract `BaseTracer` class, a `LangChainTracer` class that records to a LangChain endpoint, a `LangChainTracerV1` class that converts Run objects to LLMRun, ChainRun, or ToolRun objects, and Pydantic schemas for defining and interacting with TracerSession, TracerSessionV2, LLMRun, ChainRun, and ToolRun. It also includes functions for printing messages to the console during a LangChain run.

<!--- END SELFDOC --->