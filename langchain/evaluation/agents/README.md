<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `agents` directory is for evaluating ReAct style agents using a `TrajectoryEvalChain` class. It includes the implementation of the class in `trajectory_eval_chain.py` and a prompt template and code for evaluating an AI language model's trajectory in answering a user's question in `trajectory_eval_prompt.py`.

### Files
#### __init__.py
This file exports the `TrajectoryEvalChain` class from `trajectory_eval_chain.py` for evaluating ReAct style agents.

#### trajectory_eval_chain.py
This file contains the implementation of a chain for evaluating ReAct style agents. It defines a `TrajectoryEvalChain` class that extends the `Chain` class and contains a `TrajectoryOutputParser` class for parsing the output of the model evaluation. The chain also has a `get_agent_trajectory` method for getting the agent trajectory.

#### trajectory_eval_prompt.py
This file contains a prompt template and code for evaluating an AI language model's trajectory in answering a user's question. The evaluation is based on criteria such as the helpfulness of the final answer, the logical sequence of tools used, and the appropriateness of the tools used. The prompt includes a system message introducing the evaluation task, a human message with example input, an AI message with example output, and a human message prompt template for the evaluation.

<!--- END SELFDOC --->