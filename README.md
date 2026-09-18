# Fitness Application — Spring Boot AI Microservices

A full-stack fitness application built using **Java, Spring Boot, Spring Cloud, React, and AI-powered microservices**. The project demonstrates a production-oriented microservices architecture with service discovery, authentication, asynchronous communication, and AI-based fitness analysis.

## 🚀 Key Features

- **Microservices Architecture** — Independent services for user management, activity tracking, and AI-powered recommendations.
- **AI-Powered Fitness Analysis** — Uses Spring AI and LLMs to analyze fitness activities and generate personalized insights.
- **Authentication & Authorization** — Secure user authentication using **OAuth2 and Keycloak**.
- **Service Discovery** — Eureka-based service registration and discovery between microservices.
- **API Gateway** — Centralized entry point for routing requests to backend services.
- **Event-Driven Communication** — Apache Kafka for asynchronous communication between services.
- **Database Integration** — PostgreSQL/MySQL for transactional data and MongoDB for activity-related data.
- **REST APIs** — Backend services expose scalable RESTful APIs for frontend and inter-service communication.
- **Containerized Architecture** — Services can be independently deployed and scaled.

## 🏗️ Architecture

```text
                         ┌─────────────────┐
                         │     React UI    │
                         └────────┬────────┘
                                  │
                                  ▼
                         ┌─────────────────┐
                         │   API Gateway   │
                         └────────┬────────┘
                                  │
              ┌───────────────────┼───────────────────┐
              │                   │                   │
              ▼                   ▼                   ▼
      ┌──────────────┐    ┌──────────────┐    ┌──────────────┐
      │ User Service │    │Activity      │    │ AI Service   │
      │              │    │Service       │    │              │
      └──────┬───────┘    └──────┬───────┘    └──────┬───────┘
             │                   │                   │
             ▼                   ▼                   ▼
       ┌──────────┐        ┌──────────┐       ┌─────────────┐
       │ SQL DB   │        │ MongoDB  │       │ LLM / AI    │
       └──────────┘        └──────────┘       └─────────────┘

                         ┌─────────────────┐
                         │      Kafka      │
                         │ Event Streaming │
                         └─────────────────┘

                         ┌─────────────────┐
                         │     Eureka     │
                         │ Service Discovery│
                         └─────────────────┘
```

## 🛠️ Technology Stack

### Backend

- **Java**
- **Spring Boot**
- **Spring Web**
- **Spring Data JPA**
- **Spring Cloud**
- **Spring AI**
- **Spring Security**
- **OAuth2**
- **Keycloak**

### Microservices & Infrastructure

- **Spring Cloud Gateway**
- **Netflix Eureka**
- **Apache Kafka**
- **Docker**

### Databases

- **PostgreSQL / MySQL**
- **MongoDB**

### Frontend

- **React.js**
- **JavaScript / TypeScript**

### Development Tools

- **Maven**
- **Git & GitHub**
- **IntelliJ IDEA**
- **Postman**

## 📦 Microservices

### 1. User Service

Responsible for user management and authentication-related operations.

**Responsibilities:**

- User registration and management
- User profile management
- Persistent user data
- Integration with authentication infrastructure

### 2. Activity Service

Responsible for tracking and managing fitness activities.

**Responsibilities:**

- Record fitness activities
- Store activity metrics
- Retrieve user activity history
- Publish activity events through Kafka

### 3. AI Service

Provides AI-powered analysis of fitness activities.

**Responsibilities:**

- Consume fitness activity information
- Analyze activity metrics using an LLM
- Generate personalized fitness insights
- Return AI-generated recommendations

## 🔄 Event-Driven Workflow

```text
User records activity
        │
        ▼
 Activity Service
        │
        ▼
   Kafka Event
        │
        ▼
    AI Service
        │
        ▼
 Spring AI / LLM
        │
        ▼
Fitness Analysis
        │
        ▼
 Personalized Insights
```

Kafka enables asynchronous communication between services and reduces direct coupling between the activity and AI components.

## 🔐 Security

The application uses **Keycloak and OAuth2** for authentication and authorization.

```text
Client
  │
  ▼
Keycloak
  │
  ▼
Access Token
  │
  ▼
API Gateway
  │
  ▼
Protected Microservices
```

## 🧠 AI Integration

The project integrates **Spring AI** to connect the backend with Large Language Models.

The AI workflow processes structured fitness activity data and generates useful insights such as:

- Activity analysis
- Performance observations
- Personalized recommendations
- Fitness improvement suggestions

This demonstrates how traditional Spring Boot microservices can be integrated with modern **Generative AI / LLM-based applications**.

## ⚙️ Core Concepts Demonstrated

- Java & Object-Oriented Programming
- Spring Boot
- Dependency Injection / IoC
- REST API Development
- Spring Data JPA
- Microservices Architecture
- Service Discovery
- API Gateway
- OAuth2 & Authentication
- Keycloak
- Event-Driven Architecture
- Apache Kafka
- SQL & NoSQL Databases
- AI / LLM Integration
- Spring AI
- Docker & Containerization
- Distributed Systems Concepts

## 📂 Project Structure

```text
fitness-app/
│
├── user-service/
│   └── src/
│
├── activity-service/
│   └── src/
│
├── ai-service/
│   └── src/
│
├── api-gateway/
│   └── src/
│
├── service-registry/
│   └── src/
│
├── frontend/
│   └── src/
│
└── README.md
```

## ▶️ Getting Started

### Prerequisites

Make sure the following are installed:

- Java 17+
- Maven
- Node.js
- Docker
- MongoDB
- PostgreSQL/MySQL
- Kafka
- Keycloak

### Clone the Repository

```bash
git clone <repository-url>
cd fitness-app
```

### Build the Backend

```bash
mvn clean install
```

### Start the Services

Start the required infrastructure and microservices:

```text
1. Database
2. Kafka
3. Keycloak
4. Eureka Server
5. API Gateway
6. User Service
7. Activity Service
8. AI Service
9. React Frontend
```
