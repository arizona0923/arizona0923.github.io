# Adriel Arizona — Personal Portfolio

Personal web portfolio for Adriel Arizona — Digital Marketing Manager, AI builder, and operator based in Chicago, IL.

Live site: https://arizona0923.github.io/ _(adjust to your final URL)_

## Structure

- `index.html` — main portfolio (single-file, self-contained except Google Fonts)
- `404.html` — custom error page that matches the portfolio aesthetic
- `assets/` _(optional)_ — drop in any local images here (avatar, polaroids, OG image) when ready

## Tech

Pure HTML/CSS/vanilla JS. No build step. No dependencies beyond Google Fonts.

## Sections

1. **Hero** — terminal, ID badge, polaroid stack, iPod, live status bar with cycling notifications
2. **Behind the build** — Notion clipboard intro + iPhone widget stack (Substack/YouTube/apps)
3. **Receipts** — macOS desktop scene with stats strip, 7-slide pitch deck, and 2 desktop folders with cascading Finder windows
4. **Pick your inbox** — iMessage thread + pinned business card on corkboard

## Features

- Dark mode (toggle in nav, persists via localStorage, also flips the 404 page)
- Cycling status notifications (9 messages on rotation)
- Live ticking clock + slow battery drain + Slack status cycle
- Smooth scroll with pulse-highlight on Contact link
- Konami code easter egg (↑↑↓↓←→←→ba)
- Click-anywhere-on-terminal easter egg
- Draggable, cascading folder windows in the desktop scene
- Fully responsive (mobile collapses to single column)
- Respects `prefers-reduced-motion`

## Hosting on GitHub Pages

1. Push both files to the root of your repo
2. Settings → Pages → Source = "Deploy from a branch" → `main` / `/ (root)`
3. Your site will be at `https://<username>.github.io/<repo-name>/`
4. For a custom domain: add a `CNAME` file with your domain, then configure DNS

## Open items (waiting on real assets)

- [ ] Real song + artist for the iPod (`#trackName` / `#trackArtist`)
- [ ] Spotify Wrapped 2025 URL (auto-syncs to mini player + footer)
- [ ] Real polaroid photos for the hero stack
- [ ] Confirm email — resume has `arizonaadriel@gmail.com`, placeholders use `hello@adrielarizona.com`
- [ ] Resume PDF or URL for the Resume link
- [ ] Photography app link confirmation (currently Unsplash placeholder)
- [ ] Domain decision — when set, wire `og:url` and canonical
- [ ] OG share image (1200×630 PNG)

## Updating with new projects

To add a new project tile in the desktop folders, edit the `TREE` object inside the `<script>` block in `index.html`. Each item:

```js
{ kind: 'file', name: 'Project name', meta: '+XX% metric', stamp: 'Shipped',
  href: 'https://your-project-url.com',
  thumbCss: 'background: linear-gradient(135deg, #color1, #color2);' }
```

New work experiences go into the pitch deck as a new `<div class="slide split">` block, and the corresponding `<button class="slide-thumb">` in the slide strip.
