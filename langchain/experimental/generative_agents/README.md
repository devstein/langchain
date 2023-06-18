<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `generative_agents` directory is for building generative agents in Langchain. It includes the `GenerativeAgent` and `GenerativeAgentMemory` classes, which represent a character with memory and innate characteristics, and a memory class that extends `BaseMemory` and contains attributes and methods for storing and retrieving memories, and generating language using a language model.

### Files
#### __init__.py
This file exports the `GenerativeAgent` and `GenerativeAgentMemory` classes from the `generative_agent` and `memory` modules, respectively. These classes are primitives for building generative agents in Langchain.

#### generative_agent.py
This file contains the `GenerativeAgent` class, which represents a character with memory and innate characteristics. It includes various attributes such as the character's name, age, traits, status, memory, and language model. The class has methods for generating reactions and dialogue responses based on observations, as well as computing and returning a descriptive summary of the agent. Additionally, it has a function to parse a newline-separated string into a list of strings and a function to get a full header containing the agent's status, summary, and current time.

#### memory.py
This file contains the implementation of a `GenerativeAgentMemory` class, which defines the memory of a generative agent, including the language model, memory retriever, and current plan. It also includes methods for parsing a newline-separated string into a list of strings, reflecting on recent observations and generating insights, scoring the importance of a given memory, and adding an observation or memory to the agent's memory.

<!--- END SELFDOC --->