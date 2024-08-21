# Project Name: Microservices-grpc

## Overview

This project is a microservices architecture consisting of:

- **API Gateway (Golang)**
- **Auth Service (Node.js)**
- **Search Service (Golang + OpenSearch)**
- **Message Queue (RabbitMQ)**
- **Caching (Redis)**

## Architecture Diagram

![Architecture Diagram](path/to/your/image.png)

## Features

- **Authentication**: User registration and login with JWT.
- **Search**: Full-text search using OpenSearch and gRPC.
- **API Gateway**: Manages incoming requests and routes them to the appropriate microservice.

## Technologies Used

- **Node.js**: API Gateway and Auth Service.
- **Golang**: Search Service using gRPC.
- **OpenSearch**: Search engine for fast and scalable searches.
- **Docker Compose**: To orchestrate the microservices.
- **gRPC**: Communication between microservices.

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Docker
- Docker Compose
- Node.js
- Golang

### Setup

1. **Clone the repository**:

   ```bash
   git clone https://github.com/yourusername/yourproject.git
   cd yourproject
   ```

2. **Build and run the services using Docker Compose**:

   ```bash
   docker-compose up --build
   ```

3. **Access the services**:

   - API Gateway: `http://localhost:3000`
   - Auth Service: `http://localhost:4000`
   - Search Service: `localhost:50051` (gRPC)

### Usage

- **Register a user**:

  ```bash
  curl -X POST http://localhost:3000/auth/register -H "Content-Type: application/json" -d '{"username": "user1", "password": "pass123"}'
  ```

- **Login to get a JWT token**:

  ```bash
  curl -X POST http://localhost:3000/auth/login -H "Content-Type: application/json" -d '{"username": "user1", "password": "pass123"}'
  ```

- **Search using the Search Service (gRPC call)**:

  Implement the client logic in your preferred language (e.g., Node.js, Golang) using the `.proto` file.

### Project Structure

```plaintext
.
├── api-gateway
│   ├── Dockerfile
│   ├── index.js
│   └── ...
├── auth-service
│   ├── Dockerfile
│   ├── server.js
│   └── ...
├── search-service
│   ├── Dockerfile
│   ├── main.go
│   ├── search.proto
│   └── ...
├── docker-compose.yml
└── README.md
```
