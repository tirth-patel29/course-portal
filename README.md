# MPT Study Portal

A static, mobile-first course portal for Master of Physiotherapy students. It uses plain HTML, CSS, and vanilla JavaScript, so it can be hosted directly on GitHub Pages.

## Local preview

Open `index.html` in a browser, or serve the folder with any static server. No build step or dependency install is required.

## Add PDF links

All course content lives in `data/courses.json`. Find a topic object and replace its empty `pdf` value:

```json
"pdf": "assets/lem-1-1-principles-of-ethics.pdf"
```

Relative links and full URLs are both supported. The topic button automatically changes from `PDF coming soon` to `Notes PDF`.

## Add a third course

Add another object to the `courses` array in `data/courses.json`. Give it a unique `id`, `code`, `shortCode`, `title`, `description`, `accent`, and a `sections` array. Each section needs a `title` and `topics`; each topic needs `code`, `title`, `subtopics`, `focus`, and `pdf`. Add a matching resource entry in `data/resources.json` if needed. No JavaScript changes are required.

## Deploy on GitHub Pages

1. Push this folder to a GitHub repository.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select the branch and `/ (root)` folder.
4. Save. GitHub Pages will publish `index.html`; hash routes work without server configuration.
