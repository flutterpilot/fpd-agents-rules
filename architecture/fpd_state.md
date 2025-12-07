# FPD State Layer

## Overview
The **State Layer** is responsible for managing the application's or feature's state. It provides a controlled interface for reading and writing state changes.

## Responsibilities
- **State Management**: Holds the current state of features or the global app.
- **Exposures**: Provides observables or streams for the UI to react to.
- **Updates**: Methods to mutate state safely.

## Rules
- **No Business Rules**: Complex logic belongs in the Domain layer.
- **No UI Dependency**: Should not import UI components directly.
