<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `steamship_image_generation` directory is for generating images from a text-prompt using Steamship. It contains the `__init__.py` initialization file, the `tool.py` file with the `SteamshipImageGenerationTool` class, and the `utils.py` file with the `make_image_public` function.

### Files
#### __init__.py
This file is the initialization file for the `steamship_image_generation` directory. It imports the `SteamshipImageGenerationTool` class from the `tool` module and makes it available for import from this directory.

#### tool.py
This file contains the `SteamshipImageGenerationTool` class, which generates images from a text-prompt using Steamship. It supports Dall-E and Stable Diffusion image models, with image sizes validated and errors raised if unsupported.

#### utils.py
This file contains a function `make_image_public` that takes in a `Steamship` client and a `Block` and uploads the block to a signed URL, returning the public URL. It requires the `steamship` package to be installed.

<!--- END SELFDOC --->