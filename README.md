# Flowark-MicroServices

![.NET](https://img.shields.io/badge/.NET-8.0-blueviolet?logo=dotnet)
![Angular](https://img.shields.io/badge/Angular-17-red?logo=angular)
![Docker](https://img.shields.io/badge/Docker-RabbitMQ-blue?logo=docker)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen)

Monorepo for a **.NET 8 Microservices Application** with **Angular frontend** and **RabbitMQ with Docker**.

## Structure
- `Gateway` → API Gateway
- `Services/IdentityService` → Identity & Auth
- `Services/WorkItemService` → Project & Task Management
- `Services/AuditService` → Audit Logs
- `Shared` → Shared libraries
- `flowark-client` → Angular frontend
- `tests/` → Unit & Integration tests

## Run the Application

### 1. Start RabbitMQ (Docker)
```bash
docker-compose up -d

RabbitMQ UI → http://localhost:15672 (guest / guest)
```
### 2. Run Backend (Visual Studio)

Open Flowark.Microservices.sln

Right-click solution → Set Startup Projects…

Select Multiple startup projects → Start Gateway.Api, IdentityService.Api, WorkItemService.Api, AuditService.Api

Press Run

### 3. Run Angular Client

cd src/flowark-client
npm install
ng serve -o

## Stack

.NET 8 Web API

Angular 17

RabbitMQ + Docker

SQL Server