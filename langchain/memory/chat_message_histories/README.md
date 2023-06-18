<!--- START SELFDOC --->
## SelfDoc
_Auto-generated code documentation to make the repository easier to navigate and contribute to._

_Last Updated: 2023-06-18_

The `chat_message_histories` directory is for storing various implementations of chat message history classes. These classes include Cassandra, Cosmos DB, DynamoDB, file-based, Firestore, PostgreSQL, Redis, SQL, and Zep. Each file contains the implementation of the respective class, including functions to interact with the database or file system to store and retrieve chat messages, as well as methods to clear session memory.

### Files
#### __init__.py
This file exports all the available chat message history classes in the `langchain/memory/chat_message_histories` directory.

#### cassandra.py
This file contains the implementation of `CassandraChatMessageHistory`, a class that establishes a connection to a Cassandra database for storing and retrieving chat message histories. It includes functions for creating a table, retrieving messages, appending new messages to the table, and clearing all messages associated with a specific session ID.

#### cosmos_db.py
This file contains the implementation of `CosmosDBChatMessageHistory`, a class that represents a chat history backed by Azure CosmosDB. It includes functions to ensure the database is ready, create a container if it doesn't exist, and load and upsert messages. The class requires a cosmos endpoint, database, and container, as well as a session ID and user ID. A credential or connection string must also be provided.

#### dynamodb.py
This file contains the implementation of a chat message history that stores history in AWS DynamoDB. It includes methods to retrieve messages from the table, add user and AI messages, and append messages to the record in DynamoDB.

#### firestore.py
This file implements a `FirestoreChatMessageHistory` class for managing chat message histories using Google Firestore. It includes functions for loading, adding, updating, and clearing chat messages in both memory and Firestore.

#### in_memory.py
This file defines a `ChatMessageHistory` class that inherits from `BaseChatMessageHistory` and `BaseModel`. It provides methods to add user and AI messages to a list of messages, as well as a method to clear the list. The messages are stored in memory.

#### postgres.py
This file contains the implementation of `PostgresChatMessageHistory` class, which provides methods to interact with a PostgreSQL database to store and retrieve chat messages. It includes functions to add user and AI messages to the database, retrieve all messages for a given session ID, and clear session memory. The class also has a destructor to close the cursor and connection.

#### redis.py
This file contains the implementation of `RedisChatMessageHistory`, a class that inherits from `BaseChatMessageHistory` and provides methods to interact with Redis to store and retrieve chat messages. It uses the `redis` python package and provides methods to add user and AI messages, retrieve messages, and append messages to the Redis record. Additionally, it contains a `clear` function that clears session memory from Redis by deleting a specified key.

#### sql.py
This file contains the implementation of `SQLChatMessageHistory` class which is a subclass of `BaseChatMessageHistory`. It provides functionality to store and retrieve chat messages from an SQL database using SQLAlchemy. The `messages` property retrieves all messages from the database.

<!--- END SELFDOC --->