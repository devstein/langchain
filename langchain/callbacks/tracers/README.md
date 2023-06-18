<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `tracers` directory is for implementing tracers that record and persist information about LLM, chain, tool, and chat model runs. It includes an abstract `BaseTracer` class, a `LangChainTracer` class that records to a LangChain endpoint, a `LangChainTracerV1` class that converts Run objects to LLMRun, ChainRun, or ToolRun objects, and Pydantic schemas for defining and interacting with TracerSession, TracerSessionV2, LLMRun, ChainRun, and ToolRun. It also includes functions for printing messages to the console during a LangChain run.

### Files
#### __init__.py
This file is the initialization file for the `langchain/callbacks/tracers` directory. It imports and exports the `LangChainTracer` and `LangChainTracerV1` classes from the `langchain` and `langchain_v1` modules respectively. These classes are used to record the execution of LangChain runs.

#### base.py
This file defines the `BaseTracer` class, an abstract base class for tracers used in the Langchain application. It provides methods for starting and ending a trace, handling errors, and adding child runs to a chain or tool run. It also includes functionality for persisting runs and tracing sessions.

#### langchain.py
This file contains the implementation of a Tracer that records to a LangChain endpoint. It includes functions for getting headers and the endpoint, as well as methods for starting a trace, getting the execution order, and loading or using the tenant ID. Additionally, it contains functions for persisting a `TracerSession` and `Run`.

#### langchain_v1.py
This file contains the implementation of the LangChainTracerV1 class, which includes methods to convert a Run object to a LLMRun, ChainRun, or ToolRun object, and persisting runs and sessions. It also defines a function to load tracing sessions from the `langchain_v1` module.

#### schemas.py
This file contains Pydantic schemas for tracers, including `TracerSessionV1`, `TracerSession`, `LLMRun`, `ChainRun`, `ToolRun`, `RunTypeEnum`, `RunBase`, `Run`, and `RunCreate`. These schemas define the structure of data objects used in the LangChain API for tracing and debugging, including different types of runs, their inputs, outputs, and child runs. The `Run` schema is used when loading from the database and includes a `name` field assigned based on the serialized data.

#### stdout.py
This file contains functions for printing messages to the console during a LangChain run, including information about the start, end, and errors of tool runs, as well as input, output, and elapsed time.

<!--- END SELFDOC --->