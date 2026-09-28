# Chat Application POC

> **Status: planned, no code yet.** This repository currently contains only this README. It describes the intended design for a proof-of-concept chat application; the backend, frontend and database schema below have not been implemented.

## Overview
This project is a planned proof of concept (POC) for a real-time chat application using the following technologies:

- **Backend**: Node.js with Express and Socket.IO
- **Frontend**: Angular
- **Database**: PostgreSQL or MySQL

## Planned Features
- Real-time chat using WebSockets (Socket.IO).
- Chat history stored in a relational database.
- Two database tables: `chat_conversation` and `chat_message`.

## Planned Folder Structure
```
/socket-chat
|-- backend/       # Node.js server (not yet created)
|-- frontend/      # Angular application (not yet created)
|-- README.md      # Project documentation
```

## Planned Database Schema
### Table: `chat_conversation`
- `id` (Primary Key): Unique identifier for the conversation.
- `name`: Name of the conversation (e.g., group name).
- `created_at`: Timestamp when the conversation was created.

### Table: `chat_message`
- `id` (Primary Key): Unique identifier for the message.
- `conversation_id` (Foreign Key): Links to `chat_conversation`.
- `sender`: Name or ID of the message sender.
- `message`: The chat message content.
- `sent_at`: Timestamp when the message was sent.

## Planned Implementation
- The backend will use Socket.IO for real-time communication.
- The frontend will connect to the backend via WebSocket, using the `socket.io-client` package, for live chat updates.
- Chat history will be fetched from the database and displayed in the Angular app.

## Setup
There is nothing to install or run yet. Setup instructions will be added once the `backend/` and `frontend/` code is committed.
