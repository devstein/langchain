<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `blob_loaders` directory is for loading blobs from the local file system based on a specified directory path, glob pattern, and file suffix filter. It includes an implementation of `FileSystemBlobLoader` class in `file_system.py` and a schema for Blobs and Blob Loaders in `schema.py`. The schema provides an interface to represent raw data by either reference or value, while the `FileSystemBlobLoader` class provides a `yield_blobs` method that returns the matched blobs.

### Files
#### __init__.py
This file is the initialization file for the `blob_loaders` directory. It imports the `FileSystemBlobLoader` class from `file_system.py` and the `Blob` and `BlobLoader` classes from `schema.py`. These classes are then added to the `__all__` list, which specifies the public API of this module.

#### schema.py
This file defines a schema for Blobs and Blob Loaders, providing an interface to represent raw data by either reference or value. It includes a `Blob` class with methods to materialize the blob in different representations and a root validator to verify that either data or path is provided. Additionally, it defines the `BlobLoader` abstract class as an interface for loading raw content from a storage system and returning it as a stream of `Blob` instances.

<!--- END SELFDOC --->