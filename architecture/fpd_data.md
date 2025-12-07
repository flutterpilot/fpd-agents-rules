# FPD Data Layer

## Overview
The **Data Layer** handles data retrieval, transformation, and persistence. It implements the repository interfaces defined in the Domain layer.

## Responsibilities
- **Data Mapping**: Transforming external data (JSON, DB rows) into Domain entities.
- **Repositories**: Implementation of domain repositories.
- **Data Sources**: Interaction with local databases, caches, or remote APIs (often via Services).

## Rules
- **No UI/State Knowledge**: Does not know about screens or state management.
- **Implementation Detail**: Acts as an adapter for the Domain.
