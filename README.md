# Vite+ Monorepo Starter

A starter for creating a Vite+ monorepo.

## TODO

### Setup `Convex` in `packages/convex`

- Setup `package.json` with dependencies and scripts.
- Setup `Better Auth` for authentication.
- See if you need to setup any configs (`convex.json`) or linting/formatting rules.

### Setup `AGENTS.md` at the root of the repo

- Document how the project is organized.
  - `vite+` for the monorepo configuration and shared dependencies.
    - Linting and formatting rules (auto?).
  - `apps` for user-facing applications.
    - `tanstack-solid` for a Tanstack Solid example app.
  - `packages` for shared code and tools.
    - `devtools` for scripts and tools used in development.
    - `convex` for Convex backend code.

### Setup `Scripts` in `packages/devtools`

- Setup `package.json` with dependencies and scripts.
  - `zod` for schema validation.
  - `cac` for CLI.
  - `clack/prompts` for interactive prompts.
  - `picocolors` for colored terminal output.
  - `vitest` for unit testing script functions and utilities.
- Setup `runner` that can be lauched to select and run any script in `devtools` package.
- Setup `src` directory for the individual scripts.
  - Setup `utils` directory for shared utilities and helpers across scripts.
  - Setup `example` script to read lines of code in the `apps/tanstack-solid` directory.
- Setup `tests` directory for unit testing discrete script functions.
- Define a standard for building scripts in this repo.
  - Utility for validating ENV variables.
  - Utility for logging summaries/tables of information to the terminal.
  - Utility for logging messages/banners of different severities (info, success, warning, error).
  - Documentation for how to create and run scripts in this repo (using the `runner`).
    - Agent friendly.

### Setup `Tanstack Solid` in `packages/tanstack-solid`

- Setup `package.json` with dependencies and scripts.
  - `tailwindcss` for styling.
  - `shadcn/ui` for pre-built UI components.
- Setup basic auth and logged in page for testing Convex connection.

## Development

- Check everything is ready:

```bash
vp run ready
```

- Run the tests:

```bash
vp run -r test
```

- Build the monorepo:

```bash
vp run -r build
```

- Run the development server:

```bash
vp run dev
```
