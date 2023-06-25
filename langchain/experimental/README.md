<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `experimental` directory is for implementing and testing new features and functionalities in LangChain. It includes directories for autonomous and generative agents, implementing language models and generators, defining a pipeline for executing a series of steps, and providing instructions and code examples for enabling tracing in LangChain applications, creating and running chains on datasets, and evaluating agents using datasets.

### Directories
#### autonomous_agents
The `autonomous_agents` directory is for implementing autonomous agents that interact with the Auto-GPT model and a controller for these agents called `BabyAGI`. It contains the `autogpt` directory for defining the `AutoGPT` agent, its memory, output parser, prompt, and prompt generator, and the `baby_agi` directory for managing tasks, prioritizing them based on their objective, and executing them using a task creation chain, a task prioritization chain, and a task execution chain.

#### client
The `client` directory is for providing instructions and code examples for enabling tracing in LangChain applications, creating and running chains on datasets, and evaluating agents using datasets. It includes a Jupyter notebook that warns about the experimental tracing API and provides links to the LangChain+ client for reviewing results.

#### generative_agents
The `generative_agents` directory is for building generative agents in Langchain. It includes the `GenerativeAgent` and `GenerativeAgentMemory` classes, which represent a character with memory and innate characteristics, and a memory class that extends `BaseMemory` and contains attributes and methods for storing and retrieving memories, and generating language using a language model.

#### llms
The `llms` directory is for implementing language models and generators that can complete structured text and generate JSON data based on a prompt. It includes a JsonFormer class and a RELLM (Regular Expression Language Model) wrapped LLM (Language Model) class.

#### plan_and_execute
The `plan_and_execute` directory is for defining a pipeline for executing a series of steps, where each step is planned by a `BasePlanner` and executed by a `BaseExecutor`. It includes the `PlanAndExecute` class, schema for the plan and execution process, and directories for implementing and defining classes that execute actions for agents and chains and planners that generate plans to solve problems.

<!--- END SELFDOC --->