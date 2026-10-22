# Amzua Project 01

New Node.js workspace. The intended app stack is **Next.js (App Router)**, **TypeScript**, and **React**.

## Status

Early setup. The repo currently has a Node package and `dotenv`; the Next.js app (`app/`, pages, UI) is not in place yet.

## Requirements

- [Node.js](https://nodejs.org/) (LTS recommended)
- npm (lockfile is `package-lock.json`)

## Setup

```bash
npm install
```

Copy environment variables into a local file (do not commit secrets):

```bash
# .env or .env.local
```

Load them with `dotenv` on the server. In a Next.js app, only variables prefixed `NEXT_PUBLIC_` should be used on the client.

## Scripts

| Script | Description |
| --- | --- |
| `npm test` | Placeholder (no tests yet) |

## Conventions

- TypeScript, strict; avoid `any` unless there is no better type.
- App Router under `app/` (`page.tsx`, `layout.tsx`, `route.ts`).
- React Server Components by default; Client Components only when interactivity or browser APIs are required.
- Shared UI in `components/`; route-specific UI next to the route.
- Server data fetching in Server Components or Route Handlers (`app/api/**/route.ts`).
- Keep secrets out of git (`.env`, `.env.local`, credentials, API keys).

## License

ISC
