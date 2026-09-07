# Drop the Needle

A fast music-trivia game for people who actually know music.

## Current game loop

- 10-question rounds
- Primarily multiple choice
- One click answers a question
- Immediate correct-answer reveal
- Short music-history payoff after every answer
- Plausible distractors rather than random wrong answers
- Questions carry editorial verification status

## Project structure

- `index.html` — current playable prototype
- `data/questions.json` — canonical question bank

## Run locally

Because the question bank is loaded as JSON, serve the folder over HTTP rather than double-clicking `index.html`.

From the repository folder:

```powershell
python -m http.server 8000
```

Then open `http://localhost:8000`.

Stop the server with `Ctrl+C`.

## Editorial rule

A question is not production-ready merely because it exists in the bank.

- `verified` — source-checked and eligible for production
- `review` — plausible/currently usable for development, but needs source review
- `unverified` — do not ship until the specific claim and wording are verified

The goal is not generic pub trivia. A good Drop the Needle question should reward real music knowledge or leave a serious music fan thinking, “I didn't know that.”

## Status

Prototype stage. Core interaction is intentionally small and largely frozen while the question bank is curated and verified.
