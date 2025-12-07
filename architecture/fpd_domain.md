# FPD Domain Layer

## Overview
The **Domain Layer** contains the pure business rules of the application. It is the core of the architecture and remains independent of the UI, frameworks, data sources, or external services.

## Responsibilities
- **Core Types**: Definitions of domain entities and value objects.
- **Validations**: Business logic to ensure data integrity.
- **Behaviors**: Operations that represent business rules.
- **Interfaces**: Definitions of repositories or services (implemented in other layers).

## Rules
- **No Dependencies**: Must NOT import `services`, `data`, `state`, or `component`.
- **Pure Logic**: Focus solely on domain problems, not technical details.
