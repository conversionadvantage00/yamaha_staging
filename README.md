# Knysna Yamaha — GitHub Pages

This repository contains a self-contained, static build of the Knysna Yamaha website.

## Site file

The deployable page is [`docs/index.html`](docs/index.html). It includes the site styling, JavaScript, product imagery, Yamaha engine imagery, and animation library directly in one HTML file. No build step or asset directory is required when the page is deployed.

The contact, map, WhatsApp, Instagram, and Facebook links intentionally open their respective external services. The enquiry form opens the visitor's default email app because GitHub Pages does not provide server-side form handling.

## Publish with GitHub Pages

1. Create a GitHub repository and add this project to it.
2. Push the project to the repository's default branch (normally `main`).
3. On GitHub, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the `main` branch and the `/docs` folder, then click **Save**.
6. GitHub will show the public site URL after deployment completes.

The resulting address will normally be:

```text
https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/
```

## Preview locally

You can open `docs/index.html` directly in a browser. To preview it through a local web server instead, run:

```bash
python3 -m http.server 8000 --directory docs
```

Then visit <http://localhost:8000>.

## Editing content

The page includes an **Edit mode** toolbar. Text and image changes are stored in the browser, and **Download edited HTML** exports a new self-contained file. Rename the downloaded file to `index.html`, replace `docs/index.html`, and push the change to publish it.

## Rebuilding from the editable source

The source version is in `knysna-yamaha-v10-editable/`. The helper script `build-standalone.mjs` inlines its local files and downloads the six inventory images currently referenced by the source before creating `docs/index.html`.

The existing generated `docs/index.html` is the canonical GitHub Pages artifact. Rebuilding requires Node.js and an internet connection:

```bash
node build-standalone.mjs
```
