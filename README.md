# Nestjs and MySQL with TypeORM

<p align="center">
  <a href="http://nestjs.com/" target="blank"><img src="https://nestjs.com/img/logo-small.svg" width="200" alt="Nest Logo" /></a>
</p>

[circleci-image]: https://img.shields.io/circleci/build/github/nestjs/nest/master?token=abc123def456
[circleci-url]: https://circleci.com/gh/nestjs/nest

## Introduction

This project is a backend application developed with NestJS that provides a simple task management system. The application allows users to create, retrieve, update, and delete tasks. The project uses class-validator for input validation and UUID for generating unique identifiers for tasks.

## 🔬 Project Structure

### Main Files

- main.ts: The entry point of the application. Initializes and starts the NestJS server with global validation pipes.

- **app.module.ts**: The main module that imports the TasksModule.

- **tasks.module.ts**: Module containing the functionalities related to tasks.

- **tasks.service.ts**: Service that handles the business logic for tasks.

- **tasks.controller.ts**: Controller that defines the API endpoints for tasks.

- **entities/task.entity.ts**: Defines the Task entity and its status enum.

- **dto/task.dto.ts**: Data Transfer Objects (DTOs) for creating and updating tasks.

## 🔨 Installation and Configuration

### 1. Clone the Repository

```bash
git clone https://github.com/IgnaLog/first-nestjs-app.git
cd first-nestjs-app
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Run the Application

Development Mode

```bash
npm run start:dev
```

This will start the server in development mode at http://localhost:3000/.

## 🚀 API Endpoints

## **Tasks**

### **Get All Tasks**

- **Endpoint**: `GET /tasks`

- **Description**:  Retrieves a list of all tasks.

- **Response**: Array of `Task` objects.

### **Create a Task**

- **Endpoint**: `POST /tasks`

- **Description**: Creates a new task.

- **Request Body**:

  - **`title`**: Task title (string, required, min length 3).

  - **`description`**: Task description (string).

- **Response**: Newly created `Task` object.

### **Delete a Task**

- **Endpoint**: `DELETE /tasks/:id`

- **Description**: Deletes a task by its ID.

- **Parameters**:

  - **`id`**: Task ID (string)

- **Response**: No content.

### **Update a Task**

- **Endpoint**: `PATCH /tasks/:id`

- **Description**: Updates a task by its ID.

- **Parameters**:

  - **`id`**: Task ID (string).

- **Request Body**:

  - **`title`**: New title (optional, string).

  - **`description`**: New description (optional, string).

  - **`status`**: New status (optional, must be one of `PENDING`, `IN_PROGRESS`, `DONE`).

- **Response**: Updated `Task` object.


