# Nexus Chess

Chess in the browser: standard, bughouse, and 4-player, with online rooms. Installs as a home-screen app.

**Play:** https://calvinslinde.github.io/chess/

## What's here

- `index.html`, `js/`, `styles.css`: the game. No build step, no framework.
- `worker.js`, `wrangler.toml`: the Cloudflare Worker that hosts online rooms (a room is a Durable Object; a global store lists open rooms).
- `sw.js`, `manifest.json`: offline support and install-to-home-screen.

## Run it locally

Open `index.html` through any static file server, for example:

```
python3 -m http.server 8000
```

Then visit http://localhost:8000/. Local play works without the worker; online rooms need the worker deployed with `npx wrangler deploy` from this folder and the worker URL set in `js/`.

Built with Claude.
