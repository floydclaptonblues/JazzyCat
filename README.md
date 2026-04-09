# BMC JazzyCat GitHub Pages Repo

This repository is a static GitHub Pages bundle for the Balcony Music Club JazzyCat page.

## Files

- `index.html` — quick landing page that links into JazzyCat
- `jazzycat.html` — dedicated JazzyCat page
- `data/jazzycat-knowledge.json` — venue facts, FAQs, contacts, recurring programming
- `data/jazzycat-current-schedule.json` — current public schedule snapshot
- `data/jazzycat-artists.json` — artist metadata, genres, and links when verified
- `.nojekyll` — disables Jekyll processing so Pages serves the site as plain static files

## Quick publish steps

1. Create a new GitHub repository.
2. Upload every file from this folder to the repository root.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose:
   - **Source:** Deploy from a branch
   - **Branch:** `main`
   - **Folder:** `/ (root)`
5. Save.
6. Wait for GitHub Pages to publish the site.

Your site URL will be one of these patterns:

- `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/`
- `https://YOUR-CUSTOM-DOMAIN/` if you later connect a custom domain

## Updating content

### Club facts / FAQs
Edit:

- `data/jazzycat-knowledge.json`

### Current schedule
Edit:

- `data/jazzycat-current-schedule.json`

### Artist genres and links
Edit:

- `data/jazzycat-artists.json`

Then commit and push changes. GitHub Pages will republish the updated files.

## How JazzyCat works

The page loads all three JSON files from the local `data/` folder. It answers questions in this order:

1. current schedule
2. artist metadata
3. venue facts / FAQs

If the answer is not present in the JSON, JazzyCat says so rather than inventing details.

## Notes

- This is a static site. There is no live backend in this repo.
- If you later build a separate schedule manager, that tool should update the JSON files rather than rewriting the HTML.
- For project pages on GitHub Pages, the current file paths in `jazzycat.html` are already set up correctly.
