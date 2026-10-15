# AGENTS.md

## Architecture
- Static site: everything lives in `index.html` (inline `<style>` and an inline IIFE `<script>`). No build step, no dependencies.
- `netlify.toml` publishes the repo root (`publish = "."`).

## Behavior
- Tabs (`data-tab` / `data-section`) switch between Evaluate, History, and Method views.
- Scoring: text is normalized (lowercase, NFKC, punctuation stripped), then a Dice-style word-overlap percentage is computed. Exact match compares normalized token strings.
- History is held in memory only and is cleared on page reload. This is intentional: the UI tells users that evaluations stay in their browser session.

## Conventions
- Keep the compact single-file style and the CSS variables in `:root`.
- Render user-supplied text with `textContent` only (never `innerHTML`) to avoid XSS.
