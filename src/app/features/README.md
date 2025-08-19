app/
└── features/
    ├── <feature-name>/                  # Each business domain
    │   ├── components/                  # Standalone UI components
    │   │   ├── <component-name>/        # Example: order-list
    │   │   │   └── <component>.component.ts  # Standalone component
    │   │   └── ...
    │   ├── services/                    # Business logic, API calls
    │   │   └── <feature>.service.ts
    │   ├── entities/                    # Models, types, or interfaces
    │   │   └── <feature>.model.ts
    │   └── <feature>-routing.ts         # Routing for this feature (standalone)
    └── ...                               # Additional features

shared/
└── ...                                   # Shared standalone components, services, utilities

# Guidelines

- Each feature should be **lazy-loaded** using its **standalone routing** (`<feature>-routing.ts`).
- Components inside `components/` should be **standalone**, importing only the Angular modules or other standalone components they need.
- Features should **not import other features directly**. Use **services** or **shared components** for communication.
- Keep everything related to a feature **self-contained**: components, services, and entities/models live inside the feature folder.
- Shared resources should be placed in the **shared/** folder to avoid cross-feature dependencies.

# Example Feature: Orders

app/features/orders/
├── components/                          # Standalone UI components for orders
│   ├── order-list/
│   │   └── order-list.component.ts      # Standalone component
│   └── order-detail/
│       └── order-detail.component.ts   # Standalone component
├── services/                             # Business logic and API calls
│   └── order.service.ts
├── entities/                             # Models, types, or interfaces
│   └── order.model.ts
└── orders-routing.ts                     # Standalone routing for orders feature

# Notes

- Standalone components and routing make the app **fully modular** and **lazy-loadable**.
- Each feature is **self-contained**, **scalable**, and easy to maintain.
- Developers can locate feature-specific components, services, and entities quickly.
- Shared resources should only go in `shared/` to avoid direct dependencies between features.
