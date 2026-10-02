# catalog-ts-nestjs-template

A minimal **TypeScript + NestJS** starter used by DayZer0 catalog briefs. It is a
generic starting point — the framework wired up and nothing brief-specific. Build
your first feature on top of it.

## What's here

- NestJS app (`@nestjs/core`, `@nestjs/common`, `@nestjs/platform-express`).
- A **global `ValidationPipe`** (`whitelist: true`, `forbidNonWhitelisted: true`)
  enabled in `src/main.ts`, so DTO validation is on everywhere.
- `class-validator` and `class-transformer` installed, ready for your DTOs.
- A health route: `GET /healthz` → `{ "status": "ok" }`.

## Run it

```bash
npm install
npm run start:dev      # ts-node, no build step
# or
npm run build && npm run start
```

Then confirm the health route:

```bash
curl localhost:3000/healthz
# {"status":"ok"}
```

## Layout

```
src/
  main.ts            bootstrap + global ValidationPipe
  app.module.ts      root module
  app.controller.ts  GET /healthz
```

Add your feature module under `src/` and register it in `app.module.ts`.
