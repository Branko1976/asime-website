# ASIME website

Static bilingual site, no build step needed to deploy. Works on any static host.

```
index.html      English  →  https://YOUR-DOMAIN/
ja/index.html   Japanese →  https://YOUR-DOMAIN/ja/
styles.css      shared styles (colours match the logo, #E44117)
logo.svg        header logo
favicon.svg     browser-tab icon
```
Deploy the whole folder as-is so `ja/` and the shared files stay together.
The 日本語 / English button in the header switches between the two versions.

## Editing text
Both pages are generated from one script (`build.py`, in the zip next to this folder — run `python3 build.py`) so EN and JA stay in sync.
For a quick fix you can also edit `index.html` or `ja/index.html` directly.

## Deploy (pick one)

### A. Netlify Drop — fastest, no account setup beyond sign-in
1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page. It's live in seconds on a `*.netlify.app` URL.
3. Site settings → Domain management → Add a domain → enter your domain and follow the DNS records it shows.

### B. GitHub + Vercel — best if you want to edit and redeploy
1. Create a GitHub repo (e.g. `asime-site`) and upload everything in this folder, including `ja/`.
2. https://vercel.com/new → Import the repo → Framework preset: **Other** → Deploy.
3. Project → Settings → Domains → add `asime.org` (your domain) and `www.asime.org`.
4. At your domain registrar, add the DNS records Vercel shows. Typically:
   - `A` record, host `@` → `76.76.21.21`
   - `CNAME` record, host `www` → `cname.vercel-dns.com`
5. HTTPS is issued automatically once DNS resolves (minutes to a few hours).

Every later edit: change the files on GitHub → Vercel redeploys automatically.

## Getting the domain
- Register at Cloudflare Registrar, Namecheap, Porkbun, or お名前.com / Xserverドメイン.
- Good candidates: `asime.org`, `asime-edu.org`, `asime.jp` (.jp needs a Japanese address — you have one).
- Budget roughly ¥1,500–4,000/year for .org; .jp is a bit more.

## After launch
- Update the Wix site with a link to the new address (a free Wix plan can't redirect or attach a custom domain).
- Ask MDPI to update the society link on the IME journal pages.
- Optional: add `<link rel="canonical" href="https://YOUR-DOMAIN/">` in the `<head>`.
