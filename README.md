# Águila Integrated Systems

A responsive static website proof of concept. There is no backend, build process, dependency installation, analytics, or external asset request.

## Clickable previews for reviewers

Use Netlify Deploy Previews for a clickable website link on each pull request, with no GitHub or downloads required for visual review. See [one-time setup and the editing workflow](docs/preview-setup.md). The account owner must connect Netlify to this repository before automatic previews work. Hostinger remains separate.

## Local preview

From this folder, run:

```sh
python3 -m http.server 8000 --bind 0.0.0.0
```

Open `http://localhost:8000` in your own browser. Stop the server with Ctrl+C. You can also open `index.html` directly in a browser.

## Make changes through Codex

Ask Codex to create a feature branch, make the requested changes, preview and test them, and open a pull request targeting `main`. Ask Codex for the Netlify Deploy Preview link, review the running site, and manually merge only when satisfied. See `AGENTS.md` for project guidelines.

## Files

- `index.html`: page content, navigation, and concept eagle artwork.
- `styles.css`: colors, typography, and desktop/mobile layouts.
- `script.js`: keyboard-focus enhancement for page links.
- `favicon.svg`: matching local browser icon.
- `AGENTS.md`: instructions for future Codex changes.

Contact details are placeholders. Replace them with owner-supplied information before launch. The eagle mark is a design concept. Publishing to Hostinger is outside this proof of concept; the HTML, CSS, JavaScript, and favicon files can eventually be uploaded together without a build.

## Proof-of-concept review

Browser checks passed in Chromium at 1440, 768, 390, and 320 pixels: navigation targets and focus, no horizontal overflow, successful asset requests, UTF-8 rendering, and no console or JavaScript errors. The keyboard skip link was also checked. Contact information remains an explicit placeholder; there is no contact submission backend.

Captured previews (static images): [desktop](docs/previews/desktop.png) · [mobile](docs/previews/mobile.png).
