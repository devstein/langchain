<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `pal` directory is for implementing Program-Aided Language Models through the `PALChain` base class, with methods for input and output keys, calling the chain, and loading PAL from math and colored object prompts. It also contains modules for solving simple math problems and a colored object prompt.

### Files
#### __init__.py
This file contains the initialization code for the `pal` module, which implements Program-Aided Language Models as described in a research paper.

#### base.py
This file implements the PALChain class which is a Program-Aided Language Model. It contains a root validator that raises a warning if the class is instantiated with an llm argument instead of llm_chain, and a deprecated prompt attribute.

<!--- END SELFDOC --->