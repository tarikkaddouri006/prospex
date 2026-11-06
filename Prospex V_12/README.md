# Prospex (v12)

One self-contained page: fonts, data and art are all inside `index.html`. No build step, no server code, no external calls.

| File | What it does |
|---|---|
| `index.html` | The whole game |
| `favicon.svg` | Crown icon for the browser tab |
| `netlify.toml` | Tells Netlify to publish this folder as-is, and keeps it out of search engines |
| `robots.txt` | Asks search engines not to index the site |
| `.gitignore` | Keeps Mac and Netlify clutter out of the repo |

## 1. GitHub
1. Create a new **private** repository (e.g. `prospex`). Don't add a README.
2. Upload everything in this folder: **Add file → Upload files**, drag in all the files, then commit. `.gitignore` is hidden on a Mac: press Cmd+Shift+. in Finder to see it, or skip it.
   Or from a terminal inside this folder:
   ```
   git init && git add . && git commit -m "Prospex v12"
   git branch -M main
   git remote add origin https://github.com/<you>/prospex.git
   git push -u origin main
   ```

## 2. Netlify
1. **Add new site → Import an existing project → GitHub**, then pick the repo.
2. Leave **Build command** empty. Set **Publish directory** to `.` (it's also in `netlify.toml`).
3. Click **Deploy**. Every push to `main` redeploys.

No GitHub? Use **Add new site → Deploy manually** and drag this folder in.

## Notes
- Each visit downloads the full page (about 21 MB, or about 14 MB compressed), which counts toward Netlify bandwidth.
- Progress (credit, cards, posts) lives in each visitor's own browser. Clearing site data resets it.
- To ship a new version, replace `index.html` and push.
- The page shows likenesses of real recruits, most of them minors. Keep the repo private, and get image-rights and NIL consent before sharing it publicly.
