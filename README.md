# vibetype

Speed-typing practice for the phrases you actually fire at an AI coding agent —
`continue`, `make it work`, `you're absolutely right`, `ultrathink`, and friends.

A single, dependency-free `index.html`. Type the phrase shown; it color-codes your
keystrokes, tracks live WPM / accuracy / best, and an agent-voice line acks every run.
Phrases are drawn from a shuffle bag so each cycles once before any repeats.

- **type** to play · **⌫** fix · **⇥** skip phrase · **esc** reset session
- click a category chip to filter the drill

## Run locally

It's a static file — open it directly:

```sh
open index.html
```

Or serve it (any static server works):

```sh
npx serve .
```

## Deploy to Vercel

This is a zero-config static site (no build step). Two ways:

**CLI**

```sh
npm i -g vercel
vercel        # preview deploy
vercel --prod # production deploy
```

**Git import**

1. Push this folder to a GitHub/GitLab/Bitbucket repo.
2. In the Vercel dashboard: **Add New → Project**, import the repo.
3. Framework Preset: **Other**. Leave Build Command and Output Directory empty.
4. **Deploy.**

`vercel.json` sets clean URLs, a no-cache header on the HTML so updates show
immediately, and a few baseline security headers. Fonts load from Google Fonts
with monospace/system fallbacks, so the app still works offline.
