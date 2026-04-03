# 📰 Guess the Headlines — Quiz Game

A party quiz game where teams must identify the one **real** news headline buried among two convincing fakes.

---

## How to Run

Just open `guess-the-headlines.html` in any modern browser. No server, no installation, no internet required after the first load (it pulls React and Tailwind from CDN on first open).

---

## How to Play

### Setup
1. Open the file and choose how many teams (2–6).
2. Enter custom team names if you like.
3. Hit **Start Game**.

### During the Game (Quiz Master runs this screen)
- The **QM Dashboard** shows all questions in a grid, with which team answers each one.
- Click a question card to launch it.
- The **"👁 QM: Show Answer"** button in the top-right of the question screen reveals the correct answer and trivia **only on your screen** — use it to stay one step ahead.
- Read the three headlines out loud (or turn the screen to face the team).

### Scoring
| Attempt | Points |
|---------|--------|
| Correct on first guess | **20 pts** |
| Correct on second guess | **10 pts** |
| Both wrong | **0 pts** |

After each answer, the game reveals which headline was real and shows a short trivia blurb. Hit **"Back to Dashboard"** to move on.

### End of Game
Click **"🏆 Final Scores"** from the dashboard at any time to see the ranked leaderboard.

---

## Adding More Questions

Open `guess-the-headlines.html` in a text editor and find the `ALL_QUESTIONS` array near the top of the `<script>` block. Each question follows this format:

```js
{
  id: 16,                        // unique number — used as the question label
  options: [
    { letter: "A", text: "Headline option A" },
    { letter: "B", text: "Headline option B" },
    { letter: "C", text: "Headline option C" },
  ],
  answer: "A",                   // the correct letter
  trivia: "The real story behind the headline, shown after the reveal.",
},
```

Questions are automatically distributed to teams in round-robin order (Q1 → Team 1, Q2 → Team 2, etc.), so you don't need to assign them manually.

---

## Included Questions (Q10–Q15)

| Q  | Real Headline | Source |
|----|---------------|--------|
| Q10 | Raccoon goes on drunken rampage in Virginia liquor store | AP News |
| Q11 | A red fox stows away on a cargo ship, England to the US | AP News |
| Q12 | Nestlé: 413,793 KitKat bars stolen en route Italy → Poland | AP News |
| Q13 | Finnish pair wins barrel of ale in UK wife-carrying contest | AP News |
| Q14 | Longest line at Philly airport? Cheesesteaks, not security | AP News |
| Q15 | Atlanta Hawks plan Magic City tribute night with T.I. | AP News |

---

## Tips for Hosts

- Project the screen onto a TV or monitor so all teams can see the three options.
- Use the **"👁 QM: Show Answer"** toggle discreetly — it appears only in your browser tab.
- For best pacing: read each headline with dramatic flair, pause for effect, then let the team confer before guessing.
- Questions marked ✓ Done are greyed out on the dashboard — you can't accidentally re-play them.

---

## Tech Stack

- **React 18** (via CDN) — UI and state management
- **Tailwind CSS** (via CDN) — styling
- **Babel Standalone** (via CDN) — JSX transpilation in the browser
- Zero build step, zero dependencies to install# guessheadline
