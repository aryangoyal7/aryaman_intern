# Chatting web-app assignment | I'mbesideyou | Aryaman Sharma | IIT Bombay | BS maths

This repository is a submission for the internship assignment - MERN stack based chatting web-app with features such as JWT authentication, Group chat, real time messages and a user-friendly interface.

## How to run the project

In the frontend directory, you can run:

### npm install
 followed by 
 
### npm start

\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.


System Design Overview
The Chat Application is built on a MERN (MongoDB, Express.js, React.js, Node.js) stack, providing a robust and real-time messaging experience for users. The system architecture revolves around several key components:

Backend Server (Node.js & Express.js):

The backend server handles HTTP requests and responses, implementing various API endpoints for user authentication, chat creation, messaging, and group management.
Express.js, a minimalist web framework for Node.js, is utilized for routing and handling API requests.
Database (MongoDB & Mongoose ODM):

MongoDB, a NoSQL database, is employed to store user data, chat information, and messages. It provides flexibility and scalability for managing large volumes of data.
Mongoose ODM (Object Data Modeling) is used to interact with MongoDB, providing a schema-based solution for modeling application data.
Frontend (React.js & Redux):

The frontend is developed using React.js, a popular JavaScript library for building user interfaces. React components enable the creation of a dynamic and responsive user interface.
Redux, a state management library, is integrated to manage the application's state, ensuring consistent data flow and state synchronization across components.
Real-Time Communication (Socket.io):

Socket.io is employed to enable real-time bidirectional event-based communication. It facilitates instant message delivery and updates, ensuring a seamless chat experience for users.
Socket.io enables features such as real-time message synchronization and dynamic user presence indicators.
Authentication and Security:

User authentication is implemented using JSON Web Tokens (JWT), providing secure access to protected routes and ensuring user identity verification.

User Management and Search:

The system includes user management functionalities, allowing users to register, log in, and manage their profiles.
User search is implemented, enabling users to find and connect with others based on their names or email addresses.
Group Chat Functionality:

Users can create group chats, invite members, and manage group chat settings.
Group chat features include renaming chats, adding or removing users, and dynamic updates to group member lists.

## Features

- **Chat Rooms:** Users can create chat rooms with specific names.
- **Group Chats:** Users can create group chat rooms and invite multiple users to join.
- **Real-time Messaging:** Messages are delivered in real-time, providing a seamless chatting experience.
- **User Authentication:** Users can sign up, log in, and manage their profiles.
- **Message Read Status:** Users can see if their messages have been read by others.


## Technologies Used

- **Frontend:** React.js, Redux, Socket.io
- **Backend:** Node.js, Express.js
- **Database:** MongoDB (Mongoose ODM)
- **Authentication:** JSON Web Tokens (JWT)


# Chat Application APIs

Chat Application API is the backend service for a MERN stack-based web application that enables users to create chat rooms, send messages, and manage conversations.

## Endpoints

### 1. Access Chat

- **Description:** Create or fetch One to One Chat
- **Route:** `POST /api/chat/`
- **Access:** Protected
- **Request:**
  - `userId`: User ID of the recipient
- **Response:**
  - Returns the existing chat if one exists, otherwise creates a new chat.

### 2. Fetch Chats

- **Description:** Fetch all chats for a user
- **Route:** `GET /api/chat/`
- **Access:** Protected
- **Response:**
  - Returns an array of chats associated with the user.

### 3. Create Group Chat

- **Description:** Create a New Group Chat
- **Route:** `POST /api/chat/group`
- **Access:** Protected
- **Request:**
  - `name`: Name of the group chat
  - `users`: Array of user IDs to be added to the group
- **Response:**
  - Returns the newly created group chat.

### 4. Rename Group

- **Description:** Rename a Group Chat
- **Route:** `PUT /api/chat/rename`
- **Access:** Protected
- **Request:**
  - `chatId`: ID of the chat to be renamed
  - `chatName`: New name for the group chat
- **Response:**
  - Returns the updated group chat.

### 5. Remove User from Group

- **Description:** Remove a user from a Group Chat
- **Route:** `PUT /api/chat/groupremove`
- **Access:** Protected
- **Request:**
  - `chatId`: ID of the chat
  - `userId`: ID of the user to be removed
- **Response:**
  - Returns the updated group chat after removing the user.

### 6. Add User to Group / Leave Group

- **Description:** Add a user to a Group Chat or Allow user to leave a Group Chat
- **Route:** `PUT /api/chat/groupadd`
- **Access:** Protected
- **Request:**
  - `chatId`: ID of the chat
  - `userId`: ID of the user to be added or removed
- **Response:**
  - Returns the updated group chat after adding or removing the user.

### 7. Get All Messages

- **Description:** Get all Messages for a Chat
- **Route:** `GET /api/message/:chatId`
- **Access:** Protected
- **Response:**
  - Returns an array of messages associated with the specified chat.

### 8. Send Message

- **Description:** Create New Message
- **Route:** `POST /api/message/`
- **Access:** Protected
- **Request:**
  - `content`: Content of the message
  - `chatId`: ID of the chat where the message is sent
- **Response:**
  - Returns the newly created message.

### 9. Get or Search All Users

- **Description:** Get or Search all users
- **Route:** `GET /api/user?search=`
- **Access:** Public
- **Response:**
  - Returns an array of users based on the search query.

### 10. Register New User

- **Description:** Register a new user
- **Route:** `POST /api/user/`
- **Access:** Public
- **Request:**
  - `name`: Name of the user
  - `email`: Email address of the user
  - `password`: Password for the user
  - `pic`: Profile picture URL (Optional)
- **Response:**
  - Returns user data along with an authentication token upon successful registration.

### 11. Authenticate User

- **Description:** Authenticate the user
- **Route:** `POST /api/users/login`
- **Access:** Public
- **Request:**
  - `email`: Email address of the user
  - `password`: Password for the user
- **Response:**
  - Returns user data along with an authentication token upon successful authentication.



Following are some of the screenshots of the project and can act as a tutorial as well on how to use the web-app.




