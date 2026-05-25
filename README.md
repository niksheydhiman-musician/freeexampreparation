# Free Exam Preparation

Static GitHub Pages deployment for **freeexampreparation.com**.

## Deployment structure

```text
.
├── index.html
├── competitive-hub.html
├── exams.html
├── ssc-mock-demo.html
├── README.md
└── assets/
```

## What is wired already

- `index.html` sends users to the competitive hub and school boards dashboard.
- `competitive-hub.html` uses `ssc-mock-demo.html` as the live mock-test template destination.
- Download buttons use the Cloudflare R2 placeholder format:
  `https://YOUR_CLOUDFLARE_R2_PUBLIC_URL/placeholder-filename.pdf`
- Heavy downloads are expected to live in Cloudflare R2, not in this repository.

## Copilot-friendly authoring rules

- Keep file names lowercase and use hyphens for multi-word pages.
- Keep the Tailwind Play CDN script inside `<head>` on every HTML page.
- Reuse semantic boundary comments such as `HEADER`, `PAGE HERO`, `MAIN CONTENT`, and `FOOTER` when creating new pages.
- Use local `assets/` only for lightweight branding assets such as logos and favicons.

## Local preview

No build step is required. From the repository root you can preview locally with:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000/`.
