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

## Artifacts

### IMPOSTOR X (`artifacts/impostor-x`)
- **Type**: React + Vite web app
- **Preview Path**: `/`
- **Description**: A social deduction web game inspired by Among Us with a cyberpunk twist
- **Features**:
  - Role assignment (Crewmate vs Impostor) with secret reveal
  - 5 task mini-games: Typing Speed, Memory Flip, Quick Math, Reaction Click, Emoji Decode
  - Fake multiplayer simulation with AI-like NPC chat messages
  - Sound engine using Web Audio API (background music + SFX)
  - Voting phase with suspense animations
  - Sabotage system (blur/shake/invert effects for impostors)
  - Special events: Double Impostor, No Voting, Chaos Mode
  - Particle/stars background canvas
  - Career stats tracked via localStorage
  - Dark cyberpunk UI with neon glow and glassmorphism
  - Orbitron font for the space theme
  - Fully frontend-only (no backend needed)

## Key Commands

- `pnpm run typecheck` — full typecheck across all packages
- `pnpm run build` — typecheck + build all packages
- `pnpm --filter @workspace/api-spec run codegen` — regenerate API hooks and Zod schemas from OpenAPI spec
- `pnpm --filter @workspace/db run push` — push DB schema changes (dev only)
- `pnpm --filter @workspace/api-server run dev` — run API server locally
- `pnpm --filter @workspace/impostor-x run dev` — run the game locally

See the `pnpm-workspace` skill for workspace structure, TypeScript setup, and package details.
