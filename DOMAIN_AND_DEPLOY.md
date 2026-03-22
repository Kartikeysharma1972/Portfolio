# Domains & deploy (keep this updated)

## Your portfolio URLs

| Domain | Notes |
|--------|--------|
| `buildaiwithkartikey.site` | Primary custom domain (Netlify) |
| `iamjust.site` | Second domain — **add as extra custom domain** on the **same** Netlify site |

Both domains should point to the **same** Netlify project so one Git push updates both.

## Netlify: add `iamjust.site`

1. Netlify → your site → **Domain management** → **Add domain** → `iamjust.site`
2. At your domain registrar, set DNS as Netlify shows (often **CNAME** `www` → `your-site.netlify.app`, and **A** or ALIAS for apex `@`).
3. Wait for DNS + SSL (often 5–60 minutes).

## After you change domains — nothing extra in code

This repo is static (`index.html`). As long as **both domains** hit the same deploy, the site is identical.  
Optional: update any **hardcoded** links if you ever put one domain in bios (LinkedIn, resume).

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
- **`<link rel="canonical">`** — primary URL is **`https://buildaiwithkartikey.site/`** (use this in bios; `iamjust.site` is secondary alias).
- **Open Graph + Twitter** — better previews when the portfolio link is shared (LinkedIn, WhatsApp, etc.).
- **`og:image`** — `https://buildaiwithkartikey.site/images/personalAI.png` (change filename in `<head>` if you add a dedicated `og-image.jpg` later).

Optional: [Google Search Console](https://search.google.com/search-console) → add property `buildaiwithkartikey.site` → verify → **URL inspection** → request indexing for `/`.
