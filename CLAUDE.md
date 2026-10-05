# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Install dependencies
npm install

# Start (production)
npm start

# Start with auto-reload (development)
npm run dev

# Run all tests
npm test

# Run a single test file
npx jest tests/path/to/file.test.js
```

## Architecture

This is a minimal Express REST API.

- `src/index.js` — entry point: loads `.env`, starts the HTTP server
- `src/app.js` — Express app setup (JSON body parsing, mounts router at `/api`)
- `src/routes/index.js` — route definitions; add new routes here
- `config/index.js` — central config object reading from `process.env`

All routes are prefixed with `/api`. The only current endpoint is `GET /api/health`.

Tests go in `tests/` and are picked up automatically by Jest.
