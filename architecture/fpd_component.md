# FPD Component Layer

## Overview
The **Component Layer** contains reusable User Interface definitions. These are "dumb" or "pure" components concerned only with rendering.

## Responsibilities
- **Rendering**: Displaying data passed to them.
- **User Interaction**: Capturing events (clicks, input) and bubbling them up.
- **Reusability**: Designed to be used across multiple screens.

## Rules
- **Pure Render**: No business logic or direct state manipulation.
- **No Dependencies**: Must NOT import `domain`, `data`, or `services`.
- **Inputs/Outputs**: Relies solely on parameters and callbacks.
