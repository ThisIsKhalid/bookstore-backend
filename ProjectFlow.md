# 📚 Bookstore Microservices Project

> A comprehensive NestJS microservices architecture for a modern bookstore application

## 🚀 Project Setup Guide

### Step 1: Initialize NestJS Project

First, create a new NestJS project using the Nest CLI:

```bash
nest new bookstore
```

### Step 2: Generate Microservice Applications

Create the microservice applications that will form our distributed architecture:

#### 🌐 API Gateway

```bash
nest generate app bookstore-api-gateway
```

#### 📖 Books Service

```bash
nest generate app books
```

#### 👥 Users Service

```bash
nest generate app users
```

### Step 3: Configure Project Structure

Update the `nest-cli.json` configuration:

1. Navigate to the `nest-cli.json` file
2. Change the default project path from `bookstore` to `bookstore-api-gateway`

This ensures that the API Gateway serves as the main entry point for our microservices architecture.

## 🏗️ Architecture Overview

```
┌─────────────────────────┐
│   API Gateway           │
│  (bookstore-api-gateway)│
└─────────┬───────────────┘
          │
          ├─── Books Service
          └─── Users Service
```

## 📁 Project Structure

```
bookstore/
├── apps/
│   ├── bookstore-api-gateway/  # Main API Gateway
│   ├── books/                  # Books microservice
│   └── users/                  # Users microservice
├── nest-cli.json              # NestJS CLI configuration
└── package.json               # Dependencies
```

---

_Happy coding! 🎉_

install @nestjs/microservices in each service\_

```bash
npm install @nestjs/microservices
```


Add a users module to the gateway application
nest generate module users --project bookstore-api-gateway

Add a users service to the gateway application
nest generate service users --project bookstore-api-gateway

Add a users controller to the gateway application
nest generate controller users --project bookstore-api-gateway