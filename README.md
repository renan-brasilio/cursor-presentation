# Cursor AI — Developer Tools Presentation

A self-contained HTML slide deck for presenting **Cursor**, **Agent Skills**, **MCP servers**, **subagents**, and **slash commands** to engineering teams. No build step, no dependencies—open the file in a browser or host it on GitHub Pages.

## Contents

| Path | Description |
|------|-------------|
| `cursor-ai-guide.html` | Main presentation (keyboard navigation, slide tray, deep links) |
| `index.html` | Entry point for GitHub Pages (redirects to the deck) |
| `resources/` | Logos and diagram images referenced by the deck |

## View locally

**Option A — open directly**

```bash
open cursor-ai-guide.html
```

On macOS you can also double-click the file. Relative paths to `resources/` work when the file is opened from the repo folder.

**Option B — local HTTP server (recommended for sharing on your LAN)**

```bash
cd /path/to/cursor-presentation
python3 -m http.server 8080
```

Then open [http://localhost:8080/cursor-ai-guide.html](http://localhost:8080/cursor-ai-guide.html) (or [http://localhost:8080/](http://localhost:8080/) if using `index.html`).

## Presenting

| Action | Keys / control |
|--------|----------------|
| Next slide | `→`, `↓`, `Space`, or **Next** |
| Previous slide | `←`, `↑`, or **Prev** |
| First / last slide | `Home` / `End` |
| Slide tray | `T` or tray toggle |
| Deep link | `#slide-4` (share a specific slide) |
| Swipe | Touch devices |

## Publish on GitHub Pages

GitHub Pages serves static files from your repo over HTTPS at:

`https://<github-username>.github.io/cursor-presentation/`

### One-time setup

1. Push this repository to GitHub (if it is not there already).
2. On GitHub: **Repository → Settings → Pages**.
3. Under **Build and deployment**:
   - **Source:** Deploy from a branch
   - **Branch:** `main` (or your default branch) and **`/ (root)`**
4. Click **Save**. After a minute or two, GitHub shows the live URL.

The repo includes `index.html`, which sends visitors to `cursor-ai-guide.html`, so the deck opens at the site root without typing the filename.

### Direct link to the deck

If you prefer not to use `index.html`, the deck is always available at:

`https://<github-username>.github.io/cursor-presentation/cursor-ai-guide.html`

### Custom domain (optional)

In the same **Pages** settings, add your domain under **Custom domain** and configure DNS with your provider. GitHub’s docs: [Configuring a custom domain for your GitHub Pages site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site).

### Troubleshooting

| Issue | Fix |
|-------|-----|
| 404 after enabling Pages | Wait 2–5 minutes; confirm the default branch has `index.html` or `cursor-ai-guide.html` at the root you selected (`/`). |
| Images missing on Pages | Ensure `resources/` is committed and pushed; paths in the HTML are relative (`resources/...`). |
| Old version still showing | Hard-refresh (`Cmd+Shift+R`) or open in a private window; Pages can cache briefly. |
| Works locally but not on Pages | Use **Deploy from branch → root**, not `/docs`, unless you move files into `docs/`. |

## Editing

Edit `cursor-ai-guide.html` in any editor. Styles and scripts are inline; assets live under `resources/`. After changes, refresh the browser (or push to GitHub for Pages to update).

## License

Internal / presentation use—adjust as needed for your organization.
