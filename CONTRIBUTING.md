# Contributing to Firewall Academy

Thanks for your interest in improving this project! It's a single-file, dependency-free learning app, which keeps contributions simple.

## How it's built

Everything lives in **`index.html`** — HTML, CSS, and JavaScript in one file, no build step and no external libraries. Progress is stored in the browser via `localStorage`.

The course content is data-driven. Two JavaScript objects near the bottom of the file hold everything you'd want to edit:

- `CURRICULUM` — the modules, lessons, lesson HTML, and quiz questions.
- `GLOSSARY` — the reference terms.

The rendering engine below those objects reads from them, so adding a lesson or a quiz question usually means editing data, not logic.

## Ways to contribute

- **Fix an error.** Firewall/OPNsense behavior changes over time — corrections are very welcome. Please link a source where practical.
- **Add a quiz question.** Append to the relevant lesson's `quiz` array (`{ q, opts, a, ex }` where `a` is the zero-based index of the correct option).
- **Add or expand a lesson.** Follow the shape of an existing lesson object.
- **Improve accessibility, mobile layout, or styling.**

## Making a change

1. Fork the repo and create a branch: `git checkout -b fix/typo-in-nat-lesson`
2. Edit `index.html`.
3. Open `index.html` in a browser and click through the affected lesson and quiz to confirm it works.
4. Commit with a clear message and open a pull request describing what changed and why.

## Style notes

- Keep it dependency-free and single-file.
- Match the existing tone: concise, practical, and accurate over exhaustive.
- Prefer real-world framing ("here's why this matters") over abstract definitions.

By contributing, you agree your contributions are licensed under the project's MIT License.
