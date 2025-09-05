# SLA-RETURNS (GitHub Pages)

This repo serves the **Returns SLA Tracker** via GitHub Pages and connects to your Google Apps Script backend.

## Two ways to use it

### Option A — Embed (recommended)
Commit **index.html** (the embed version). Visitors to
`https://ohpolly-ops.github.io/SLA-RETURNS/` see the Apps Script app inside a full-screen iframe.  
Pros: keeps the GitHub URL, simple, allows presence/refresh features.  
If you redeploy Apps Script, no change is needed here. Cache-bust by adding `?v=9` if you want.

### Option B — Redirect
Alternatively, commit **index-redirect.html** as **index.html**. This hard-redirects the page to:
```
https://script.google.com/a/macros/ohpolly.com/s/AKfycbz4KxABa4GRcpPbtZ9n2p9EWNNeSdksFgA7o4ZYrCInCBE5wwTYwmmzRjaOQ6bLQ4L2/exec
```
Useful if you prefer not to embed.

## Steps
1. Choose either **index.html** (embed) or **index-redirect.html** (redirect). If using redirect, rename it to **index.html**.
2. Commit to `main` and ensure GitHub Pages is enabled for the repo (Settings → Pages → Source: Deploy from a branch → `main` / `/root`).
3. Open: https://ohpolly-ops.github.io/SLA-RETURNS/?v=now

## Updating the Apps Script URL
If you create a brand-new deployment with a different web app URL, edit the URL in the HTML file(s):
```
https://script.google.com/a/macros/ohpolly.com/s/AKfycbz4KxABa4GRcpPbtZ9n2p9EWNNeSdksFgA7o4ZYrCInCBE5wwTYwmmzRjaOQ6bLQ4L2/exec
```

## Access & Auth
If your Apps Script deployment access is **"Anyone in ohpolly.com"**, users must be signed into the Workspace account in their browser (even inside the iframe). To allow external viewers, change access to **"Anyone with the link"** (it still runs as you).

— Generated 2025-09-05 14:24:55
