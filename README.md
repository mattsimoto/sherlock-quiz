# The Baker Street Academy

A browser-based Sherlock Holmes trivia game built from the original Sherlock Holmes works of Sir Arthur Conan Doyle.

## Current game
- 5 unlockable levels
- 50 questions
- Multiple-choice and typed-answer questions
- Immediate answer explanations
- 10- and 20-point difficulty tiers
- 70% score required to unlock the next level
- Progress and best scores saved with localStorage
- Responsive Victorian casebook-inspired interface
- No framework or build process required

## Run locally
Open `index.html` in a browser.

For a local web server:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Structure
- `index.html` — application shell
- `style.css` — interface and responsive design
- `questions.js` — level and question database
- `app.js` — game state, scoring, unlocking, and persistence

## Next development targets
Expand the Canon into themed paths covering all four novels and 56 short stories; add streaks, ranks, achievements, lives/hints, daily cases, question randomization, richer typed-answer grading, accessibility controls, and optional sound.

Questions should be checked against Conan Doyle's original text before release.