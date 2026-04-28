# Workspace

## Overview

pnpm workspace monorepo using TypeScript. Each package manages its own dependencies.

## Stack

- **Monorepo tool**: pnpm workspaces
- **Node.js version**: 24
- **Package manager**: pnpm
- **TypeScript version**: 5.9
- **API framework**: Express 5
- **Database**: PostgreSQL + Drizzle ORM
- **Validation**: Zod (`zod/v4`), `drizzle-zod`
- **API codegen**: Orval (from OpenAPI spec)
- **Build**: esbuild (CJS bundle)

## Portfolio Artifact

The `artifacts/portfolio` package is a React + Vite portfolio website for Shiv Yadav (WebCraft Developer).

### Features
- Full single-page portfolio: Hero, About, Skills, Projects, Services, TechLogos, Contact, Footer
- Dark/light mode, custom cursor, scroll progress bar, loading screen, back-to-top
- 7 real-world business project pages with internal routing via wouter:
  - `/project/cafe` — Cafe website with menu, cart, table booking
  - `/project/shop` — E-commerce shop with cart state and checkout
  - `/project/ca` — CA/Accounting dashboard with recharts
  - `/project/restaurant` — Restaurant with tabbed menu, reservations, reviews
  - `/project/clinic` — Clinic with doctor profiles and appointment booking
  - `/project/realestate` — Real estate listings with filters and property detail
  - `/project/dashboard` — Full admin panel with dark sidebar, charts, data tables

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
