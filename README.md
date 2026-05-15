# Distributed Task Processing Platform

I wanted to move beyond traditional CRUD-style MERN projects and understand how real backend systems process tasks asynchronously at scale.

Most beginner projects handle everything inside a single server request-response cycle. But modern systems often use queues, background workers, retries, and distributed processing to manage workloads more efficiently.

This project is my attempt to learn those concepts through implementation instead of only studying system design theory.

The goal is not to build a huge enterprise platform, but to understand:
- how queues work
- why worker services are separated
- how async processing improves scalability
- how realtime task updates are handled
- how distributed systems communicate internally

The platform allows users to submit tasks such as:
- scraping jobs
- report generation
- email jobs
- background processing tasks

Instead of processing tasks directly inside the API server:

```text
User submits task
        ↓
API receives request
        ↓
Task pushed to Redis queue
        ↓
Worker services consume task
        ↓
Task processed asynchronously
        ↓
Realtime status updates sent to client
```

The project is being built progressively while learning concepts like:
- Redis queues
- BullMQ
- worker architecture
- retries and failure handling
- Socket.io realtime communication
- Dockerized multi-service applications
- concurrent task processing
- backend scalability concepts

---

## Tech Stack

### Frontend
- React.js
- Tailwind CSS
- Socket.io Client

### Backend
- Node.js
- Express.js
- Socket.io

### Infrastructure
- Redis
- BullMQ
- Docker
- Docker Compose

---

## Project Structure

```text
distributed-task-platform/

├── client/
├── api-server/
├── worker/
├── shared/
└── docker-compose.yml
```

---

## Current Focus

Currently working on:
- architecture planning
- Redis queue integration
- worker communication
- async task flow
- realtime status updates

This project is intentionally being developed step-by-step to properly understand the reasoning behind each architectural decision instead of blindly assembling technologies together.
