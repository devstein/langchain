<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `plan_and_execute` directory is for defining a pipeline for executing a series of steps, where each step is planned by a `BasePlanner` and executed by a `BaseExecutor`. It includes the `PlanAndExecute` class, schema for the plan and execution process, and directories for implementing and defining classes that execute actions for agents and chains and planners that generate plans to solve problems.

### Directories
#### executors
The `executors` directory is for implementing and defining classes that execute actions for agents and chains. It contains the `BaseExecutor` and `ChainExecutor` classes, which are used as base classes for other executors, and the `load_agent_executor` function, which loads a `StructuredChatAgent` and creates an `AgentExecutor` from it.

#### planners
The `planners` directory is for implementing planners that generate plans to solve problems. It contains the `BasePlanner` and `LLMPlanner` classes for planning and executing actions based on input, as well as the `chat_planner.py` file which implements a chat planner that uses a language model to generate a plan from a system prompt.

<!--- END SELFDOC --->