# Technology Stack

This document defines the default technology stack for all new projects.

Unless a project has specific requirements, these technologies should be used.

---

# Philosophy

- Prefer stable, well-supported technologies.
- Prefer official libraries over community alternatives.
- Minimize dependencies.
- Keep the stack consistent across projects.
- Upgrade to the latest stable versions regularly.

---

# Frontend

## Framework

- Angular

### Standards

- Standalone Components
- Signals
- Functional Route Guards
- Lazy Loaded Routes
- Reactive Forms
- HttpClient

---

## Styling

### CSS

- Tailwind CSS

### UI Components

- DaisyUI

### Icons

Preferred:

- Heroicons

Acceptable:

- Lucide

---

# Backend

## Framework

- NestJS

### Standards

- REST APIs
- Feature Modules
- Dependency Injection
- ValidationPipe
- CORS Enabled

---

## Validation

- class-validator
- class-transformer

---

## Authentication

- JWT
- Passport
- bcrypt

---

# Database

## Primary Database

- MongoDB

## ODM

- Mongoose

---

# Infrastructure

## Development

Use Docker Compose for infrastructure only.

Containerize:

- MongoDB

Run locally:

- Angular
- NestJS

---

## Production

Containerize every service.

---

# Package Manager

- npm

Use npm Workspaces.

---

# Code Quality

## Language

- TypeScript (Strict Mode)

## Formatting

- Prettier

## Linting

- ESLint

---

# API Documentation

- OpenAPI (Swagger)

---

# Version Control

- Git
- GitHub

---

# Future Technologies

These are supported but should only be introduced when required.

- Redis
- MinIO
- Mailpit
- PostgreSQL
- OpenSearch
- RabbitMQ

Avoid introducing technologies until they solve a real problem.

---

# General Guidelines

- Use the latest stable releases.
- Prefer official documentation.
- Avoid experimental features in production.
- Avoid unnecessary dependencies.
- Keep the technology stack intentionally small.

---

# Project Template

Every project contains a `project.template.json`.

Example:

```json
{
  "frontend": "angular",
  "backend": "nestjs",
  "database": "mongodb",
  "ui": "daisyui",
  "css": "tailwind"
}
```

The values in `project.template.json` override the defaults in this document.

This document defines the preferred stack.

The project template defines the selected stack for the current project.