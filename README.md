# MPT Study Portal

A static, mobile-first course portal for Master of Physiotherapy students. It uses plain HTML, CSS, and vanilla JavaScript, so it can be hosted directly on GitHub Pages.

## Local preview

Open `index.html` in a browser, or serve the folder with any static server. No build step or dependency install is required.

## Course data

The portal loads each course from its own JSON file in `pack/data`. The two entries in `js/app.js` are the only course registry; adding a third course requires a new JSON file and one registry entry. Course syllabus links use the matching files in `pack/assets/syllabus`.

Topic PDF links can be added by setting a topic's `pdf` value in the course JSON:

```json
"pdf": "assets/lem-1-1-principles-of-ethics.pdf"
```

Relative links and full URLs are both supported. The topic button automatically changes from `PDF coming soon` to `Notes PDF`.

## Deploy on GitHub Pages

1. Push this folder to a GitHub repository.
2. Open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select the branch and `/ (root)` folder.
4. Save. GitHub Pages will publish `index.html`; hash routes work without server configuration.
