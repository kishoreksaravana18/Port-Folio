# Kishore S · Portfolio

Static portfolio site for Kishore S, Senior Manager of E-commerce and Marketing Technology.
Plain HTML and CSS, no build step and no dependencies.

## Files

| Path | What it is |
|---|---|
| `index.html` | Home page: summary, career impact, experience, expertise, design registration, résumé, contact |
| `command-center.html` | Command Center case study (also served at `/command-center`) |
| `assets/` | Screenshots, the two walkthrough videos, poster frames and the résumé PDF |
| `favicon.svg` | Browser tab icon |
| `404.html` | Not-found page |
| `netlify.toml` | Netlify settings: publish folder, security headers, asset caching, pretty URL |

Light and dark mode follow the visitor's system setting.

## Preview locally

```bash
python3 -m http.server 8000
# open http://localhost:8000
```

## Push to GitHub

```bash
cd kishore-portfolio
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

## Publish on Netlify

1. In Netlify, choose **Add new site → Import an existing project → GitHub** and pick the repository.
2. Leave **Build command** empty and set **Publish directory** to `.` (the `netlify.toml` already sets this).
3. Deploy. Every push to `main` redeploys automatically.

Alternative without GitHub: drag the `kishore-portfolio` folder onto **app.netlify.com/drop**.

## After the first deploy

- **Social preview:** link previews (LinkedIn, Slack) need an absolute image URL. Replace
  `content="assets/og-image.jpg"` in both HTML files with `https://<your-site>.netlify.app/assets/og-image.jpg`.
- **Custom domain:** Netlify → Domain management → Add a domain.
- **Résumé link:** point the "Portfolio" link in the résumé PDF at the live URL.

## Updating content

Text lives directly in `index.html` and `command-center.html`. Search for the words you want to change,
edit, commit and push. Replace a file in `assets/` with one of the same name to update an image or video.
