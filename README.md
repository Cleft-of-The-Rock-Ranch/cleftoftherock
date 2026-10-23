# Cleft of the Rock Ranch

Plain HTML/CSS/JS site for Cleft of the Rock Ranch (Cloudflare Pages, deployed from the `Cleft-of-The-Rock-Ranch/cleftoftherock` GitHub repo). There is no build step: pushing to `main` publishes the files as they are.

## Preview locally

```bash
py serve.py          # http://localhost:8081
```

`serve.py` mimics Cloudflare Pages (extensionless URLs such as `/about` serve `about.html`, `/about.html` redirects to `/about`, unmatched paths return `404.html` with a 404 status). A plain `python -m http.server` does not, and makes internal links look broken.

## Layout

- `index.html`, `about.html`, `donate.html`, `404.html` - the pages. Link between them without the `.html` extension.
- `style.css` - the only stylesheet.
- `gallery.js` - the photo gallery on the home page.
- `images/` - photos used by the pages; `assets/` - icons and manifest images.
- `sitemap.xml`, `robots.txt` - edit `sitemap.xml` by hand when a page is added.
