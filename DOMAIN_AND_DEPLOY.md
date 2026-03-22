# Domains & deploy (keep this updated)

## Your portfolio URLs

| Domain | Notes |
|--------|--------|
| **`iamjust.site`** | **Preferred / canonical** — use this in bios, resume, LinkedIn, posts |
| `buildaiwithkartikey.site` | Extra domain — same Netlify site; can redirect to `iamjust.site` in Netlify (optional) |

Both domains should point to the **same** Netlify project so one Git push updates both.

## Netlify: both domains on one site

1. Netlify → your site → **Domain management** → **Add domain** for each domain you own.
2. DNS at registrar as Netlify shows (often **CNAME** `www` → `your-site.netlify.app`, and **A** or ALIAS for apex `@`).
3. Optional: set **Primary domain** to **`iamjust.site`** so Netlify treats it as the main URL.

## After you change domains — nothing extra in code

This repo is static (`index.html`). Canonical + Open Graph in **`index.html`** use **`https://iamjust.site/`** as the preferred URL.  
Use **`iamjust.site`** everywhere you share the portfolio.

## YouTube Unlisted — step by step (then paste link in `index.html`)

1. Go to [YouTube Studio](https://studio.youtube.com) → **Create** → **Upload video**
2. Select your `.mp4` file
3. **Title** e.g. `Kartikey Sharma — Intro | AI Agent Developer`
4. **Visibility** → **Unlisted** (link se koi open kar sakta hai; search me nahi dikhega)
5. Upload finish → **Copy link** (looks like `https://www.youtube.com/watch?v=xxxxxxxxxxx` or `https://youtu.be/xxxxxxxxxxx`)
6. In this project, open `index.html` → search for `YOUR_VIDEO_ID` in the **About** section → replace with your real video ID (the part after `v=`)

Example:

```html
href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

(Use your real ID, not this example.)

## Umami analytics

If you use Umami, add **both** domains in the Umami website settings (or one domain — depending on Umami UI) so stats stay clean.

## SEO (meta + Open Graph + JSON-LD)

`index.html` includes:

- **`<meta name="description">`** — search snippet text (Google may still rewrite it).
- **`<link rel="canonical">`** — primary URL is **`https://iamjust.site/`**
- **Open Graph + Twitter** — better previews when the portfolio link is shared (LinkedIn, WhatsApp, etc.).
- **`og:image`** — `https://iamjust.site/images/personalAI.png` (change in `<head>` if you add a dedicated `og-image.jpg` later).

### Where you can **see results** (kahan dikhega)

| What | Where to look |
|------|----------------|
| **Meta tags live** | Browser → open `https://iamjust.site/` → right‑click → **View page source** → search `canonical`, `og:`, `description` |
| **Google indexing / clicks / queries** | [Google Search Console](https://search.google.com/search-console) → add property **`https://iamjust.site`** (and optionally `buildaiwithkartikey.site`) → **Performance** + **Pages** |
| **Rich results / structured data** | [Google Rich Results Test](https://search.google.com/test/rich-results) — paste `https://iamjust.site/` |
| **Link preview (WhatsApp / LinkedIn / FB)** | [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) — paste URL → **Scrape again** after deploy |
| **LinkedIn preview** | [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/) — paste `https://iamjust.site/` |
| **Umami (visitors)** | Your Umami dashboard (site you added) |

Add **both** domains in Search Console if both stay public; canonical tells Google **`iamjust.site`** is preferred.

Optional: Search Console → **URL inspection** → `https://iamjust.site/` → **Request indexing** after big updates.
