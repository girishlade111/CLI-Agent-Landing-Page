# CLI AI Assistant — Landing Page

A static marketing website for a terminal-based AI coding agent: "Your Terminal. Your Models. Your AI." Pure HTML, CSS, and vanilla JavaScript — no build step, no dependencies.

Part of the LadeStack open-source collection.

## Features

- **Landing page** (`index.html`) — hero, features, and CTAs for the CLI AI assistant
- **CLI spec page** (`pages/cli-spec.html`) — detailed product/spec documentation
- **Roadmap** (`pages/roadmap.html`) — product roadmap
- **Vision** (`pages/vision.html`) — product vision
- **Team** (`pages/team.html`) — team page
- **Design spec** (`website-design-specification.md`) — full design specification used to build the site
- **Zero build tooling** — hand-written CSS (`css/styles.css`) and vanilla JS (`js/main.js`); opens directly in any browser

## Tech Stack

- HTML5
- CSS3 (custom stylesheet, no framework)
- Vanilla JavaScript

## Project Structure

```
CLI-Agent-Landing-Page/
├── index.html                      # Landing page entry
├── css/
│   └── styles.css                  # Site-wide styles
├── js/
│   └── main.js                     # Site interactivity
├── pages/
│   ├── cli-spec.html               # Product/spec page
│   ├── roadmap.html                # Roadmap page
│   ├── team.html                   # Team page
│   └── vision.html                 # Vision page
└── website-design-specification.md # Design specification
```

## Quick Start

No installation needed. Serve the folder with any static server:

```sh
npx serve .
```

Or open `index.html` directly in a browser.

## Deployment

Static files — deploy as-is to GitHub Pages, Netlify, Vercel, or Cloudflare Pages. No build step, no environment variables.

## License

MIT

---

Built by Girish Lade — https://ladestack.in
