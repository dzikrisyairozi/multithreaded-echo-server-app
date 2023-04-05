## Multi-Threaded Echo Server

This is a multi-threaded echo server written in Java. The server listens on port 5000 for incoming connections from clients and creates a new thread for each client connection. Each thread handles input/output for a single client and does not affect the operation of other client connections.

When a client connects to the server, the server sends a message to the console indicating the client's IP address. The client can then send messages to the server, which are echoed back to the client.

This server uses the Java `ServerSocket` class to listen for incoming connections and the `Thread` class to handle each client connection. The `ClientHandler` class implements the `Runnable` interface and contains the logic for handling a single client connection.

This multi-threaded server is useful for applications that require handling multiple client connections simultaneously, such as chat applications, online games, or distributed computing systems. By using a separate thread for each client connection, the server can handle many client connections without slowing down or crashing.

## Requirements

To run this server, you need to have Java installed on your system.

## Usage

To run the server, compile the `App.java` file and run the resulting `.class` file using the java command:

```java
javac App.java
java App
```

The server will start listening for incoming connections on port 5000. You can connect to the server using a telnet client or any other client that can connect to a server socket.

To test the server, you can open a telnet client and connect to the server using the following command:

```lua
telnet localhost 5000
```

You should see a message indicating that the client has connected to the server. You can then type messages into the telnet client and they will be echoed back to you by the server.

To stop the server, you can press Ctrl + C in the console window where the server is running.

