# FPD Services Layer

## Overview
The **Services Layer** provides access to external infrastructure and system capabilities. It handles Input/Output (IO) operations.

## Responsibilities
- **Infrastructure Access**: HTTP clients, Database drivers, File system access.
- **Device Features**: Camera, geolocation, sensors.
- **External APIs**: Direct calls to third-party services.

## Rules
- **No Business Logic**: Only handles the technical integration.
- **Pure IO**: Focus on sending/receiving data.
- **No Data Layer Dependency**: Services should not depend on the Data layer.
