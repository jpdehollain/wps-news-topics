# Waverley PS News Topics

A simple web app for parents to check the weekly news topic for students at Waverley Public School. Opens in any browser, works offline once loaded.

🔗 **Live app:** https://YOUR-USERNAME.github.io/waverley-news-topics/

## Repo structure

```
waverley-news-topics/
├── index.html       # The app (no need to edit this)
├── kindy.json       # Kindy topic data — update each term
├── stage1.json      # Stage 1 topic data — update each term
├── pdfs/            # Optional: store the original PDF letters here
└── README.md        # This file
```

## Updating each term

1. **Edit the relevant JSON file** (e.g. `stage1.json`) with the new term's data
2. **Optionally upload the new PDF** to the `pdfs/` folder for reference
3. **Commit and push** — GitHub Pages updates automatically within a minute

### JSON file format

```json
{
  "school": "Waverley Public School",
  "stage": "Stage 1",
  "term": "Term 3, 2026",
  "weeks": [
    {
      "label": "Week 2",
      "weekStart": "2026-07-20",
      "topic": "Your topic text here.",
      "free": false
    },
    {
      "label": "Week 3",
      "weekStart": "2026-07-27",
      "topic": "Free choice",
      "free": true
    }
  ]
}
```

- `weekStart` — the **Monday** of that school week, in `YYYY-MM-DD` format
- `free` — `true` for free choice weeks, `false` for set topics
- To show a "not yet uploaded" message, leave `weeks` as an empty array `[]`

## Adding more stages

To add Stage 2 or Stage 3 in the future:
1. Create `stage2.json` (copy the format from `stage1.json`)
2. Add a tab in `index.html`:
   ```html
   <div class="tab" data-file="stage2.json" onclick="switchTab(this)">Stage 2</div>
   ```

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

## Licence

MIT — free to use and adapt.
