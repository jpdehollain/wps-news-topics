# Waverley PS Stage 1 News Topics

A simple web app for parents to check the weekly news topic for Stage 1 students at Waverley Public School. Opens in any browser, works offline once loaded.

🔗 **Live app:** https://YOUR-USERNAME.github.io/waverley-news-topics/

## Repo structure

```
waverley-news-topics/
├── index.html      # The app (don't need to edit this)
├── topics.json     # Topic data — update this each term
├── topics.pdf      # The letter from school — keep for reference
└── README.md       # This file
```

## Updating each term

1. **Upload the new PDF** — replace `topics.pdf` with the new term's letter
2. **Edit `topics.json`** — update the following fields:
   - `term` — e.g. `"Term 3, 2026"`
   - `weeks` — replace the array with the new term's weeks

### topics.json week format

```json
{
  "label": "Week 2",
  "weekStart": "2026-07-20",
  "topic": "Your topic text here.",
  "free": false
}
```

- `weekStart` — the **Monday** of that school week, in `YYYY-MM-DD` format
- `free` — set to `true` for free choice weeks, `false` for set topics

3. **Commit and push** — GitHub Pages will update automatically within a minute or two.

## Setting up GitHub Pages (first time only)

1. Go to your repo on GitHub
2. Settings → Pages
3. Source: **Deploy from a branch**
4. Branch: `main` / `(root)`
5. Save — your site will be live at `https://YOUR-USERNAME.github.io/waverley-news-topics/`

## Sharing with other parents

Share the GitHub Pages URL. Parents can:
- Bookmark it in their browser
- On Android (Chrome): Menu → Add to Home Screen
- On iPhone (Safari): Share → Add to Home Screen
