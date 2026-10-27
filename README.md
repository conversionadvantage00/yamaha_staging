# Knysna Yamaha Website

One-page website for Knysna Yamaha (boats, Yamaha outboards and marine service), ready to host on GitHub Pages.

## What's in this repo

| File / folder | What it is |
| --- | --- |
| `index.html` | The entire site: page content, styling, scripts and boat listings |
| `assets/images/` | Every photo used on the site (WebP and JPG) |
| `assets/images/gallery/` | The pop-up gallery photos for each stock boat, one folder per boat |
| `assets/images/configurator/` | The seven finished Odyssey CX 580 colourway renders (PNG) used by the "Build your Odyssey CX 580" section |
| `assets/videos/` | The hero reel: `hero-reel.mp4` for desktop and `hero-reel-mobile.mp4` for phones |
| `README.md` | This file |

The site has no build step. Whatever is in `index.html` and `assets/` is what visitors see. Keep the `assets/` folder next to `index.html`, because the page loads everything by those relative paths.

## Publishing on GitHub Pages

1. Create a new repository on GitHub and upload everything in this folder (`index.html`, `README.md` and the `assets` folder) to the top level of the repository.
2. Open the repository on GitHub, go to **Settings**, then **Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, then click **Save**.
4. After a minute or two the site is live at `https://<your-username>.github.io/<repository-name>/`.

To update the site later, replace the changed files in the repository and commit. Pages redeploys on its own.

## Things to know

- **Fonts** load from Google Fonts, so visitors need an internet connection for the site to use its intended typefaces.
- **Forms**: the enquiry and booking forms open the visitor's email app (a `mailto` link) because the site has no server. To receive enquiries directly, connect a form service and point the forms at it.
- **Configurator quotes** open a WhatsApp chat to 082 457 4026 with the chosen colourway filled in.
- **Photos**: some listing photos were taken from the old Knysna Yamaha site. Confirm the client has the right to reuse them before the site goes public.
- **Size**: the folder is about 36 MB, well inside GitHub's limits (100 MB per file, about 1 GB per repository).
