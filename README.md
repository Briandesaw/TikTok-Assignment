# Real-Time Messager App with GoLang

This is a completed project for backend assignment of 2023 TikTok Tech Immersion with the use of Redis as the main database for storing messages and users.

## HTTP Server
The main package sets up an HTTP server that listens for incoming requests and provides two endpoints for sending and pulling messages. It uses the hertz framework for building HTTP servers and the kitex framework for RPC communication with the backend server.

The server is initialized with default configurations and starts listening on port 8080. It also establishes a connection with the backend RPC server using the imservice client.

## RTC Server
The main package sets up an RPC server using the kitex framework to handle incoming RPC requests from clients. It also initializes a Redis client for data storage and retrieval.

The server is initialized with the following configurations:

- It establishes a connection with the Etcd registry for service discovery.
- It creates a new RPC server with the implementation of the IMServiceImpl service.
- It runs the server, listening for incoming RPC requests.

## Redis Database
This in-memory data structure store helps to save messages by users so that it can be retrieved by the pull requests when needed.
