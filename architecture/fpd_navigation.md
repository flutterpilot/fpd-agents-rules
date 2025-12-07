# FPD Navigation Layer

## Overview
The **Navigation Layer** manages the routing and screen definitions of the application.

## Responsibilities
- **Routes**: Definitions of available paths/URLs.
- **Screens**: High-level containers that assemble Components.
- **Flows**: Navigation logic (push, pop, replace).

## Rules
- **No Business Rules**: Orchestration handles *when* to navigate; this layer handles *how*.
- **Screen Assembly**: Connects Orchestration outputs to Components.
