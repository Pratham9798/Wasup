Instructions on how to run the server and client applications- 

Running the Server:

Navigate to the directory containing the server application.
Install dependencies by running: npm install.
Run the server application using the command: node server.js.
The server will start listening for incoming connections on a specified port.

Running the Client:

Navigate to the directory containing the client application.
Install dependencies by running: npm install.
Run the client application using the command: node client.js.
The client will prompt you to enter the server's IP address and port number.
Once connected, you can start sending and receiving messages in real-time.

A brief description of the application's architecture and how concurrency is handled-

Application Architecture:

The chat application follows a client-server architecture using Node.js for the server-side logic and Socket.io for real-time communication between clients and the server. 
Socket.io enables bidirectional communication between the client and server, allowing messages to be sent and received instantly without the need for polling.

Concurrency Handling:

- Event-Driven Architecture: Node.js follows an event-driven, non-blocking I/O model, allowing the server to handle multiple client connections concurrently without blocking the main thread.
   This is achieved through asynchronous event handling using event emitters and callbacks.

- Socket.io Rooms: Socket.io allows clients to join different rooms, enabling the server to handle multiple chat rooms or private conversations concurrently.
  Each room acts as an isolated communication channel, ensuring that messages are only broadcasted to clients within the same room.

 - Session Management: The server manages client sessions using unique identifiers (socket IDs) assigned to each client upon connection.
  This allows the server to track and manage client connections, handle disconnections gracefully, and maintain the state of active rooms and participants.


Any assumptions or design choices you made and why-

Real-Time Communication: The application prioritizes real-time communication, allowing users to exchange messages instantly without the need to refresh the page or wait for server responses. 
This enhances the user experience and fosters seamless interaction between participants.

Basic User Authentication: The application does not include user authentication or authorization mechanisms.
All clients are treated as anonymous users with equal access to chat rooms.
Implementing authentication would add complexity and is beyond the scope of this basic implementation.
