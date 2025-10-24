# Repository Guidelines

## Project Structure & Module Organization
The site ships as a static build with `index.html` as the production entry point and `index2.html` as an alternative hero layout kept for reference. Both pages embed their CSS and JavaScript inline. Brand assets live in `logo/`, while showcase imagery belongs in `Thumbnails/`; place new files in those folders and reference them with relative paths so deployments remain portable.

## Build, Test, and Development Commands
Serve the site locally to exercise external fonts and icon scripts: `npx serve .` from the repo root works if Node.js is available, and `python -m http.server 8000` is the lightweight fallback. Open `http://localhost:8000/index.html` (or `/index2.html`) in the browser under test once the server is running.

## Coding Style & Naming Conventions
Keep HTML indented with two spaces and prefer semantic wrappers (`section`, `header`, `footer`) when adding blocks. Tailwind utility classes should read left to right as layout > spacing > color > effects. Custom CSS selectors stay in kebab-case, with properties grouped from layout to visuals for quick scanning. Inline JavaScript functions use camelCase names and attach at the bottom of the document before the closing `</body>`.

## Testing Guidelines
Perform visual QA in modern Chromium and WebKit browsers, confirming gradients, Lucide icons, and scroll-triggered reveals behave on both desktop and mobile breakpoints. When updating media, keep individual image assets under ~300 KB and spot-check load time with Lighthouse or the browser’s performance panel. Document manual checks in the pull request to capture coverage.

## Commit & Pull Request Guidelines
Use short, imperative commit subjects such as `Update hero gradient` or `Add portfolio item`, and wrap body text at 72 characters when extra context is required. Squash noisy fixup commits before opening a PR. Pull requests should include: a summary of changes, before/after screenshots of affected sections, steps for local verification, and links to any tracking issues. Tag reviewers responsible for the impacted area (design, content, or build) and wait for at least one approval before merging.
