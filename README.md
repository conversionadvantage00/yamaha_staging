# Knysna Yamaha Website

One-page website for Knysna Yamaha (boats, Yamaha outboards and marine service), hosted on GitHub Pages.

## What's in this repo

| File / folder | What it is |
| --- | --- |
| `index.html` | The entire site: page content, styling and boat listings |
| `images/` | Every photo used on the site (WebP) |
| `README.md` | This file |

The site has no build step. Whatever is in `index.html` and `images/` is what visitors see.

## Publishing changes

1. Upload the changed files to this repo (or commit and push them).
2. GitHub Pages redeploys automatically and the change is live within a minute or two.

GitHub Pages must be set to deploy from the `main` branch, root folder: **Settings → Pages → Build and deployment**.

When uploading through the GitHub website, drag `index.html` and the `images` folder in together, then click **Commit changes**.

## Adding, changing or removing listings

All listings live in three lists inside `index.html`. Use search (Ctrl/Cmd + F) to jump to them:

| Search for | What it controls |
| --- | --- |
| `INVENTORY_NEW` | "New Boats" stock cards |
| `INVENTORY_USED` | "Pre-Owned" stock cards |
| `BRANDS` | Brand sections and their model ranges |

### Stock listing (new or pre-owned)

Each listing is one line:

```js
{id:'fusion15',brand:'Pre-Owned',name:'Fusion 15',price:'R269,000',year:'2017',engine:'50 hp Honda',image:'images/preowned-fusion-15.webp',desc:'Fusion 15 with F50 Honda and galvanised trailer. Garmin, canopy and safety equipment.'},
```

- **Add a listing:** copy an existing line, paste it directly below, then change every field. The `id` must be unique and use lowercase letters and numbers only.
- **Remove a listing:** delete its whole line, then delete its photo from `images/`.
- Keep the comma at the end of each line except the last one in the list.
- If text contains an apostrophe, write it as `\'` (for example `Skipper\'s special`), otherwise the page will break.
- `brand` is `New Boat` for new stock and `Pre-Owned` for used stock.

### Brand model (inside `BRANDS`)

```js
{name:'Odyssey 650',image:'images/odyssey-650.webp',desc:'A spacious 6.55 m platform...',specs:[['LOA','6.55 m'],['Beam','2.58 m'],['Power','200–300 hp'],['Fuel','150 L']]},
```

Each spec is a `['Label','Value']` pair. Four specs per model looks best.

## Images

- Save every photo in the `images/` folder and point to it as `images/your-file.webp`.
- File names are **case sensitive** on GitHub Pages. Use lowercase with hyphens, for example `preowned-regal-225.webp`.
- Recommended sizes: listing photos about 1024 px wide, brand hero images about 1920 px wide.
- Keep each image under roughly 200 KB. Export as WebP (or JPG) rather than PNG. Convert with [squoosh.app](https://squoosh.app), free and in the browser.
- Do **not** paste images into `index.html` as base64 text. That is what made the original file 56 MB and too large for GitHub.

Current file naming:

| Prefix | Used for |
| --- | --- |
| `stock-` | New boat stock listings |
| `preowned-` | Pre-owned stock listings |
| `*-hero` | Large banner image for a brand section |
| `engine-`, `intro-logo` | Homepage animation and intro |

## Limits to keep in mind

- Files uploaded through the GitHub website must be under 25 MB each.
- Keep the whole repo well under 1 GB. Committing large images repeatedly makes it grow.
