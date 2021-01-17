# chat_system
"""
This is a typical ​distributed client-server system​, where multiple clients interact with a central server. Conceptually, this is how wechat is constructed. Clients interact with each other ​as if directly, what actually happens is, however, the server is passing messages back and forth, and adds other functionalities (such as indexing history). There can be multiple clients, each of them is either idle, or actively participates in one chat session with a group of other clients. Think of a client as an ordinary user of WeChat. Our system is simple: ​it allows chatting in one group only​​.

The server has a few extra modules:

A membership management module, to look at who is chatting with whom, for example.
A chat log, one per user. This allows a user to search her past chatting history with keywords.
A sonnet database, so a user can ask for a poem when she is not chatting.
Files that make up the system, client side:

chat_cmdl_client.py​​, ​chat_client_class.py​​
chat_state_machine.py​​: handles main events interacting with the chat system.
Files that make up the system, server side

chat_server.py​​
indexer.py​​: indexes messages and sonnets.
AllSonnets.txt, roman.txt.pk​​: sonnets and roman-to-numeral conversion, given.
chat_group.py​​: membership handling.
index_util.py​​ and ​chat_util.py​​ are utility files/modules we provide. See ​appendix​ on how to run chat clients and server on separate machines. When server starts, you should have this screenshot:

When completed, you can run it as the followings:

On one console: “python chat_server.py”. This starts the server.
On another console: “python chat_cmdl_client.py”. This starts a client

"""
