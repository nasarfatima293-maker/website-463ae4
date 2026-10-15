# AI Mike — AI Testing & Evaluation Platform

AI Mike is a browser-based workspace for evaluating AI model responses. You enter a prompt, the model's response, and a trusted reference answer. It then reports a word-overlap similarity score and an exact-match flag, and lets you save each evaluation to a session history that can be exported as CSV.

## Technologies

- A single static `index.html` with inline CSS and vanilla JavaScript (no framework, no build step)
- Hosted on Netlify (`netlify.toml` publishes the repository root)

## Running locally

Open `index.html` in a browser, or serve it locally:

```bash
netlify dev --port 8889
```

## Possible next steps

- Persist evaluation history across sessions (for example with Netlify Database)
- User accounts and shared test sets
- Semantic or model-graded scoring in addition to word overlap
