✈️ Travel Plan – Microservices Architecture

📌 Project Overview

Travel Plan is a microservices-based application designed to manage travel-related services. The application is divided into independent services to improve scalability, maintainability, and flexibility, Travel Management System with an Admin Dashboard.

## Technology Stack

- Frontend: Angular
- Backend: Java and Spring Boot
- Relational Database: PostgreSQL
- Graph Database: Neo4j
- Containerization: Docker and Docker Compose
- CI/CD: Jenkins
- Code Quality: SonarQube
- Automation: Ansible

📂 Project Structure
text

Travel-plan/
│
├── gateway-service/
│
├── user-service/
│
├── travel-service/
│
├── payment-service/
│
└── readme.md

## Local Infrastructure

Start databases:

```bash
docker compose --env-file .env \
  -f infrastructure/docker/docker-compose.yml up -d
```

Check services:

```bash
docker compose --env-file .env \
  -f infrastructure/docker/docker-compose.yml ps
```

Stop containers without deleting data:

```bash
docker compose --env-file .env \
  -f infrastructure/docker/docker-compose.yml down
```

## Run the Microservices

Start each microservice independently:
bash

cd user-service
./mvnw spring-boot:run

