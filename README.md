# Kintaba — website deploy package

A standalone marketing site (3 pages) for Kintaba. Built to deploy at **kintaba.app**.

- `index.html` → `/` (landing)
- `privacy.html` → `/privacy` (interim draft — see note below)
- `contact.html` → `/contact` (contact form, wired to Web3Forms)

## Before you deploy — 2 quick things

1. **Contact form key.** Go to **web3forms.com**, enter **info@kintaba.app**, and get a free Access Key (they email it to you). Open `contact.html`, find `YOUR_WEB3FORMS_ACCESS_KEY`, and paste your key in its place. Submissions will then be emailed to info@kintaba.app. (A fallback `mailto:info@kintaba.app` link is already on the page.)
2. *(optional)* Swap the **hero image** / **font** if you finalise them — see "Swapping later".

## Deploy to Vercel (recommended)

- **Drag & drop:** vercel.com → Add New → Project → drag this whole folder in. Done.
- **Git:** push this folder to a GitHub repo and import it in Vercel.

Then connect the domain: **Vercel → Project → Settings → Domains → add `kintaba.app`** and follow the DNS steps. `vercel.json` (included) turns on clean URLs, so `/privacy` and `/contact` work without `.html`.

(Netlify works the same way — drag the folder into app.netlify.com.)

## Domain setup (the Option B you chose)

- **This site** lives at **kintaba.app**.
- **Your app** stays exactly where it is: **www.kintaba.app** — nothing to move.
- The **"Get started — it's free"** and **"Open app"** buttons already link to `https://www.kintaba.app` (the app). No change needed.

## What's inside

| File | Purpose |
|---|---|
| `index.html`, `privacy.html`, `contact.html` | the three pages |
| `hero.jpg` | hero photo |
| `favicon-16.png`, `favicon-32.png`, `apple-touch-icon.png` | browser/app icons |
| `og-image.png` | social share card (shows when the link is shared) |
| `vercel.json` | clean-URL config |

## Privacy page — important

`/privacy` is an **interim draft**. Keep its draft banner until the real policy is written, and **have a lawyer review it before relying on it** (Kintaba records data about the people users send to, and you're in the EU → GDPR applies). The page lists exactly what to confirm before publishing.

## Swapping later

- **Hero image:** replace `hero.jpg` with the final (landscape, ~1600–2000px wide). The CSS already uses `object-fit: cover` so it won't distort.
- **Font:** currently **Hanken Grotesk** via Google Fonts. To change it, update the `<link>` and the `font-family` in each page's `<style>`.
- **Icons / share card:** regenerate from the logo if the brand changes.

## Using Claude Code

Open this folder in Claude Code and ask it to deploy to Vercel and connect `kintaba.app`. It can handle the Git/Vercel steps and drop in your Web3Forms key for you.
