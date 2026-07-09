# Recipes

This document defines common development workflows.

When asked to perform one of these tasks, follow the corresponding recipe unless instructed otherwise.

---

# Create a New Feature

A feature should be implemented end-to-end.

## Frontend

Create:

```
features/<feature>/

components/
pages/
services/
models/

<feature>.routes.ts
```

## Backend

Create:

```
modules/<feature>/

dto/
schemas/
mappers/
types/

<feature>.controller.ts
<feature>.service.ts
<feature>.module.ts
```

## Integration

- Add Angular routes.
- Register the NestJS module.
- Add navigation if required.

---

# Create CRUD

Implement complete CRUD.

## Backend

Create:

- Create DTO
- Update DTO
- Response DTO
- Schema
- Mapper
- Service
- Controller

Expose:

```
GET

GET /:id

POST

PATCH /:id

DELETE /:id
```

## Frontend

Create:

- List page
- Details page (if required)
- Create form
- Edit form
- Angular service
- Models

---

# Add Authentication

Create:

Backend

```
Auth Module

JWT Strategy

Auth Guard

Register Endpoint

Login Endpoint

Refresh Endpoint
```

Frontend

```
Login Page

Authentication Service

Route Guard

HTTP Interceptor
```

Passwords must always be hashed.

Never store plaintext passwords.

---

# Add a New Page

Create

```
pages/

<page>.component.ts

<page>.component.html

<page>.component.scss
```

Update

```
routes.ts
```

Do not place business logic inside pages.

---

# Add API Endpoint

Implement:

- DTO
- Validation
- Service method
- Controller endpoint

Return Response DTOs.

Never expose persistence models.

---

# Add Database Collection

Create:

```
schema

dto

mapper

service
```

Register schema inside the module.

Enable timestamps.

---

# Add External API

Create:

```
services/

external-api.service.ts
```

Requirements

- Typed responses
- Error handling
- Timeouts
- Retry when appropriate
- Configuration through environment variables

Never hardcode API keys.

---

# Add File Upload

Backend

- Validation
- File size limits
- MIME type validation

Frontend

- Progress indicator
- Error handling
- Drag-and-drop when appropriate

---

# Add Pagination

Backend

Support

```
page

limit

sort

search
```

Frontend

- Pagination controls
- Loading state
- Empty state

---

# Add Search

Backend

Prefer database filtering.

Frontend

Debounce search requests.

Avoid client-side filtering for large datasets.

---

# Add Dashboard

Separate:

- Statistics
- Charts
- Recent Activity
- Quick Actions

Load data concurrently when possible.

---

# Add Settings

Organize settings by category.

Examples

```
Profile

Account

Notifications

Appearance
```

Avoid one massive settings page.

---

# Refactor Existing Code

Goals

- Improve readability
- Reduce duplication
- Preserve behaviour

Do not introduce architectural changes unless requested.

---

# Debug an Issue

Follow this order:

1. Understand the problem.
2. Reproduce it.
3. Identify the root cause.
4. Fix the issue.
5. Explain why it happened.
6. Suggest prevention if appropriate.

Avoid speculative fixes.

---

# Before Finishing Any Task

Verify:

- Code compiles.
- Types are correct.
- Naming follows project conventions.
- Folder structure is preserved.
- No placeholder code remains.
- No unrelated code was modified.

If something cannot be completed, explain why and what is missing.