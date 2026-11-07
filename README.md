# salvage-bots

Source for [Salvage Bots](https://autofire.beeliever.net), a playable browser game, installable as a PWA.

A single static site, no build step. `index.html` is the whole game; `manifest.webmanifest`, `sw.js` and the icons are its PWA wiring.

Deployed by Cloudflare Pages from this repo. Pushes to the principal branch deploy automatically.

This repo's deployment is served at [salvage-bots.beeliever.net](https://salvage-bots.beeliever.net). The older address, autofire.beeliever.net, still serves the last zip-uploaded copy from the previous project until the domain is moved to this one.

Working files (design pool, journey log, packaging script) live outside this repo. A new game build is published by copying the assembled package files over the ones here, bumping the cache name in `sw.js` (currently `salvage-bots-v4`), committing and pushing. The cache bump is not optional: without it, installed copies keep serving the older build.
