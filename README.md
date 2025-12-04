# Personal Portfolio (Plain HTML/CSS/JS)

A minimal, responsive, accessible personal portfolio template built with plain HTML, CSS, and vanilla JavaScript. Ready to copy into a Git repository and deploy to GitHub Pages.

## What you get
- Multi-page site: `index.html`, `about.html`, `projects.html`, `contact.html`
- Styling: `css/styles.css` (light/dark mode with `localStorage` persistence)
- JavaScript: `js/main.js` (theme, mobile nav focus trap, reveal animations, projects rendering, contact validation)
- Assets: `assets/` (placeholders for `profile.jpg`, `project1.jpg`, `project2.jpg`, `project3.jpg`, `resume.pdf`)
- Accessibility features: skip link, keyboard focus, ARIA attributes, prefers-reduced-motion support.

## Files (copy into your repo)
- `index.html`
- `about.html`
- `projects.html`
- `contact.html`
- `css/styles.css`
- `js/main.js`
- `assets/profile.jpg` (placeholder)
- `assets/project1.jpg`, `assets/project2.jpg`, `assets/project3.jpg` (placeholders)
- `assets/resume.pdf` (optional)

## Replace placeholders
Search for `<!-- REPLACE:` comments and plain `EMAIL@EXAMPLE.COM`, `USERNAME`, and `NAME` strings:
- `NAME` — replace with your display name.
- `EMAIL@EXAMPLE.COM` — replace with your contact email.
- `USERNAME` — replace with your GitHub / LinkedIn username in links.
- Replace `assets/profile.jpg` and thumbnail images with your real images.
- Replace `assets/resume.pdf` with your resume file (optional).

## Preview locally
You can preview the site locally using a simple static server.

If you have Python 3:
```powershell
# From the project root
python -m http.server 8000
# Then open http://localhost:8000 in your browser
```

Or use VS Code Live Server extension for a quick preview.

## Deploy to GitHub Pages
Option A — Simple (recommended):
1. Create a new GitHub repository and push your files to the `main` branch.
2. In the repository settings, enable "Pages" and set the source to the `main` branch (root).
3. Your site will be published at `https://<username>.github.io/<repo-name>/` (or `https://<username>.github.io/` for a repo named `<username>.github.io`).

Option B — GitHub Actions (example)
- Create `.github/workflows/gh-pages.yml` and use a deploy action (example uses `peaceiris/actions-gh-pages`).
- This is optional; enabling Pages via settings is sufficient for most static sites.

Example workflow (optional):
```yaml
name: Deploy to GitHub Pages
on:
  push:
    branches:
      - main
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./   # root of repo
```

## Example commit messages
- "feat: add basic multi-page layout and styles"
- "feat: implement dark/light mode and localStorage persistence"
- "feat: add projects rendering and contact form validation"
- "chore: add README and placeholder assets"

## Notes & Next steps
- The contact form uses `mailto:` fallback — there is no backend.
- The projects are rendered from the `projects` array in `js/main.js`. Edit that array to add or change projects.
- Accessibility: run audits (Lighthouse, axe) and update content for best results.
- If you'd like, I can:
  - Wire up a simple static site CI deploy workflow.
  - Convert this to a single-page app with client-side routing.
  - Add more sample content or visual polish (animations, icons).

Enjoy — and replace placeholders before publishing!
