# Chat Application POC

## Overview
This project is a proof of concept (POC) for a chat application using the following technologies:

- **Backend**: Node.js with Express and Socket.IO
- **Frontend**: Angular
- **Database**: PostgreSQL or MySQL

## Features
- Real-time chat using WebSockets (Socket.IO).
- Chat history stored in a relational database.
- Two database tables: `chat_conversation` and `chat_message`.

## Folder Structure
```
/socket-chat
|-- backend/       # Node.js server
|-- frontend/      # Angular application
|-- README.md      # Project documentation
```

## Database Schema
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

## Setup Instructions
1. **Backend**:
   - Navigate to the `backend` folder.
   - Install dependencies: `npm install`.
   - Start the server: `npm start`.

2. **Frontend**:
   - Navigate to the `frontend` folder.
   - Install dependencies: `npm install`.
   - Start the Angular app: `ng serve`.

3. **Database**:
   - Set up a PostgreSQL or MySQL database.
   - Create the tables using the schema provided above.

## Implementation Details
- The backend will use Socket.IO for real-time communication.
- The frontend will connect to the backend via WebSocket for live chat updates.
- Chat history will be fetched from the database and displayed in the Angular app.