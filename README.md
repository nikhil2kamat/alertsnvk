# Alerts Portal (GitHub Pages)

Single‑page app to view and track alerts. It loads from `alerts.json` (in this repo) and supports search, filters, manual add, import/export.

## Deploy (2 minutes)
1. Create a public GitHub repo (or use your existing `DailyAlerts_Nikhil`).
2. Upload these files to the repo root: `index.html`, `alerts.json`, `.nojekyll` (optional).
3. Settings → Pages → Source: Deploy from a branch → Branch: `main` → Folder: `/ (root)` → Save.
4. Open `https://<username>.github.io/<repo>/`

> If you get “Sync failed: HTTP 404”, ensure `alerts.json` exists at the **same level** as `index.html` and the Pages branch is correct.

## JSON format
```json
[
  {
    "id": "unique-id-123",
    "category": "Company News (8 AM)",
    "companyTopic": "PI Industries",
    "title": "Headline",
    "summary": "1–3 lines",
    "link": "https://example.com",
    "sentAt": "2025-08-24T12:00:00+05:30"
  }
]
```

## Optional: Use a different feed URL
Append `?feed=https://raw.githubusercontent.com/<user>/<repo>/main/alerts.json` to the page URL.
