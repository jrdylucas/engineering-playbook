# Engineering Starter Template

> An opinionated, AI-first starter template for building modern full-stack applications with consistent architecture, development workflows, and engineering standards.

---

# Overview

This repository provides a reusable foundation for new software projects.

Rather than serving as a traditional boilerplate, this repository defines a set of engineering standards that guide both developers and AI assistants when creating, maintaining, and extending applications.

The goal is to eliminate repetitive setup work while maintaining consistency across projects.

---

# Philosophy

This template is built around a few core principles.

- Prefer official framework conventions.
- Keep the technology stack intentionally small.
- Organize applications by feature.
- Generate production-ready implementations.
- Avoid unnecessary abstractions.
- Optimize for readability and maintainability.
- Use AI to automate repetitive engineering tasks.

---

# Repository Structure

```text
.
├── .engineering/
├── apps/
│   ├── frontend/
│   └── backend/
├── packages/
├── docker/
├── scripts/
├── docs/
├── package.json
├── project.template.json
└── README.md
```

---

# Engineering Standards

All engineering standards are located inside the `.engineering` directory, the `README.md` is in the root.

```text
README.md
.engineering/

tech-stack.md
architecture.md
setup.md
recipes.md
checklist.md
ai.md
```

These documents define:

- Preferred technology stack
- Project architecture
- Project setup process
- Development workflows
- Engineering quality checklist
- AI collaboration guidelines

Together they form the engineering context for every project created from this template.

---

# Project Configuration

Every project should contain a:

```text
project.template.json
```

This file defines the technologies, architecture, and project-specific configuration.

When present, it should be treated as the source of truth for the current project.

---

# AI Workflow

When working on this project, AI assistants should follow this process:

1. Read `README.md`.
2. Read all referenced engineering documents.
3. Read `project.template.json`.
4. Follow the defined engineering standards.
5. Preserve architectural consistency.
6. Generate production-ready implementations.

---

# Goals

This template aims to provide:

- Consistent architecture
- Modern development practices
- AI-friendly engineering context
- Rapid project initialization
- Production-ready defaults
- Excellent developer experience

---

# What This Repository Does Not Provide

This repository intentionally does not include application-specific business logic.

Instead, it provides:

- Engineering standards
- Architectural guidance
- Development workflows
- Project conventions

Applications built from this template should inherit these standards while remaining free to implement their own business requirements.

---

# Contributing

When updating this repository:

- Keep the engineering standards concise.
- Prefer official framework recommendations.
- Avoid documenting project-specific decisions.
- Maintain consistency across all engineering documents.
- Keep AI context practical and easy to consume.

---

# License

MIT