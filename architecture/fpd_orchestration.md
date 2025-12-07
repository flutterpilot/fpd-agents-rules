# FPD Orchestration Layer

## Overview
The **Orchestration Layer** is the "Director" of the architecture. It coordinates the interactions between all other layers to fulfill specific use cases.

## Responsibilities
- **Use Case Implementation**: "Send Notification", "Login User", etc.
- **Coordination**:
  - Fetches data via `Data`.
  - Validates via `Domain`.
  - Updates `State`.
  - Triggers side-effects via `Services`.
  - Logs via `Cross-Cutting`.
  - Directs `Navigation`.

## Rules
- **The Connector**: The *only* layer that can import multiple other layers to wire them together.
- **Strict Direction**: UI Components interact with Orchestration (via inputs/outputs) to trigger actions.
