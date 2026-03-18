# Services

## Overview

This project follows a **microservices architecture**.  
Each service is responsible for a specific functionality.

The platform is a task marketplace, where users can post tasks and workers can complete them.

---

## Authentication Service

### Purpose
Handles user authentication and authorization.

### Responsibilities
- User registration (Signup)
- User login
- OTP verification (Email)
- Password reset
- Role management (User / Worker / Admin)

### Features
- JWT-based authentication
- Secure password handling
- Input validation

---

## Work Service

### Purpose
Manages tasks/jobs in the system.

### Responsibilities
- Create task (by user)
- View/browse tasks (by worker)
- Accept or reject tasks
- Update task status  
  (Pending → Accepted → In Progress → Completed)
- Manage categories

### Features
- Task listing with filters
- Pagination and search
- Task lifecycle management

---

## Communication Service

### Purpose
Handles real-time chat between users and workers.

### Responsibilities
- Send and receive messages
- Store chat history
- Mark messages as read
- Real-time communication

### Features
- WebSocket / Socket.IO based chat
- Unread message count
- Live updates

---

## Payment Service

### Purpose
Handles all payment-related operations.

### Responsibilities
- Process payments
- Manage worker payouts
- Handle refunds
- Track payment status

### Features
- Secure transactions
- Payment status tracking  
  (Pending, Success, Failed, Refunded)
- Order-payment linking

---

## Notification Service

### Purpose
Sends notifications to users and workers.

### Responsibilities
- Send email notifications
- Send in-app notifications
- Trigger event-based alerts  
  (task accepted, payment completed, etc.)

### Features
- Real-time notifications
- Notification history
- Read/unread status tracking

---

## Service Communication

### Methods
- REST APIs (HTTP)
- Event-driven communication (optional)

### Example Flow
1. User creates a task → Work Service  
2. Worker accepts task → Work Service  
3. Notification sent → Notification Service  
4. Chat starts → Communication Service  
5. Payment processed → Payment Service  

---

## Tech Stack (Example)

- Backend: Node.js, Express
- Database: MongoDB, PostgreSQL (for payments)
- ORM/ODM: Mongoose / Prisma
- Realtime: Socket.IO
- Authentication: JWT
- Containerization: Docker

---

## Benefits of This Architecture

- Scalable system
- Independent services
- Easy maintenance
- Clear separation of concerns
