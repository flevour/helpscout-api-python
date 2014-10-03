helpscout-api-python
====================

Python wrapper for the Help Scout API

## Installation:
`git clone git@github.com/mccannm11/helpscout-api-python`
`cd helpscout-api-python && python setup.py install`

Example Usage: API
---------------------

```
import helpscout

client = helpscout.Client()
client.API_KEY = "your-api-key"

conversations = client.search_conversations({"query": "(* AND tag: 'your-tag')"})
for conversation in conversations.items:
  print conversation.customerEmail + "\t" + conversation.customerName

```


Field Selectors
---------------------
Field selectors are given as a list of Strings. When field selectors are used, the appropriate object is created with the fields provided.

ApiClient Methods
--------------------
Each method can accept a field selector as an addition parameter.

### Mailboxes
* mailboxes()
* mailbox(int mailbox_id)

### Folders
* folders(int mailbox_id)

### Conversations
* conversations_for_folders(int mailbox_id, int folder_id)
* conversations_for_mailbox(int mailbox_id)
* conversations_for_customerByMailbox(int mailbox_id, int customer_id)
* conversation(Integer conversation_id)

### Attachments
* attachment_data(int attachment_id)

### Customers
* customers()
* customer(int customer_id)

### Users
* users()
* users_for_mailbox(int mailbox_id)
* user(int user_id)

### Search
* search_conversations(query params)

