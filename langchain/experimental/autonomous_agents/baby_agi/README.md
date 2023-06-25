<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `baby_agi` directory is for implementing a controller for autonomous agents called `BabyAGI`. It includes methods for managing tasks, prioritizing them based on their objective, and executing them using a task creation chain, a task prioritization chain, and a task execution chain. The directory also contains files for the task creation, task execution, and task prioritization chains, which are used to generate tasks, execute tasks, and prioritize tasks, respectively.

### Files
#### __init__.py
This file is the initialization file for the `langchain/experimental/autonomous_agents/baby_agi` directory. It imports and exports the `BabyAGI` class and the task-related classes `TaskCreationChain`, `TaskExecutionChain`, and `TaskPrioritizationChain`.

#### baby_agi.py
This file contains the implementation of the `BabyAGI` class, which is a controller for autonomous agents. It includes methods for managing tasks, prioritizing them based on their objective, and executing them using a task creation chain, a task prioritization chain, and a task execution chain. The `execute_task` function takes an objective, task, and k value, and returns the result of running the task. The `max_iterations` parameter can be used to limit the number of iterations.

#### task_creation.py
This file contains the `TaskCreationChain` class, which is a subclass of `LLMChain`. It generates tasks using the result of an execution agent and returns the tasks as an array. It uses a `PromptTemplate` to create a prompt for the task creation AI.

#### task_execution.py
This file contains the `TaskExecutionChain` class, which is a chain used to execute tasks. It includes a method to create a new instance of the chain from a `BaseLanguageModel` and a prompt template for generating prompts to execute tasks.

#### task_prioritization.py
This file contains the `TaskPrioritizationChain` class, which is a chain used to prioritize tasks. It includes a method to create a response parser from a given language model. The class uses a prompt template to provide instructions to the AI on how to reprioritize tasks.

<!--- END SELFDOC --->