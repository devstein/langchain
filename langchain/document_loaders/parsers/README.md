<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `parsers` directory is for parsing various document formats such as HTML, PDF, and text. It includes a generic parser that uses mime-types to determine how to parse a blob, PDF parsers that use different libraries, a registry of default parser configurations for different mime-types, and a text parser. The directory also contains an `html` subdirectory for parsing HTML files using the Beautiful Soup library and enriching metadata with page title.

### Files
#### __init__.py
This file is the initialization file for the `parsers` module, which contains parsers for various document formats such as HTML and PDF. It imports and exports the available parsers for use in other parts of the codebase.

#### generic.py
This file contains a generic parser, `MimeTypeBasedParser`, that uses mime-types to determine how to parse a blob. It takes a mapping from mime-types to functions that parse a blob and return a document. Additionally, the file contains a function `lazy_parse` that loads documents from a blob, checks the mimetype of the blob, and uses the appropriate handler to parse it. If the mimetype is not supported and there is no fallback parser, it raises a ValueError.

#### pdf.py
This file contains three classes that parse PDFs using different libraries: `PyPDFParser` uses pypdf and chunks at character level, `PDFMinerParser` uses PDFMiner, and `PyMuPDFParser` uses PyMuPDF. All three classes inherit from `BaseBlobParser` and have a `lazy_parse` method that yields `Document` objects.

### Directories
#### html
The `html` directory is for parsing HTML files using the Beautiful Soup library and enriching metadata with page title. It contains an initialization file and a `bs4.py` file that defines the `BS4HTMLParser` class for loading HTML documents into document objects.

<!--- END SELFDOC --->