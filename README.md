
Server Initialization:
The code initializes a Node.js server using Socket.IO on port 8000.
User Connection Handling:

When a new user connects (connection event), the server listens for the event 'new-user-joined' and broadcasts to other users when a new user joins.
Message Broadcasting:

When a user sends a message (send event), the server broadcasts the message to all connected users except the sender.
User Disconnection Handling:

When a user disconnects (disconnect event), the server broadcasts a 'left' event to inform other users about the departure and removes the user from the list of connected users.
User Data Storage:

The server maintains a simple in-memory storage (users object) to associate user names with their socket IDs. This allows the server to broadcast meaningful user-related events.
