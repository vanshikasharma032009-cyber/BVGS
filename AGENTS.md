# Agent instructions

## Project overview
- This is a static school website built with HTML, CSS, and vanilla JavaScript.
- Pages are in the repository root: `index.html`, `about.html`, `academics.html`, `admissions.html`, `facilities.html`, `gallery.html`, and `contact.html`.
- Shared styling is in `css/style.css`; shared interactions are in `js/main.js`.
- Images and other visual assets are stored in `images/`.

## Development guidelines
- Keep changes focused and follow the existing visual style and accessible HTML patterns.
- When changing shared navigation, footer, or site-wide components, keep all pages consistent.
- Use local image assets with paths relative to the HTML page. Give meaningful `alt` text to informative images.
- Keep layouts responsive for desktop and mobile.
- Do not add a framework or dependency for a change that can be handled with the existing HTML, CSS, and JavaScript.
- Preserve existing user edits and avoid unrelated changes.

## Validation
- Run `node --check js/main.js` after JavaScript changes.
- Run `git diff --check` before finishing.
- Check that referenced local image files exist and that navigation links point to valid pages.
