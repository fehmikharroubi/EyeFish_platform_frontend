# Core Module

The `core` folder contains **singleton services** and **application-wide features**.  
This module should be imported **only once** in `AppModule`.

### What to put here
- Authentication services
- Route guards
- HTTP interceptors
- Global configuration (e.g. environment tokens, API URLs)
- Logging and error handling services

### What NOT to put here
- Reusable UI components (go to `/shared`)
- Feature-specific logic (go to `/features/<feature>/`)
