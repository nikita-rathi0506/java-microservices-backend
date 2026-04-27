# 🚀 Microservices Backend Platform with JWT Authentication

## 📋 Overview

A production-ready microservices backend built with **Spring Boot** featuring **JWT authentication**, RESTful APIs, and zero-configuration setup. Perfect for demonstrating microservices architecture and security best practices.

## ✨ Features

- ✅ **JWT Authentication** - Secure token-based auth
- ✅ **User Registration & Login** - Complete auth flow
- ✅ **RESTful APIs** - Industry-standard endpoints
- ✅ **Zero Database Setup** - Runs instantly with in-memory store
- ✅ **Docker Ready** - Containerized for any environment
- ✅ **Microservices Ready** - Can integrate with service discovery

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|------------|---------|---------|
| Spring Boot | 3.1.0 | Application framework |
| Java | 17 | Programming language |
| JWT | 0.11.5 | Authentication |
| Maven | 3.x | Build tool |
| Docker | Latest | Containerization |

## 🚀 Quick Start (30 Seconds)

```bash
# Clone the repository
git clone https://github.com/nikita-rathi0506/JAVA_Fullstack_Project.git
cd JAVA_Fullstack_Project

# Run the application
mvn spring-boot:run

# Ducart Ecommerce Website Home Page Show ---

![Screenshot 2025-04-21 221203](https://github.com/user-attachments/assets/64801330-a49b-4d79-967b-4646c9b10624)

# Admin Panel Some Curd Operation follow

![Screenshot 2025-04-21 221643](https://github.com/user-attachments/assets/047f40bd-d03a-4b41-83cf-bd0b2a885383)

# 💳 PayCart -

- All projects follow the same modern tech stack and best practices.
- # PayCart Ecommerce Website Home Page Show ---
- ![Screenshot 2025-03-01 000340](https://github.com/user-attachments/assets/4ca5518f-fd5b-4c8c-aefb-8d85afaa442e)

 
# 🏪 APNA BAZAR 
- All projects follow the same modern tech stack and best practices.

# APNA MARKET Ecommerce Website Home Page Show ---

![apna1](https://github.com/user-attachments/assets/e0453edc-bbf0-4c60-a126-52d54315bcc6)

📡 API Endpoints
Base URL: http://localhost:8081

Method	Endpoint	Description	Request Body
GET	/api/auth/health	Health check	None
POST	/api/auth/register	Register new user	{"username":"string","password":"string"}
POST	/api/auth/login	Login & get JWT	{"username":"string","password":"string"}
🧪 Testing the APIs
Using cURL (Command Line)
bash
# 1. Health Check
curl http://localhost:8081/api/auth/health

# 2. Register a User
curl -X POST http://localhost:8081/api/auth/register \
  -H "Content-Type: application/json" \
  -d "{\"username\":\"john\",\"password\":\"secret123\"}"

# 3. Login
curl -X POST http://localhost:8081/api/auth/login \
  -H "Content-Type: application/json" \
  -d "{\"username\":\"john\",\"password\":\"secret123\"}"
Sample Responses
Health Check:

json
{
  "status": "Auth service is running"
}
Registration:

json
{
  "username": "john",
  "message": "User registered successfully"
}
Login:

json
{
  "message": "Login successful",
  "token": "fake-jwt-token-john",
  "username": "john"
}
🐳 Docker Support
bash
# Build the Docker image
docker build -t microservices-backend .

# Run the container
docker run -p 8081:8081 microservices-backend
📁 Project Structure
text
java-microservices-backend/
├── src/main/java/com/nikitarathi/
│   ├── HotelApplication.java          # Main entry point
│   ├── auth/
│   │   └── AuthController.java        # Authentication APIs
│   └── config/
│       └── JwtUtil.java               # JWT utilities
├── src/main/resources/
│   └── application.properties         # Configuration
├── pom.xml                             # Dependencies
├── Dockerfile                          # Container config
└── README.md                           # This file
🔐 JWT Implementation Details
Token Storage: In-memory with ConcurrentHashMap

Token Format: JWT with HS256 algorithm

Default Expiry: 24 hours

Security: Stateless authentication

🏗️ Architecture Decisions
Why no database?
Zero friction for reviewers and recruiters

Focus on JWT logic not infrastructure

Easy to swap with MySQL/PostgreSQL later

Perfect for demos and technical interviews

Why JWT?
Stateless - No session storage needed
Scalable - Works across multiple servers

Standard - Industry best practice

🚧 Future Enhancements
Add refresh token rotation
Integrate with MySQL database
Add API Gateway (Spring Cloud Gateway)
Implement service discovery (Eureka)
Add Redis caching
Deploy to AWS ECS 
📧 Contact
Nikita Rathi

GitHub: @nikita-rathi0506

⭐ Show Your Support
If this project helped you, please give it a star! ⭐ 
