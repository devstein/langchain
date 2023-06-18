<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `zapier` directory is for the Zapier Toolkit, which contains the `ZapierToolkit` class and its methods for creating a toolkit from a `ZapierNLAWrapper` and returning the tools in the toolkit. It also contains an initialization file.

### Files
#### __init__.py
This file is the initialization file for the Zapier Toolkit.

#### toolkit.py
This file defines the `ZapierToolkit` class, which is a subclass of `BaseToolkit`. It contains a method `from_zapier_nla_wrapper` that creates a toolkit from a `ZapierNLAWrapper` and a method `get_tools` that returns the tools in the toolkit. The `ZapierToolkit` class has an empty list of tools by default, but `from_zapier_nla_wrapper` populates it with `ZapierNLARunAction` instances.

<!--- END SELFDOC --->