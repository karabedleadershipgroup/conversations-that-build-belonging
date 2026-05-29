# Conversations That Build Belonging — Companion

An AI-powered, bilingual practice companion for the *Conversations That Build Belonging* training by Dr. Isa Karabed, DSW.

The training teaches a simple framework — **WHY → WHAT → HOW** — for responding in ways that build belonging instead of erode it, especially in moments when culture is tested.

## What this is

A single-page web app with six ways into the training:

1. **Ask Dr. Isa** — conversational, in her voice.
2. **Curriculum Refresher** — the heart of the training, one idea at a time.
3. **Ask for Guidance** — bring a real situation, get coached through WHY → WHAT → HOW.
4. **Scenario Practice** — multiple-choice flashcards with real-world moments.
5. **Assumption Trap Spotter** — short snap-judgment cards.
6. **Concept Check** — quick recall on the framework.

Bilingual English / Spanish. KLG brand.

## Architecture

- `index.html` — the full single-page app (HTML + CSS + JS, all in one file).
- `netlify/functions/chat.js` — serverless function that proxies to the Anthropic API. The browser never sees the API key.
- `netlify.toml` — Netlify config (publish root, functions folder, `/api/chat` redirect).

## Deploy

1. Push this repo to GitHub.
2. In Netlify, **Add new site → Import an existing project**, connect this repo. Build settings are read from `netlify.toml` — leave them as-is.
3. In **Site settings → Environment variables**, add `ANTHROPIC_API_KEY` with your Anthropic key. Redeploy.
4. Open the site.

## Local development

```bash
npm install -g netlify-cli
netlify dev
```

Set `ANTHROPIC_API_KEY` in a local `.env` file (don't commit it).

## License

© Karabed Leadership Group. All rights reserved.
