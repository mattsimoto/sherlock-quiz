# The Baker Street Academy

A browser-based Sherlock Holmes trivia campaign based on the original Sherlock Holmes works of Sir Arthur Conan Doyle.

## Current game

The project now contains a complete first-pass Canon progression:

- **24 unlockable levels**
- **240 questions**
- **6 campaign arcs**
- **196 multiple-choice questions**
- **44 typed-answer questions**
- Immediate answer explanations
- Difficulty tiers worth 10–40 points per correct answer
- **70% required to solve a level and unlock the next case**
- Highest score on each level determines Canon mastery
- Seven player ranks from **New Lodger** through **Canon Master**
- Progress and best scores saved locally in the browser
- Responsive Victorian casebook-inspired interface
- No framework or build process required

## Campaign structure

### Arc 1 — The Game Is Afoot
1. A Study in Scarlet
2. The Sign of Four
3. A Scandal and a League
4. The Speckled Band and the Blue Carbuncle

### Arc 2 — The Adventures
5. The Five Orange Pips and the Twisted Lip
6. The Engineer and the Noble Bachelor
7. The Beryl Coronet and the Copper Beeches
8. Boscombe Valley and a Case of Identity

### Arc 3 — The Memoirs
9. Silver Blaze
10. The Yellow Face and the Stockbroker's Clerk
11. The Gloria Scott and the Musgrave Ritual
12. Secrets, Treaties and Reichenbach

### Arc 4 — The Return
13. The Empty House
14. The Norwood Builder and the Dancing Men
15. Cyclists, Schoolboys and Black Peter
16. The Later Return Cases

### Arc 5 — The Great Novels and the Last Bow
17. The Hound of the Baskervilles
18. The Valley of Fear
19. From Wisteria Lodge to His Last Bow
20. The Canon's Great Adversaries

### Arc 6 — The Case-Book and Canon Mastery
21. The Illustrious Client to the Three Gables
22. Vampires, Garridebs, Thor Bridge and the Creeping Man
23. The Lion's Mane to the Retired Colourman
24. The Canon Master's Examination

## Rank progression

Ranks are based on the number of levels solved at 70% or higher:

- 0 solved — New Lodger
- 4 solved — Baker Street Regular
- 8 solved — Investigator
- 12 solved — Consulting Detective
- 16 solved — Senior Detective
- 20 solved — Master of Deduction
- 24 solved — Canon Master

## Scoring

Early cases award fewer points per question; later and more obscure Canon material awards more.

The displayed mastery-point total is based on the player's **best score on each level**, so repeatedly replaying an easy level cannot inflate the campaign total.

## Run locally

Open `index.html` directly in a browser, or run:

```bash
python3 -m http.server 8000
```

Then visit `http://localhost:8000`.

## Structure

- `index.html` — application shell and data loading
- `style.css` — interface and responsive campaign design
- `questions.js` — campaign constants, pass score, and rank ladder
- `data/arc-1.js` through `data/arc-6.js` — Canon question bank
- `app.js` — rendering, scoring, typed-answer grading, level unlocking, rank calculation, and persistence

## Validation

The current question bank has been structurally checked for:

- 24 sequential level IDs
- Exactly 10 questions per level
- Exactly four distinct choices for every multiple-choice item
- Valid answer indexes
- Accepted-answer arrays for every typed item
- Explanations for every question
- No duplicate question prompts

## Next development phase

The question bank and campaign progression are now large enough to serve as the stable content foundation. The next phase can focus on game mechanics and presentation rather than adding raw volume: randomized question order, lives, hints, streaks, achievements, daily cases, richer answer tolerance, sounds, accessibility controls, and a more visual campaign map.

Before a public release, the question bank should receive a final editorial fact-check against authoritative editions of Conan Doyle's original text.
