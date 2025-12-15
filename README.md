# DevOps Architecture Lab

This repository is a hands-on learning project focused on understanding
modern backend and DevOps architecture from the ground up.

The main goal of this project is not to build a production product,
but to **deeply understand how real-world systems are structured**,
how components interact with each other, and how architectural decisions
affect security, scalability, and reliability.

---

## 🎯 Project Goals

- Understand how client requests flow through a system
- Learn the role of an entry point (HTTP server) in backend architecture
- Separate responsibilities between:
  - entry point
  - application logic
  - data storage
- Practice container-based architecture using Docker
- Build a solid foundation for future topics:
  - load balancing
  - security hardening
  - service isolation
  - Kubernetes (later stage)

This project is designed as a **learning lab**, not a framework or a template.

---

## 🧱 High-Level Architecture (v1)

Client
|
v
Nginx (entry point)
|
v
Application service
|
v
Database


### Key ideas:
- Clients communicate **only** with Nginx
- Application logic is isolated from direct external access
- The database is never exposed to clients
- Each component has a single, clear responsibility

---

## 🔌 Components Overview

### Nginx
Acts as the single entry point for all incoming HTTP requests.
It handles request routing and protects the application from direct exposure.

### Application Service
A simple backend service that processes requests and returns responses.
All business logic lives here.

### Database
Used for storing minimal data required by the application.
In early stages, the database is used only to demonstrate
application-to-database interaction.

---

## 🐳 Why Docker

Each component runs in its own container.
This allows:
- clear separation of concerns
- easier debugging and experimentation
- reproducible environments

The system is started as a **set of containers working together**,
not as a single monolithic application.

---

## 🚧 Current Stage

- [x] Architecture design
- [x] Project documentation (v1)
- [ ] Application service (v1)
- [ ] Nginx configuration
- [ ] Docker Compose setup
- [ ] Load balancing (later)
- [ ] Security hardening (later)
- [ ] Kubernetes (future stage)

---

## 📌 Notes

This repository evolves step by step.
Architectural decisions may change as understanding improves.

The focus is on **learning and reasoning**, not on rushing implementation.

---

## 📄 License

Educational use only.
