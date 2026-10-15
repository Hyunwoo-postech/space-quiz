# Copilot instructions

## Project structure and architecture

This project is a single-page space quiz implemented entirely in `index.html`. The document contains the semantic page markup, inline CSS, quiz data, and vanilla JavaScript; there is no framework, module system, backend, or separate asset pipeline.

The `questions` array is the source of truth for question text, categories, answer choices, correct-answer indexes, and explanations. The script renders each question into the existing page, tracks the current question and score, updates progress and feedback after an answer, and switches to a results view at the end. Restart resets the quiz state and renders the first question again. Keep changes consistent across this data, the DOM elements in the document, and the quiz state transitions.

## Project-specific conventions

- Keep the app self-contained in `index.html`; use the existing DOM IDs as the interface between markup and script.
- The UI is built with semantic HTML and CSS custom properties. Preserve the existing responsive layout, light/dark color-scheme support, and reduced-motion behavior when changing styles.
- Build dynamic question content with DOM APIs. Set user-facing text with `textContent` or text nodes rather than interpolating it into HTML.
- Preserve the accessibility patterns already used: labels and live regions for status/progress, visible keyboard focus, focus movement when advancing or showing results, and disabled answer buttons after selection.

## Build, test, and lint

There are no configured build, test, or lint commands, and no automated single-test runner. To check a change, open `index.html` in a browser and manually play through the quiz: select correct and incorrect answers, advance through the final question, confirm the results, and restart. Also check a narrow viewport and light/dark color schemes when changing layout or styling.
