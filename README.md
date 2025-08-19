
````markdown
# EyeFishPlatformFrontend

This repository contains the **frontend application** for the EyeFish Platform, built with **Angular** using **standalone components**.  
It follows a **feature-based architecture** to keep the codebase modular, scalable, and maintainable.

---

## 🚀 Tech Stack

- **Angular 20** (with standalone components, no NgModules)
- **TypeScript**
- **RxJS** for reactive programming
- **Angular Router** (standalone lazy-loaded routes)
- **TailwindCSS / SCSS** (if applicable)
- **Jest / Karma** for testing

---

## 🛠️ Development Setup

### 1. Install Dependencies
```bash
npm install
````

### 2. Start Development Server

```bash
ng serve
```

The app will be available at: [http://localhost:4200](http://localhost:4200).
The server reloads automatically when you modify any source files.

### 3. Build for Production

```bash
ng build
```

Build artifacts will be stored in the `dist/` directory.
Production builds are optimized for speed and performance.

---

## 🧩 Project Structure

We follow a **feature-based folder structure** with **standalone components**:

```
app/
├── features/                       # Business domains (self-contained features)
│   ├── <feature-name>/
│   │   ├── components/             # Standalone UI components
│   │   │   └── <component-name>/
│   │   │       └── <component>.component.ts
│   │   ├── services/               # Feature-specific services (business logic, API)
│   │   ├── entities/               # Models, interfaces, or types
│   │   └── <feature>-routing.ts    # Standalone routing for lazy loading
│   └── ...
├── shared/                         # Shared components, services, and utilities
│   ├── components/                 # Reusable standalone components
│   ├── services/                   # Reusable services
│   └── utils/                      # Helper functions
├── assets/                         # Static files (images, icons, styles, etc.)
├── environments/                   # Environment configs (dev, prod)
└── main.ts                         # Application bootstrap
```

### 🔑 Guidelines

* Each **feature is lazy-loaded** with its own routing file.
* **Do not import one feature directly into another**. Use services or shared layer for communication.
* Place only **cross-feature reusable code** in the `shared/` folder.
* Use **OnPush change detection** for components when possible to improve performance.

---

## 🧪 Testing

### Run Unit Tests

```bash
ng test
```

### Run End-to-End Tests

```bash
ng e2e
```

> Angular CLI does not ship with an e2e framework by default. You can integrate Cypress, Playwright, or another framework of choice.

---

## 📖 Code Generation

Use Angular CLI to scaffold new elements:

* Generate a new **component**:

  ```bash
  ng generate component features/<feature>/components/<component-name> --standalone
  ```
* Generate a new **service**:

  ```bash
  ng generate service features/<feature>/services/<service-name>
  ```
* Generate a new **interface/model**:

  ```bash
  ng generate interface features/<feature>/entities/<model-name>
  ```

For more options:

```bash
ng generate --help
```

---

## 🤝 Contribution Guidelines

* Follow the **Angular style guide** (naming, file structure, coding conventions).
* Write **unit tests** for new components and services.
* Keep features **self-contained** (components, services, entities inside the feature).
* Use the `shared/` folder only for **truly reusable** code.
* Update documentation (README or feature-specific docs) when introducing new structures.

---

## 📚 Additional Resources

* [Angular Documentation](https://angular.dev)
* [Angular CLI Reference](https://angular.dev/tools/cli)
* [Angular Style Guide](https://angular.dev/style-guide)

---

✅ With this setup, our project remains **clean, scalable, and easy to maintain** as it grows.

```

---


