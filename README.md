# 💬 Real-Time Chat Application (Socket.io)

## 🚀 Overview
This project is a **real-time chat application** built using **Node.js**, **Express**, **Socket.io**, and **React**.  
It demonstrates **bidirectional, low-latency communication** between clients and the server — supporting live messaging, typing indicators, online/offline status, and private chats.

This assignment was developed as part of **Week 5: Real-Time Communication with Socket.io**.

---

## 🧠 Objectives
- Implement **real-time messaging** using Socket.io.  
- Enable **user presence tracking** (join/leave notifications).  
- Build a **global chat room** with typing indicators.  
- Add **private messaging** and message history.  
- Implement **notifications** and online user management.

---

## 🏗️ Project Structure

socketio-chat/
<br>├── client/ # React front-end</br>
<br>│ ├── public/ # Static assets</br>
<br>│ ├── src/ # React source code</br>
<br>│ │ ├── components/ # Chat UI components</br>
<br>│ │ ├── context/ # React context providers</br>
<br>│ │ ├── hooks/ # Custom React hooks</br>
<br>│ │ ├── pages/ # Page components</br>
<br>│ │ ├── socket/ # Socket.io client setup (socket.js)</br>
<br>│ │ └── App.jsx # Main application entry</br>
<br>│ └── package.json # Client dependencies</br>
<br>├── server/ # Node.js back-end</br>
<br>│ ├── config/ # Environment config</br>
<br>│ ├── controllers/ # Socket event handlers</br>
<br>│ ├── models/ # Data models</br>
<br>│ ├── socket/ # Socket.io setup (server.js integrates here)</br>
<br>│ ├── utils/ # Utility functions</br>
<br>│ ├── server.js # Main server entry file</br>
<br>│ └── package.json # Server dependencies</br>
<br>└── README.md # Project documentation</br>


---

## ⚙️ Setup Instructions

### 1️⃣ Prerequisites
Make sure you have installed:
- **Node.js v18+**
- **npm v9+**
- **MongoDB** (optional if persistent storage is added)

---

### 2️⃣ Clone the Repository
```bash
git clone https://github.comPLP-MERN-Stack-Developmentreal-time-communication-with-socket-io-Jsews.git
cd real-time-communication-with-socket-io

3️⃣ Setup the Server
cd server
npm install


Create a .env file in the /server folder:

PORT=5000
CLIENT_URL=http://localhost:3000


Start the server:

npm run dev


The server should now be running on:

http://localhost:5000

4️⃣ Setup the Client
cd ../client
npm install
npm run dev


The client will start at:

http://localhost:5173

💡 Features Implemented

| Feature                 | Description                                         |
| ----------------------- | --------------------------------------------------- |
| **Real-Time Messaging** | Instantly send and receive messages using Socket.io |
| **User Presence**       | Displays online/offline users and join/leave events |
| **Typing Indicators**   | Shows when users are typing messages                |
| **Private Messaging**   | Send direct messages between users                  |
| **Message History**     | Stores messages in memory for quick retrieval       |
| **Notifications**       | Real-time and browser-based message notifications   |
| **Responsive UI**       | Works smoothly on both desktop and mobile devices   |
| **Error Handling**      | Handles connection loss and reconnection gracefully |


🧩 Socket.io Events
Client → Server
| Event             | Payload           | Description                               |
| ----------------- | ----------------- | ----------------------------------------- |
| `user_join`       | `username`        | Notify server of a new user               |
| `send_message`    | `{ message }`     | Send a chat message to everyone           |
| `private_message` | `{ to, message }` | Send a private message to a specific user |
| `typing`          | `boolean`         | Indicate if user is typing or not         |

Server → Client
| Event             | Payload           | Description                         |
| ----------------- | ----------------- | ----------------------------------- |
| `receive_message` | `{ messageData }` | Broadcasts new message to all users |
| `private_message` | `{ messageData }` | Sends direct message to recipient   |
| `user_list`       | `[users]`         | Updates online user list            |
| `user_joined`     | `{ username }`    | Announces user joining              |
| `user_left`       | `{ username }`    | Announces user leaving              |
| `typing_users`    | `[usernames]`     | Shows who is typing                 |

🧪 Expected Outcome

A fully functional real-time chat app with:

Global chat

Private messages

Typing indicators

Online/offline tracking


🧑‍💻 Author

Janice Tusiime Sewava
🌐 Project: Real-Time Communication with Socket.io

🧾 License

This project is licensed under the MIT License — free to use and modify for educational purposes.