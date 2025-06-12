# Full Stack FastAPI + Next.js Turborepo Starter

This Turborepo starter provides a modern full-stack development environment with FastAPI backend and Next.js frontend, using pnpm as the package manager.

## Prerequisites

- [Node.js](https://nodejs.org/) (v18 or later)
- [pnpm](https://pnpm.io/) (v8 or later)
- [Python](https://www.python.org/) (v3.11 or later)

## Using this example

First, ensure you have pnpm installed:

```sh
npm install -g pnpm
```

Then run:

```sh
npx create-turbo@latest
```

## What's inside?

This Turborepo includes the following packages/apps:

### Apps and Packages

- `web`: a [Next.js](https://nextjs.org/) frontend application
- `api`: a [FastAPI](https://fastapi.tiangolo.com/) backend application
- `@repo/ui`: a shared React component library used by the frontend
- `@repo/eslint-config`: `eslint` configurations (includes `eslint-config-next` and `eslint-config-prettier`)
- `@repo/typescript-config`: `tsconfig.json`s used throughout the monorepo
- `@repo/shared`: shared types and utilities between frontend and backend

Each package/app is 100% [TypeScript](https://www.typescriptlang.org/).

### Tech Stack

- **Frontend**: Next.js 14 with App Router
- **Backend**: FastAPI with Python 3.11+
- **Database**: PostgreSQL (configurable)
- **Authentication**: JWT-based auth system
- **API Documentation**: Swagger/OpenAPI (FastAPI)
- **Type Safety**: TypeScript + Python type hints
- **Package Manager**: pnpm

### Utilities

This Turborepo has some additional tools already setup for you:

- [TypeScript](https://www.typescriptlang.org/) for static type checking
- [ESLint](https://eslint.org/) for code linting
- [Prettier](https://prettier.io) for code formatting
- [Black](https://black.readthedocs.io/) for Python code formatting
- [isort](https://pycqa.github.io/isort/) for Python import sorting
- [mypy](https://mypy.readthedocs.io/) for Python type checking

### Build

To build all apps and packages, run the following command:

```sh
cd my-turborepo
pnpm build
```

### Develop

To develop all apps and packages, run the following command:

```sh
cd my-turborepo
pnpm dev
```

This will start:
- Next.js frontend on http://localhost:3000
- FastAPI backend on http://localhost:8000
- API documentation on http://localhost:8000/docs

### Package Management

This project uses pnpm workspaces for managing dependencies. Key pnpm commands:

```sh
# Install dependencies
pnpm install

# Add a dependency to a specific workspace
pnpm add <package> --filter <workspace>

# Add a dev dependency to a specific workspace
pnpm add -D <package> --filter <workspace>

# Run a script in a specific workspace
pnpm --filter <workspace> <script>
```

### Remote Caching

> [!TIP]
> Vercel Remote Cache is free for all plans. Get started today at [vercel.com](https://vercel.com/signup?/signup?utm_source=remote-cache-sdk&utm_campaign=free_remote_cache).

Turborepo can use a technique known as [Remote Caching](https://turborepo.com/docs/core-concepts/remote-caching) to share cache artifacts across machines, enabling you to share build caches with your team and CI/CD pipelines.

By default, Turborepo will cache locally. To enable Remote Caching you will need an account with Vercel. If you don't have an account you can [create one](https://vercel.com/signup?utm_source=turborepo-examples), then enter the following commands:

```sh
cd my-turborepo
npx turbo login
```

This will authenticate the Turborepo CLI with your [Vercel account](https://vercel.com/docs/concepts/personal-accounts/overview).

Next, you can link your Turborepo to your Remote Cache by running the following command from the root of your Turborepo:

```sh
npx turbo link
```

## Project Structure

```
my-turborepo/
├── apps/
│   ├── web/          # Next.js frontend
│   └── api/          # FastAPI backend
├── packages/
│   ├── ui/           # Shared UI components
│   ├── shared/       # Shared types and utilities
│   ├── eslint-config/
│   └── typescript-config/
├── pnpm-workspace.yaml
└── package.json
```

## Useful Links

Learn more about the power of Turborepo:

- [Tasks](https://turborepo.com/docs/crafting-your-repository/running-tasks)
- [Caching](https://turborepo.com/docs/crafting-your-repository/caching)
- [Remote Caching](https://turborepo.com/docs/core-concepts/remote-caching)
- [Filtering](https://turborepo.com/docs/crafting-your-repository/running-tasks#using-filters)
- [Configuration Options](https://turborepo.com/docs/reference/configuration)
- [CLI Usage](https://turborepo.com/docs/reference/command-line-reference)
