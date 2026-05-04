# Agent Notes for Local Development

This repo is configured for local development in this environment.

## Git Remotes

- `origin`: `https://github.com/tunaSandwichCursor/cal.diy.git` (your fork)
- `upstream`: `https://github.com/calcom/cal.diy.git` (source project)
- Local `main` tracks `origin/main`.

## First-Time Setup

1. Install dependencies:
   - `yarn`
2. Create env file:
   - `cp .env.example .env`
3. Set required secrets in `.env`:
   - `NEXTAUTH_SECRET` (random base64 string)
   - `CALENDSO_ENCRYPTION_KEY` (random base64 string)

## Start Local Stack

- Start Docker runtime first (OrbStack or Docker Desktop).
- Run:
  - `yarn dx`

This starts Postgres, Mailhog, and the web app.

## Local URLs

- App: `http://localhost:3000`
- Login: `http://localhost:3000/auth/login`
- Mailhog: `http://localhost:8025`
- Prisma Studio (optional): `yarn db-studio` then `http://localhost:5555`

## Simple Login

The seeded dev user from `yarn dx`:

- Email: `free@example.com`
- Password: `free`

## Stop Services

- Stop app process by ending the `yarn dx` terminal.
- Stop containers:
  - `docker compose down`
