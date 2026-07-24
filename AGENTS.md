# AGENTS.md

## Cursor Cloud specific instructions

This is a Fern-powered documentation site for Credal. There is no database, Docker, or backend service — just the Fern CLI.

### Key commands

| Task | Command |
|------|---------|
| Validate docs/API definitions | `fern check` |
| Local dev server (hot-reload) | `fern docs dev` |
| Generate hosted preview | `FERN_TOKEN=<token> fern generate --docs --preview` |
| Publish docs | `FERN_TOKEN=<token> fern generate --docs` |

### Caveats

- `fern docs dev` starts a backend on port 3001 and a frontend on port 3000. The first startup takes ~20-30 seconds to bootstrap the docs preview bundle.
- `fern check` may report warnings (e.g. about unused types); 0 errors is the passing criterion used in CI.
- Publishing and preview generation require a `FERN_TOKEN` environment variable (not needed for local dev or `fern check`).
- The Fern CLI version is pinned in `fern/fern.config.json` (`"version": "4.18.0"`). Running `npm install -g fern-api` installs whatever version is specified there.
