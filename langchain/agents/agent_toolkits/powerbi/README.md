<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `powerbi` directory is for constructing Power BI agents and toolkits that interact with a Power BI dataset. It includes files for initializing the agent toolkit, creating a Power BI agent, constructing a conversational chat agent, providing prompts and instructions for the agent, and a toolkit for interacting with the dataset.

### Files
#### __init__.py
This file is the initialization file for the Power BI agent toolkit.

#### base.py
This file contains a function `create_pbi_agent` that constructs a Power BI agent using an LLM and tools. The function takes in optional parameters such as a Power BI dataset, callback manager, input variables, and more. It checks if a toolkit or Power BI dataset is provided and constructs the agent accordingly.

#### prompt.py
This file contains prompts and instructions for the PowerBI agent, including `POWERBI_PREFIX`, `POWERBI_SUFFIX`, `POWERBI_CHAT_PREFIX`, and `POWERBI_CHAT_SUFFIX`. These prompts provide an introduction to the agent, explain how it can help users interact with a PowerBI dataset, and provide guidance on how to interpret user questions and format answers. Additionally, `POWERBI_CHAT_SUFFIX` provides information about available tools and instructions for formatting responses, including limiting the query to a specified number of results.

#### toolkit.py
This file contains the `PowerBIToolkit` class, which is a toolkit for interacting with a Power BI dataset. It includes tools for querying, listing, and providing information about the dataset, as well as a prompt template for generating queries. The class inherits from `BaseToolkit` and uses `pydantic` for configuration. Additionally, the file includes a `Toolkit` class with a `get_tools` method that returns a list of `BaseTool` objects, including a `QueryPowerBITool`, `InfoPowerBITool`, `ListPowerBITool`, and an `InputToQueryTool`.

<!--- END SELFDOC --->