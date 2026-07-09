# Architecture

Build software in vertical slices.

Prefer feature-first organization.

Avoid layered architectures where every feature is spread across unrelated folders.

Keep business logic inside services.

Controllers coordinate.

DTOs validate.

Repositories abstract persistence only when useful.

Do not introduce unnecessary abstractions.

Every abstraction must remove duplication or isolate complexity.

Prefer composition.

Avoid inheritance.