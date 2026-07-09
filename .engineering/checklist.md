# Engineering Checklist

Run through this checklist before completing any task.

---

# Architecture

- [ ] Follows the project structure in `architecture.md`.
- [ ] Respects `project.template.json`.
- [ ] Uses feature-first architecture.
- [ ] No unnecessary abstractions.
- [ ] No duplicated code.

---

# Frontend

- [ ] Uses Standalone Components.
- [ ] Uses Signals for local state.
- [ ] Uses Reactive Forms when applicable.
- [ ] Uses Tailwind CSS.
- [ ] Uses DaisyUI components.
- [ ] Uses Angular best practices.
- [ ] No business logic inside components.
- [ ] Services handle API communication.

---

# Backend

- [ ] Business logic lives inside services.
- [ ] Controllers remain thin.
- [ ] DTOs validate requests.
- [ ] Response DTOs are used.
- [ ] Persistence models are never returned directly.
- [ ] Environment variables are used.
- [ ] Proper HTTP exceptions are returned.

---

# Database

- [ ] Schema belongs to the correct module.
- [ ] Indexes added where appropriate.
- [ ] Relationships modeled correctly.
- [ ] Timestamps enabled when appropriate.

---

# Code Quality

- [ ] TypeScript strict mode respected.
- [ ] No `any` unless explicitly justified.
- [ ] No placeholder code.
- [ ] No TODO comments.
- [ ] Consistent naming.
- [ ] Imports cleaned up.
- [ ] No dead code.

---

# User Experience

- [ ] Loading states implemented.
- [ ] Empty states implemented.
- [ ] Error states handled.
- [ ] Responsive layout.
- [ ] Accessible where practical.

---

# Security

- [ ] Input validated.
- [ ] Sensitive data not exposed.
- [ ] Secrets stored in environment variables.
- [ ] Passwords hashed.
- [ ] Authentication respected.

---

# Final Review

- [ ] Code compiles.
- [ ] Project builds successfully.
- [ ] Folder structure preserved.
- [ ] Existing functionality not broken.
- [ ] Solution follows the engineering standards.

If any checklist item cannot be satisfied, explain why before completing the task.