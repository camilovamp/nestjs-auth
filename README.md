# nestjs-auth

**Production-ready authentication & authorization starter for NestJS.**

Built with **NestJS, PostgreSQL, Prisma**, and modern security best practices.

## Tech Stack

- Node.js 20+
- NestJS
- PostgreSQL
- Prisma ORM
- JWT
- Docker & Docker Compose
- npm


## Requirements

- Docker + Docker Compose
- Node.js 20+
- npm or pnpm (local development)

## Quick start (Docker)

```bash
docker-compose up --build
```

## Or local(without Docker)

```bash
npm install
npm run start:dev
```

API will be available at:

- http://localhost:3000
- Swagger UI: http://localhost:3000/docs
- Health check: http://localhost:3000/health

## Environment

The default Docker database credentials are defined in `docker-compose.yml`:

- user: `postgres`
- password: `postgres`
- database: `nestjs_auth`

The app uses `.env` for `DATABASE_URL`. For Docker, it should point to the `db`
service, e.g.:

```
DATABASE_URL="postgresql://postgres:postgres@db:5432/nestjs_auth"
```

## example .env

# App
NODE_ENV=development
PORT=3000
APP_URL=http://localhost:3000

# Database
DATABASE_URL="postgresql://postgres:postgres@db:5432/nestjs_auth"

# JWT
JWT_ACCESS_SECRET=replace_me_access
JWT_REFRESH_SECRET=replace_me_refresh
JWT_ACCESS_TTL_SECONDS=900
JWT_REFRESH_TTL_SECONDS=2592000

# Token hashing
TOKEN_PEPPER=replace_me_long_random_string

# Email
EMAIL_PROVIDER=console
EMAIL_FROM="NestJS Auth <no-reply@example.com>"
