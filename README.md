# Dockerized Node.js Todo App

A simple Todo application built with **Node.js** and **Express.js**, fully containerized with **Docker**.

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express.js](https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

---

## Project Overview

This is my **second Docker project** as part of my DevOps learning journey with **Train With Shubham**. The project demonstrates:

- Building a Node.js web application
- Containerizing applications using Docker
- Using Docker Compose for container orchestration
- Working with Express.js and EJS templating

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| **Backend** | Node.js + Express.js |
| **Templating** | EJS (Embedded JavaScript) |
| **Containerization** | Docker & Docker Compose |
| **Language** | JavaScript |

---

## Project Structure

```
├── views/                  # EJS template files
│   ├── todo.ejs            # Main todo list view
│   └── edititem.ejs        # Edit item view
├── app.js                  # Main application entry point
├── package.json            # Node.js dependencies
├── Dockerfile              # Docker image configuration
├── docker-compose.yaml     # Docker Compose configuration
├── test.js                 # Test files
└── README.md               # Project documentation
```

---

## Getting Started

### Prerequisites

- Docker installed on your machine
- Docker Compose installed

### Run with Docker Compose

```bash
# Clone the repository
git clone https://github.com/yourusername/node-todo-cicd.git
cd node-todo-cicd

# Build and run the containers
docker-compose up -d

# Stop the containers
docker-compose down
```

### Run with Docker

```bash
# Build the Docker image
docker build -t node-todo-app .

# Run the container
docker run -d -p 8000:8000 node-todo-app
```

### Access the Application

| Service | URL |
|---------|-----|
| Todo App | http://localhost:8000 |

---

## Docker Commands

```bash
# Build the Docker image
docker build -t node-todo-app .

# Run the container
docker run -d --name node-todo-ctr -p 8000:8000 node-todo-app

# Using Docker Compose
docker-compose up -d      # Start in detached mode
docker-compose down       # Stop containers
docker-compose logs       # View logs
docker-compose ps         # List running containers

# Container Management
docker ps                 # List running containers
docker stop <container>   # Stop a container
docker rm <container>     # Remove a container
docker images             # List images
```

---

## Dockerfile Explained

```dockerfile
# Node Base Image
FROM node:12.2.0-alpine

# Working Directory
WORKDIR /app

# Copy the Code
COPY . /app

# Install the dependencies
RUN npm install

# Expose port
EXPOSE 8000

# Run the application
CMD ["node","app.js"]
```

---

## My DevOps Journey

This project is part of my DevOps learning journey. Here's my progress:

### Completed
- [x] **Docker Fundamentals** - Containerization basics
- [x] **Project 1** - Dockerized React-Django Todo App
- [x] **Project 2** - Dockerized Node.js Todo App *(This Project)*

### Currently Learning
- [ ] Docker Compose Advanced
- [ ] Docker Networking
- [ ] Docker Volumes & Persistence
- [ ] Multi-stage Docker Builds

---

## Acknowledgements

- **Train With Shubham** - For the amazing DevOps training
- **Docker Documentation** - For comprehensive guides

---

## License

This project is open source and available for learning purposes.

---

## Connect With Me

Feel free to connect and share your DevOps journey!

⭐ If you found this project helpful, please give it a star!

---

*Happy Learning! 🚀*