# RealTime-ChatApp

ChatApp is a real-time chat application built using **Spring Boot** and **Thymeleaf** for the frontend. The application allows users to send and receive chat messages in real-time. It leverages **Spring WebSocket** for bidirectional communication between the client and the server.

## Setup and Background

ChatApp is a basic real-time messaging application designed to provide instant communication between users. The app is built on the following technologies:

- **Backend**: The backend is built using **Spring Boot** and **Spring WebSocket** to provide real-time communication over WebSocket connections.
- **Frontend**: The frontend is designed using **Thymeleaf**, **HTML**, **CSS**, and **JavaScript** for dynamic content rendering.
- **WebSocket**: The app uses WebSockets to establish a continuous connection between the server and the client for real-time communication.

### Purpose

The purpose of this project is to showcase how to integrate **Spring WebSocket** with **Thymeleaf** to create a chat interface that allows for real-time communication. Users can send messages, and other connected users will receive them instantly.

### Key Features

- **Real-time Messaging**: Chat in real-time with other users.
- **WebSocket Integration**: Bidirectional communication using WebSocket.
- **Thymeleaf Frontend**: Simple and dynamic chat interface built with Thymeleaf templating engine, HTML, CSS, and JavaScript.
- **Spring Boot**: Backend built using Spring Boot for ease of use and rapid development.

## Technologies Used

- **Backend**: Spring Boot, Spring WebSocket
- **Frontend**: Thymeleaf, HTML, CSS, JavaScript
- **Build Tool**: Maven for backend build management

## Prerequisites

Before setting up the project, ensure that you have the following installed:

- **Java 11+**: Java Development Kit (JDK)
- **Maven**: Build tool for managing dependencies and building the project
- **Web Browser**: For accessing the frontend (e.g., Chrome, Firefox)

## Installation Instructions

### 1. Clone the repository:
First, clone the repository to your local machine.

```bash
git clone https://github.com/yourusername/ChatApp.git
cd ChatApp
2. Set up the Backend
Navigate to the ChatApp directory:

bash
cd ChatApp
Build the application using Maven:

bash
mvn clean install
Configure application settings in src/main/resources/application.properties if needed (e.g., server port, WebSocket settings).

Run the application:

bash
mvn spring-boot:run
The backend should now be running on http://localhost:8080.

3. Access the Chat Interface
Open src/main/resources/templates/chat.html in your web browser to start chatting. This is the Thymeleaf-powered chat interface that connects to the WebSocket server and allows you to send and receive messages in real-time.
Usage
Start the server: Run the Spring Boot application using mvn spring-boot:run.
Open the chat interface: Visit http://localhost:8080/chat.html to access the chat interface.
Send a message: Type a message in the input field and click "Send" to send it.
Receive messages: Any message sent by a connected user will appear in real-time on the interface.

# WebSocket Communication
WebSocket URL: The backend communicates with the frontend using WebSockets.
Endpoint: /chat (configured in the WebSocketConfig.java class).
Messages: The server receives messages from the client and broadcasts them to all connected clients in real-time.
Frontend (Thymeleaf)
chat.html: The main chat interface built using Thymeleaf templates. It includes dynamic rendering of chat messages and integrates with the WebSocket server.
chat.css: The styling for the chat interface.
chat.js: Handles the JavaScript logic for connecting to the WebSocket server and sending/receiving messages.

# Future Enhancements
Database Integration: Currently, the chat messages are not stored in a database. Future updates will include message persistence using a relational database like MySQL or PostgreSQL.
User Authentication: Adding user authentication to allow for private chats and user profiles.
Frontend Improvements: Enhance the frontend using more advanced features such as user status, message notifications, and custom UI components.
API Documentation
Currently, there are no separate API endpoints as the communication happens via WebSockets. The WebSocket configuration in WebSocketConfig.java defines the endpoint and the message handling methods.

# Contributing
If you'd like to contribute to this project, feel free to fork the repository, create a branch for your feature, and submit a pull request with your changes.

# Steps for Contributing:
Fork the repository.
Create a new branch for your feature (git checkout -b feature-name).
Make your changes and commit them (git commit -m "Add new feature").
Push to the branch (git push origin feature-name).
Open a pull request to merge your changes into the main branch.
