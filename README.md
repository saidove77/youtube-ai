# بوصلة الشرق AI — TypeScript edition

Backend starter built with Node.js 22+, TypeScript, Fastify and Prisma. Python and ElevenLabs are not included.

## Run on Windows

1. Install Node.js 22 LTS and Git.
2. Open PowerShell in this folder.
3. Run:

```powershell
Copy-Item .env.example .env
npm install
npm run dev
```

4. Open `http://127.0.0.1:8000` and `http://127.0.0.1:8000/api/v1/health`.

## Database (local prototype)

```powershell
npm run db:generate
npm run db:migrate
```

The starter uses SQLite locally. Before continuous cloud operation, migrate to PostgreSQL and configure backups.

## Voice engine

The project intentionally has no voice vendor hard-coded. `src/modules/voice/provider.ts` defines a provider-neutral interface. We will compare Arabic Modern Standard Arabic voice cloning quality, API support, licensing, data handling and price before selecting a replacement. Use only your own voice or a voice with explicit permission.

## Safety defaults

- No automatic YouTube publishing or live broadcasting is enabled.
- API keys belong in `.env` locally or a server secret manager, never in GitHub.
- News must pass source verification and editorial checks before production.
