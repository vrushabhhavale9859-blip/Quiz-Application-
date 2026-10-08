# Quiz Application

A browser-based quiz app built with plain HTML, CSS and JavaScript. No installation, frameworks or internet connection needed.

## Features (Feature Set A)

| Feature | How it works |
|---|---|
| Category selection | Choose from General Knowledge, Science, Technology or Geography on the home screen. |
| 10 questions | Each round picks 10 questions from the chosen category, in random order. |
| Timer | 15 seconds per question, with a countdown and progress bar. When time runs out, the question counts as unanswered. |
| Score calculation | Correct answer = 10 points + 1 bonus point for every 3 seconds left. Wrong or unanswered = 0. |
| Final result | Shows total score, correct count, accuracy, a message, and a review of every question with the correct answer. |

## How to Run

1. Download `quiz-app.html`.
2. Open it in any modern browser (Chrome, Edge, Firefox, Safari).

That's it. Everything is in one file.

## How to Play

1. Tap a category.
2. Read the question and tap one answer before the timer ends.
3. The correct answer is highlighted. Tap **Next question**.
4. After question 10, view your results. Choose **Play again** or **Change category**.

## Project Structure

```
quiz-app.html   # HTML structure, CSS styles and JavaScript logic
README.md       # This file
```

Inside `quiz-app.html`:

- `<style>`: layout, colors, light/dark theme and responsive design.
- `DATA`: the question bank. Each question is `[question, [options], correctIndex]`.
- `start()`, `load()`, `answer()`, `finish()`: the main game flow.

## Customization

- **Add a question:** add a new entry to a category in `DATA`, for example:
  `["Capital of Italy?", ["Rome","Milan","Turin","Naples"], 0]`
- **Add a category:** add a new key in `DATA` with at least 10 questions. It appears on the home screen automatically.
- **Change the time limit:** edit `PER_Q` (seconds per question) at the top of the script.
- **Change scoring:** edit the line `pts = 10 + Math.floor(left / 3)` in `answer()`.

## Technologies

- HTML5
- CSS3 (CSS variables, grid, automatic dark mode)
- Vanilla JavaScript (ES6)
