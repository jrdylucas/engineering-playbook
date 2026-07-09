# Project Setup

This document defines how new projects should be bootstrapped.

Always follow this process unless the user explicitly requests otherwise.

---

# Goal

The objective of project setup is to produce a production-ready development environment with minimal manual configuration.

After setup, the project should be immediately ready for development.

---

# Default Stack

Use the technologies defined in `stack.md`.

If a `project.template.json` exists, its configuration overrides the defaults.

---

# Project Structure

Generate the standard repository structure defined in `architecture.md`.

```
project/

.engineering/

apps/
    frontend/
    backend/

packages/

docker/

scripts/

docs/
```

---

# Bootstrap Order

Always create the project in the following order.

## 1. Create repository structure

Create the standard folders.

Do not overwrite existing files.

---

## 2. Create frontend

Create an Angular application.

Requirements:

- Standalone Components
- Routing enabled
- SCSS
- Strict TypeScript

Install:

- Tailwind CSS
- DaisyUI

---

## 3. Create backend

Create a NestJS application.

Install:

- Mongoose
- Passport
- JWT
- bcrypt
- class-validator
- class-transformer

Configure:

- ValidationPipe
- CORS

---

## 4. Configure MongoDB

Create Docker Compose configuration.

Development uses Docker only for infrastructure.

Applications run locally.

---

## 5. Environment Variables

Generate

```
.env
```

Generate

```
.env.example
```

Never hardcode:

- Ports
- Secrets
- Database URLs

---

## 6. Port Allocation

Never assume default ports are available.

Automatically find an available port.

Store generated ports inside `.env`.

Example

```
DATABASE_PORT=27018
```

Applications should always read ports from environment variables.

---

## 7. Install Dependencies

Install:

- Root dependencies
- Frontend dependencies
- Backend dependencies

Verify installation completed successfully.

---

## 8. Verify

Verify:

- Frontend builds
- Backend builds
- Docker Compose is valid
- MongoDB starts successfully

---

# Docker

Development

Containerize infrastructure only.

Examples

- MongoDB
- Redis
- Mailpit

Run applications locally.

Production

Containerize every service.

---

# Idempotency

Setup should be safe to run multiple times.

Never overwrite:

- Source code
- Environment files
- User configuration

without confirmation.

---

# AI Guidelines

When creating a new project:

- Follow this order.
- Explain what is being created.
- Prefer official framework tooling.
- Keep setup deterministic.
- Avoid unnecessary dependencies.
- Stop immediately if a required step fails.