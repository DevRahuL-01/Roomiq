# 💬 Full Stack Real-Time Chat App — React + Vite + Spring Boot

A complete **real-time chat application** built using **React (Vite)** on the frontend and **Spring Boot** on the backend.  
Supports **real-time bidirectional messaging** using **WebSockets (STOMP)** and persists chat history in **MongoDB**.

---

## 🧱 Tech Stack

### 🖥️ Frontend

- React 19 (Vite)
- Tailwind CSS v4
- React Router DOM
- StompJS & SockJS-client (WebSockets)
- Axios
- React Hot Toast

### ⚙️ Backend

- Spring Boot 3.5.0
- Spring WebSocket / STOMP
- Spring Data MongoDB
- Spring Web (REST APIs)
- Lombok

---

## 📸 Screenshots

### Create or Join Room
![Chat Interface](https://github.com/DevRahuL-01/Roomiq/blob/main/screenshots/create-or-join-room.png)

### Chat Room 
![Chat Interface](https://github.com/DevRahuL-01/Roomiq/blob/main/screenshots/chat-room.png)

---

## 📁 Project Structure

```text
Roomiq Project/
│
├── roomiq/                   # Spring Boot Backend
│   ├── src/
│   ├── pom.xml
│   └── application.properties (or yml)
│
├── roomiq-frontend/          # React + Vite Frontend
│   ├── src/
│   ├── package.json
│   └── vite.config.js
│
└── README.md
```

---

## ⚙️ Backend Setup (Spring Boot)

### 🧩 Prerequisites

- Java 17+
- Maven 3.9+ (or use provided `mvnw`)
- MongoDB (Running locally or MongoDB Atlas)
- Git

### 🧰 Steps to Run Backend

1. Navigate to the backend folder:

   ```bash
   cd roomiq
   ```

2. Ensure your MongoDB instance is running locally on the default port `27017` (or configure your `application.properties` accordingly).

3. Run the Spring Boot app:

   ```bash
   # On macOS/Linux
   ./mvnw spring-boot:run

   # On Windows
   mvnw.cmd spring-boot:run
   ```

📍 Backend runs on **http://localhost:8080**

---

## 💻 Frontend Setup (React + Vite)

### 🧩 Prerequisites

- Node.js 18+
- npm / yarn / pnpm

### ⚙️ Steps to Run Frontend

1. Navigate to frontend directory:

   ```bash
   cd roomiq-frontend
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start development server:

   ```bash
   npm run dev
   ```

📍 Frontend runs on **http://localhost:5173**

---

## 🔗 Communication Flow

1. **Connection Establishment:**
   - Client initializes a WebSocket connection to the Spring Boot server using SockJS and STOMP.
   
2. **Subscription:**
   - The user subscribes to specific STOMP topics (e.g., `/topic/public` for global chat or `/user/queue/messages` for private chat).

3. **Message Broadcasting:**
   - When a user sends a message, it is sent to a backend application destination (e.g., `/app/chat.sendMessage`).
   - The backend processes the message, optionally saves it to MongoDB, and broadcasts it to all subscribed clients.

---

## 🧰 Common Commands

| Task            | Command                         | Directory |
| --------------- | ------------------------------- | --------- |
| Run backend     | `./mvnw spring-boot:run`        | `roomiq` |
| Package backend | `./mvnw clean package`          | `roomiq` |
| Run frontend    | `npm run dev`                   | `roomiq-frontend` |
| Build frontend  | `npm run build`                 | `roomiq-frontend` |


---

## 🧑‍💻 Author

**Rahul Nanhore**  
*Full Stack Developer*  
🌐 [www.linkedin.com/in/rahulnanhore](#)  
🐙 [github.com/rahulnanhore](#)  

---

⭐ **If this project helped you, consider giving it a star!**
