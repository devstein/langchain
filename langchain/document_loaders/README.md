<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `document_loaders` directory is for loading various types of documents from different sources. It includes loaders for specific file types such as EPub, Evernote, Facebook chat, Figma, Google Drive, Gutenberg, Hacker News, HTML, Hugging Face datasets, iFixit, images, IMSDb, JSON, Markdown, Mastodon toots, MediaWiki dump XML files, Modern Treasury API endpoint, Notion pages and databases, Obsidian files, Open Office ODT files, OneDrive files, PDF files, PowerPoint files, Psychic.dev platform, Python files, ReadTheDocs documentation directory dump, Reddit posts, Roam directory dump, rich text files, S3 directory, S3 file, sitemap, and Slack directory dump. Additionally, it contains loaders for loading data from APIs such as Spreedly, Stripe, and Twitter, and for loading data from URLs using Playwright, Selenium, and urllib. The directory also includes loaders for loading data from local files such as WhatsApp messages, Word documents, and YouTube transcripts. Finally, the directory contains subdirectories for loading blobs and parsing various document formats.

### Files
#### __init__.py
This file contains a comprehensive list of document loaders available in the langchain repository, including loaders for various file types, web-based content, and chat loaders for social media platforms. It also provides backwards compatibility for two loaders.

#### azure_blob_storage_container.py
This file contains the implementation of a loader for loading documents from an Azure Blob Storage container. It defines a class `AzureBlobStorageContainerLoader` which inherits from `BaseLoader` and has a `load` method that returns a list of `Document` objects. The loader uses `AzureBlobStorageFileLoader` to load documents from the container.

#### azure_blob_storage_file.py
This file contains the implementation of `AzureBlobStorageFileLoader` class which loads documents from an Azure Blob Storage file. It uses the `BlobClient` class from the `azure.storage.blob` package to download the blob data and then uses `UnstructuredFileLoader` to load the documents from the downloaded file.

#### base.py
This file defines an abstract interface for document loader implementations in the langchain library. It includes methods for lazy and eager parsing of blobs into documents, and splitting documents into chunks. It also provides an abstract class for blob parsers to parse raw data into one or more documents.

#### bigquery.py
This file defines a `BigQueryLoader` class and a function that loads data from a BigQuery table and creates a list of Document objects. The loader class loads a query result into a list of documents, with each document representing one row of the result. The function iterates over the query results, extracts the page content and metadata from each row, creates a Document object with the extracted data, and appends it to the list of documents.

#### bilibili.py
This file implements a BiliBili transcript loader that extracts the video ID from a list of video URLs and retrieves the video information and transcript using the `bilibili_api` package. It returns a list of `Document` objects containing the transcript and metadata of each video. If no subtitles are found, it returns an empty transcript and issues a warning.

#### blackboard.py
This file contains the implementation of a BlackboardLoader class that loads all documents from a Blackboard course, extracts attachments, and downloads them as documents. It also includes functions for parsing filenames and downloading files from a URL.

#### blockchain.py
This file defines a BlockchainDocumentLoader class that loads elements from a blockchain smart contract into Langchain documents, supporting Ethereum and Polygon networks using the Alchemy API. It includes methods for retrieving NFTs and detecting token ID value types.

#### chatgpt.py
This file contains the implementation of a loader that loads conversations from exported ChatGPT data. It defines a function to concatenate rows of messages and a class `ChatGPTLoader` that loads the conversations from a JSON file and returns a list of `Document` objects.

#### college_confidential.py
This file contains the `CollegeConfidentialLoader` class, which is a web-based loader that loads College Confidential webpages. The `load` method scrapes the webpage, selects the main content, and returns a list of `Document` objects containing the page content and metadata.

#### confluence.py
This file contains the implementation of a ConfluenceLoader class that loads Confluence pages and attachments into Document objects. The loader supports both username/api_key and Oauth2 login and allows the user to specify a list of page_ids and/or space_key to load. The class also provides an option to include attachments, which is set to False by default. Additionally, it includes functions for processing Confluence documents and their attachments, such as extracting text from images, Word documents, PDFs, Excel files, and SVGs.

#### directory.py
This file contains the implementation of the `DirectoryLoader` class, which loads visible documents from a directory and its subdirectories using a specified loader class. It also includes a `_is_visible` function to check if a file is hidden and uses the `tqdm` library for progress logging if available.

#### discord.py
This file contains the `DiscordChatLoader` class, which is used to load chat logs from a Pandas DataFrame. The `load` method returns a list of `Document` objects, each representing a chat message with metadata.

#### docugami.py
This file contains a `DocugamiLoader` class that loads processed documents from Docugami, as well as several private methods and functions used to parse XML trees and retrieve document and project details using the Docugami API. The file also includes a `load` function that can load documents either locally or remotely.

#### duckdb_loader.py
This file defines the `DuckDBLoader` class, which loads query results from DuckDB into a list of documents. Each document represents one row of the result, with the specified columns written into the `page_content` and `metadata` of the document.

#### email.py
This file defines two classes, `UnstructuredEmailLoader` and `OutlookMessageLoader`, for loading email files using different libraries. It also contains a function that extracts email metadata and body as a `Document` object.

#### epub.py
This file contains the implementation of the `UnstructuredEPubLoader` class, which is a loader that uses the `UnstructuredFileLoader` to load EPub files. It defines a method `_get_elements()` that partitions the EPub file using the `partition_epub()` function from the `unstructured.partition.epub` module.

#### evernote.py
This file implements a Python module for loading and parsing documents from Evernote files using the `lxml` and `pypandoc` libraries. It includes functions for parsing the content and resources of a note, as well as the note itself in XML format. Additionally, it defines a class `EverNoteLoader` that takes a file path and loads the content of the file as a `Document` object, returning a list of `Document` objects.

#### figma.py
This file contains the implementation of a loader that loads Figma files json dump. It defines a class `FigmaFileLoader` that inherits from `BaseLoader` and has a `load` method that returns a list of `Document` objects containing the page content and metadata of the Figma file.

#### gcs_directory.py
This file contains the implementation of a class `GCSDirectoryLoader` that loads documents from a Google Cloud Storage (GCS) directory. It imports the `Document` class and `BaseLoader` from `langchain.docstore.document` and `langchain.document_loaders.base` respectively. It also imports `GCSFileLoader` from `langchain.document_loaders.gcs_file`. The `load` method of this class loads all the documents from the specified GCS directory.

#### git.py
This file defines the `GitLoader` class, which loads text files from a Git repository into a list of `Document` objects. It applies filters to skip certain files and creates metadata for each document. The repository can be local or remote.

#### gitbook.py
This file contains a GitBook loader class that can load either a single page or all relative paths in the navbar. It inherits from the WebBaseLoader class and takes in a web page, a boolean flag to indicate whether to load all paths, a base URL, and a content selector. The class defines methods for loading text from a single GitBook page or multiple pages.

#### googledrive.py
This file contains the implementation of a document loader for Google Drive in the LangChain repository. It includes functions to load documents from a folder and from an ID, using the Google Drive API. The loaded documents are returned as instances of the `Document` class.

#### gutenberg.py
This file contains the `GutenbergLoader` class, which is a loader that loads .txt web files from the Gutenberg project. It inherits from the `BaseLoader` class and has a `load` method that returns a list of `Document` objects.

#### helpers.py
This file contains a function `detect_file_encodings` that tries to detect the encoding of a file and returns a list of `FileEncoding` tuples with the detected encodings ordered by confidence. The function uses the `chardet` library to detect the encoding and runs the detection in a separate thread to avoid blocking the main thread.

#### hn.py
This file implements a web scraper that loads data from Hacker News. It defines an HNLoader class that inherits from WebBaseLoader and has methods to load either the main page results or the comments page. The file also contains a function `load_results` that extracts information from an HN page and returns a list of `Document` objects.

#### html.py
This file contains the `UnstructuredHTMLLoader` class, which is a loader that uses `unstructured` to load HTML files. It inherits from the `UnstructuredFileLoader` class and overrides the `_get_elements` method to partition the HTML file using `unstructured.partition.html`.

#### html_bs.py
This file defines a document loader that uses BeautifulSoup to load HTML files and enriches metadata with page title. The `BSHTMLLoader` class takes a file path, file encoding, and optional arguments to pass to the BeautifulSoup object. The `load` method loads the HTML document into a document object and returns it.

#### hugging_face_dataset.py
This file contains the `HuggingFaceDatasetLoader` class and two functions, `lazy_load` and `load`, which are responsible for loading documents from the Hugging Face Hub dataset. The class and functions take in various arguments such as the path or name of the dataset, data directory, cache directory, and number of processes, and return the documents as a list of `Document` objects.

#### ifixit.py
This file contains the implementation of a loader for iFixit data, which allows downloading the text of a repair guide, text of Q&A's and wikis from devices on iFixit using their open APIs and web scraping. The loader is initialized with a web path and verifies that it starts with "https://www.ifixit.com" and contains one of the allowed paths ("/Device", "/Guide", "/Answers", "/Teardown").

#### image_captions.py
This file contains a loader that uses a pre-trained BLIP image captioning model to load captions for a list of images. It also includes a helper function that generates captions and metadata for a single image using the same model and processor.

#### imsdb.py
This file contains the `IMSDbLoader` class which is a web scraper that loads IMSDb webpages. It inherits from the `WebBaseLoader` class and overrides the `load` method to scrape the webpage and return a list of `Document` objects containing the page content and metadata.

#### json_loader.py
This file contains the implementation of a JSONLoader class that loads data from a JSON file and extracts text or data using a jq schema. It allows for the extraction of content from a specific key and the use of a metadata function to update metadata. Additionally, it performs validation and converts the sample to string format, and allows the user to customize the default metadata based on the content of the JSON object.

#### modern_treasury.py
This file contains a class called ModernTreasuryLoader that fetches data from Modern Treasury API endpoint. It includes a dictionary of endpoints and initializes with a resource, organization ID, and API key, and sets headers for authorization. The class has a method `_make_request` that sends a request to the API endpoint and returns a list of documents. The `load` method of the class returns the list of documents obtained from the API endpoint.

#### notebook.py
This file contains a `NotebookLoader` class that loads `.ipynb` notebook files, normalizes the data, and extracts relevant information such as cell type, source, and outputs. It also includes two helper functions: `concatenate_cells` to combine cells information in a readable format, and `remove_newlines` to remove newlines from data structures. The resulting text is concatenated and returned as a `Document` object.

#### notion.py
This file contains the implementation of a Notion directory loader that loads a directory dump of Notion pages as documents. It uses the `BaseLoader` class and the `Document` class from the `langchain.document_loaders` and `langchain.docstore.document` modules respectively. The `load` method reads the contents of each `.md` file in the directory and creates a `Document` object for each file with the page content and metadata.

#### notiondb.py
This file implements a Notion database loader for langchain, using the Notion API to read content from pages within a database and return a list of documents. It includes methods for loading pages and blocks, and a private method for sending HTTP requests to the Notion API.

#### obsidian.py
This file implements the ObsidianLoader class, which loads Obsidian files from disk, parses front matter metadata, removes it from the content, and returns a list of Document objects with metadata including source, path, creation time, and modification time.

#### odt.py
This file contains the implementation of a loader for Open Office ODT files using the UnstructuredFileLoader class. It validates the version of the Unstructured library and defines a method to retrieve the elements of the ODT file using the partition_odt function from the unstructured.partition.odt module.

#### onedrive.py
This file contains the implementation of a OneDrive document loader that loads supported document files from a specified OneDrive drive and returns a list of Document objects. It includes error handling and uses a OneDriveFileLoader to load the files.

#### onedrive_file.py
This file contains the implementation of a OneDrive file loader that downloads a file from OneDrive and uses an unstructured file loader to load the contents of the file as a list of documents.

#### pdf.py
This file contains multiple classes for loading PDF files and extracting their contents using different libraries such as `pdfminer`, `PyMuPDF`, and Mathpix OCR API. It also includes classes for cleaning PDF contents and parsing them using `pdfplumber`.

#### powerpoint.py
This file contains the implementation of a loader that uses the unstructured library to load PowerPoint files. It checks the version of the unstructured library and raises an error if it is not compatible. It then detects the file type and partitions the file using the appropriate method from the unstructured library.

#### reddit.py
This file implements a Reddit document loader using the `praw` package to interact with the Reddit API. It includes functions for loading posts by subreddit or by username and formatting the posts into a string. The function extracts metadata such as subreddit, title, score, and author and returns a list of documents.

#### roam.py
This file contains the implementation of a document loader called RoamLoader. This loader loads Roam directory dump from disk and returns a list of documents.

#### rtf.py
This file contains the implementation of a loader that loads rich text files using the UnstructuredFileLoader class. It checks if the version of the unstructured package is compatible and uses the partition_rtf function to partition the file into elements.

#### s3_directory.py
This file contains the implementation of a document loader for loading documents from an S3 directory. It uses the `boto3` package to interact with the S3 bucket and loads documents using the `S3FileLoader` class.

#### s3_file.py
This file contains the implementation of a loader for loading documents from an S3 file. It uses the `boto3` package to download the file from S3 and then uses the `UnstructuredFileLoader` to load the documents from the downloaded file.

#### sitemap.py
This file contains a class for loading sitemap documents and a method for parsing sitemap XML into a list of dictionaries. It allows for filtering of URLs and customization of the loading process through parameters such as filter_urls, parsing_function, and meta_function. The class can be initialized with a webpage path, a block size, a block number, and a boolean indicating whether the sitemap is a local file.

#### slack_directory.py
This file defines a `SlackDirectoryLoader` class that loads documents from a Slack directory dump. It includes methods to get a dictionary mapping channel names to their respective IDs, read JSON data from a zip subfile, convert a message to a Document object, create and return metadata for a given message and channel, and get the message source as a string.

#### spreedly.py
This file contains the `SpreedlyLoader` class which is a loader that fetches data from the Spreedly API. It uses the `BaseLoader` class and the `Document` class to fetch and return data from various endpoints of the Spreedly API. The class takes an access token and a resource as input and returns a list of documents containing the fetched data.

#### srt.py
This file contains the implementation of a loader for .srt (subtitle) files. It defines a class `SRTLoader` that inherits from `BaseLoader` and has a `load` method that uses the `pysrt` package to parse the file and return a list of `Document` objects containing the subtitle text and metadata.

#### stripe.py
This file contains the implementation of a loader that fetches data from Stripe API. It defines a `StripeLoader` class that inherits from `BaseLoader` and has a `_make_request` method that sends a request to the Stripe API and returns a list of `Document` objects containing the response data. The loader can be used to fetch data for different resources such as balance transactions, charges, customers, events, refunds, and disputes.

#### telegram.py
This file contains the implementation of a loader that loads a Telegram chat JSON dump and returns the messages as a list of `Document` objects. It also includes a helper function for converting text to `Document` objects with metadata.

#### twitter.py
This file implements a Twitter document loader using Tweepy package to access the Twitter API. It returns a list of formatted tweets and contains a Python class `TwitterTweetLoader` with methods for authentication and formatting tweets.

#### unstructured.py
This file contains implementations of loaders for unstructured files using the `unstructured` package. It includes an abstract base class `UnstructuredBaseLoader` with a method to get elements, and two subclasses `UnstructuredFileLoader` and `UnstructuredAPIFileLoader` for loading files and using the unstructured web API, respectively. The loaders return a list of `Document` objects and check the `unstructured` package version before use.

#### url.py
This file contains a Python class, `UnstructuredURLLoader`, that inherits from `BaseLoader` and loads HTML files from a list of URLs. It validates the mode and has methods for checking headers and loading files. It uses `partition` and `partition_html` from the `unstructured.partition` module to extract elements and create `Document` objects.

#### url_playwright.py
This file contains a PlaywrightURLLoader class that uses Playwright to load pages and extract unstructured HTML. It is useful for loading pages that require JavaScript to render, and allows for customization of URLs, failure handling, headless mode, and selectors to remove.

#### url_selenium.py
This file contains a Python class that implements a loader using Selenium to load pages that require JavaScript to render. It can be configured to use either Chrome or Firefox and can run in headless mode. The class creates and returns a WebDriver instance based on the specified browser and raises a ValueError if an invalid browser is specified. The `load` function loads specified URLs using Selenium and creates Document instances.

#### web_base.py
This file defines a `WebBaseLoader` class that inherits from `BaseLoader` and is used to load webpages using `urllib` and `beautifulsoup`. It includes a method to build metadata from `beautifulsoup` output and allows for multiple web paths to be loaded.

#### word_document.py
This file contains a loader for unstructured Word documents that can handle both .doc and .docx files. It uses docx2txt to load a DOCX file and partitions it at the character level. If the file is a web path, it will download it to a temporary file and use that, then clean up the temporary file after completion.

#### youtube.py
This file contains multiple implementations of a YouTube document loader for the LangChain project. It includes functions and classes to load transcripts and metadata for YouTube videos and channels using various Python packages such as `googleapiclient`, `youtube_transcript_api`, and `pytube`. The loader can be used to load documents for a specific channel or a list of video IDs.

### Directories
#### blob_loaders
The `blob_loaders` directory is for loading blobs from the local file system based on a specified directory path, glob pattern, and file suffix filter. It includes an implementation of `FileSystemBlobLoader` class in `file_system.py` and a schema for Blobs and Blob Loaders in `schema.py`. The schema provides an interface to represent raw data by either reference or value, while the `FileSystemBlobLoader` class provides a `yield_blobs` method that returns the matched blobs.

#### parsers
The `parsers` directory is for parsing various document formats such as HTML, PDF, and text. It includes a generic parser that uses mime-types to determine how to parse a blob, PDF parsers that use different libraries, a registry of default parser configurations for different mime-types, and a text parser. The directory also contains an `html` subdirectory for parsing HTML files using the Beautiful Soup library and enriching metadata with page title.

<!--- END SELFDOC --->