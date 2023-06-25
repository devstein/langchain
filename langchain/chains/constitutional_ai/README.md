<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `constitutional_ai` directory is for implementing the `Constitutional AI` method proposed by Bai et al. in 2022. It includes files for defining constitutional principles, generating prompts for few-shot learning, and implementing the `ConstitutionalChain` for critiquing and revising text based on constitutional principles.

### Files
#### __init__.py
This file contains a brief description of the `Constitutional AI` method proposed by Bai et al. in 2022, which is used for self-critique in the `constitutional_ai` chain.

#### base.py
This file contains the implementation of `ConstitutionalChain`, a chain for applying constitutional principles to the outputs of another chain. It includes methods for critiquing and revising text based on constitutional principles, as well as parsing critique output strings and running a text manager.

#### models.py
This file defines a Pydantic BaseModel class for a constitutional principle. It includes three attributes: critique_request, revision_request, and name.

#### principles.py
This file defines a dictionary of `ConstitutionalPrinciple` objects, each representing a principle that the AI assistant should adhere to. The principles include avoiding harmful, unethical, racist, sexist, toxic, dangerous, or illegal content. Each principle has a critique request and a revision request to ensure the assistant's responses align with the principles.

<!--- END SELFDOC --->