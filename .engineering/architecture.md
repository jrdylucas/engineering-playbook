# Architecture

This document defines the standard project architecture used across all projects.

Unless instructed otherwise, all generated code should follow these conventions.

---

# Philosophy

Applications should be organized around **features**, not technical layers.

Related code should live together.

Every application should be easy to navigate without prior knowledge of the project.

---

# Repository Structure

```
project/

.engineering/

apps/
├── frontend/
└── backend/

packages/

docker/

scripts/

docs/

package.json
project.template.json
docker-compose.yml
README.md
```

---

# Applications

The repository contains two independent applications.

```
apps/

frontend/
backend/
```

Both applications should be independently runnable and deployable.

---

# Shared Packages

Shared code belongs inside:

```
packages/
```

Examples:

```
packages/

shared/

types/

utils/

constants/
```

Do not duplicate code between frontend and backend.

---

# Frontend

```
src/

app/

core/
shared/
features/
```

## Core

Contains application-wide functionality.

Examples:

- Authentication
- Configuration
- Guards
- Interceptors
- Layout

Core should not contain business logic.

---

## Shared

Contains reusable code.

Examples:

- Components
- Pipes
- Directives
- Models
- Utilities

Do not place feature-specific code inside Shared.

---

## Features

Organize by business capability.

Example:

```
features/

users/

products/

orders/

dashboard/

settings/
```

Every feature owns:

```
components/

pages/

services/

models/

routes.ts
```

---

# Backend

```
src/

common/

config/

modules/
```

---

## Common

Contains reusable backend functionality.

Examples:

```
guards/

decorators/

filters/

interceptors/

pipes/

exceptions/
```

Only place code here when shared by multiple modules.

---

## Config

Application configuration.

Examples:

```
database.config.ts

jwt.config.ts

app.config.ts
```

Configuration should always come from environment variables.

---

## Modules

Every business capability becomes a module.

Example:

```
modules/

users/

products/

orders/

inventory/
```

---

# Module Structure

Every module should follow this structure.

```
users/

dto/
mappers/
schemas/
types/

users.controller.ts
users.service.ts
users.module.ts
```

## dto

Request and response DTOs.

Examples:

```
create-user.dto.ts

update-user.dto.ts

user-response.dto.ts
```

---

## schemas

Persistence models.

Examples:

```
user.schema.ts
```

Schemas should never contain business logic.

---

## mappers

Responsible for converting between:

- Database models
- DTOs
- API responses

Example:

```
UserMapper.toResponse()

UserMapper.toEntity()
```

Never return persistence models directly from controllers.

---

## types

Internal TypeScript types.

Examples:

```
user.types.ts

jwt.types.ts
```

---

# Ownership

Every feature owns:

- API
- Business logic
- Persistence
- Mapping
- Validation

Avoid spreading one feature across multiple directories.

---

# Naming Conventions

Directories:

```
users

shopping-cart

user-profile
```

Files:

```
users.service.ts

users.controller.ts

create-user.dto.ts

user.schema.ts

user.mapper.ts
```

Use lowercase with hyphens for directories.

Use standard NestJS naming for files.

---

# Project Rules

- Keep controllers thin.
- Keep business logic inside services.
- Never expose persistence models.
- Prefer composition over inheritance.
- Prefer feature-first organization.
- Keep related code together.

---

# Avoid

Avoid structures like:

```
controllers/

services/

repositories/

schemas/
```

at the project root.

This separates related code and makes projects harder to navigate.

---

# AI Guidelines

When generating code:

- Preserve this folder structure.
- Create new features inside `features/` (frontend) and `modules/` (backend).
- Never invent new architectural patterns.
- Keep naming consistent.
- Follow framework conventions.

# Quick Reference

| I need to create... | Put it here |
|----------------------|------------|
| Angular page | `features/<feature>/pages` |
| Angular component | `features/<feature>/components` |
| Angular service | `features/<feature>/services` |
| Angular model | `features/<feature>/models` |
| NestJS controller | `modules/<feature>` |
| NestJS service | `modules/<feature>` |
| DTO | `modules/<feature>/dto` |
| Schema | `modules/<feature>/schemas` |
| Mapper | `modules/<feature>/mappers` |
| Shared utility | `packages/shared/utils` |
| Shared type | `packages/shared/types` |