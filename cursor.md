# Amzua Project 01 — Cursor instructions

This file is project context for Cursor. Keep it short and update it as conventions settle.

## Project

- Name: Amzua Project 01
- Status: new workspace
- Prefer small, focused changes. Do not invent extra files or features unless asked.

## Tech stack

- Runtime: Node.js
- Language: TypeScript (strict; no `any` unless unavoidable)
- Framework: Next.js (App Router)
- UI: React Server Components by default; Client Components only when interactivity or browser APIs are required
- Styling: follow whatever CSS approach already exists in the repo (CSS Modules, Tailwind, etc.)
- Package manager: use the lockfile already in the repo (`npm`, `pnpm`, or `yarn`)

## TypeScript / Next.js conventions

- Use the App Router under `app/` (`page.tsx`, `layout.tsx`, `route.ts`).
- Colocate route-specific components with the route; put shared UI in `components/`.
- Server-side data fetching in Server Components or Route Handlers; do not fetch from the client unless needed.
- API / server logic: Route Handlers in `app/api/**/route.ts` or server-only modules — never import server secrets into Client Components.
- Prefer typed props, typed API responses, and `unknown` + narrowing over `any`.
- Keep `"use client"` at the leaf; do not mark whole trees as client unless required.

## How to work in this repo

- Match existing language, naming, and folder layout once code exists.
- Do not commit, push, or change git config unless the user asks.
- Do not add README, tests, or docs unless the user asks.
- Secrets stay out of git: `.env`, `.env.local`, credentials, API keys, tokens.
- Use `process.env` only on the server unless the variable is prefixed `NEXT_PUBLIC_`.

## When implementing UI

- Verify the changed flow in the browser (or the closest substitute) before calling the work done.
- Check related pages that share the same state, data, or components.
- Hunt for regressions, not only the happy path.
- Check desktop and mobile if layout or styling changed.
