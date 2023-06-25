<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `powerbi` directory is for tools that interact with a PowerBI dataset. It includes files for writing DAX queries and a tool for querying a Power BI dataset by taking a detailed question as input and outputting a result.

### Files
#### __init__.py
This file contains a brief description of the `langchain/tools/powerbi` directory, which includes tools for interacting with a PowerBI dataset.

#### prompt.py
This file provides instructions and examples for writing DAX queries that can be sent to Power BI. It includes commonly used functions for table expressions, sorting query results, and defining calculated entity definitions. Additionally, it contains functions for filtering tables, returning tables with single rows, and removing duplicates from tables or columns. The file also lists aggregation and date/time functions available in Power BI. Finally, it includes a Python script for prompting the user to input a DAX query and handling errors.

#### tool.py
This file contains the implementation of `QueryPowerBITool`, a tool for querying a Power BI dataset by taking a detailed question as input and outputting a result. It has a maximum of 5 iterations to try to answer the question and includes methods for validating input variables and executing a query.

<!--- END SELFDOC --->