# ASIME website — asime.online

Website of the **Academic Society for International Medical Education (ASIME)**, in English and Japanese.
It is a plain static site (HTML + CSS), hosted free on **GitHub Pages** and published with **GitHub Desktop**.

- English: https://asime.online/
- Japanese: https://asime.online/ja/

---

## Files

```
index.html         English page
ja/index.html      Japanese page
styles.css         design and colours, shared by both pages
logo.svg           ASIME logo (header and certificate)
favicon.svg        browser-tab icon
img/               board photos: branko.jpg, itzel.jpg, yuko.jpg
CNAME              created by GitHub, connects the site to asime.online (do not delete)
README.md          this file
```

---

## What is on the site

Both pages have the same sections, in this order:

| Section | Content |
|---|---|
| **Header** | Logo, menu (Membership, Microcredentials, Conferences, Services, Journal), 日本語 / English switch, Join button |
| **Hero** | Society name, short mission, tiles linking to IME, Microcredentials, Conferences and member savings |
| **About** | Mission statement and four focus areas: curriculum internationalization, joint teaching modules, professional development, research and publication |
| **Membership** | Four member benefits and the two membership types (below) |
| **Microcredentials** | Short certified courses, course languages, focus areas, how it works, "Register interest" email button |
| **Conferences** | What to expect, member rate note, "Ask about upcoming events" email button |
| **Services** | Course languages; custom-tailored workshops; student experience tours (in Japan and abroad), each with an email button |
| **Journal** | International Medical Education (IME), the society journal: ISSN 2813-141X, open access, Scopus, first Impact Factor, aims and scope |
| **Board** | Branko Aleksic and Itzel Bustos Villalobos (Co-Presidents), Yuko Aleksic (Treasurer), each with photo and short CV |
| **Contact** | Postal address and a "Send an email" button |
| **Join band / footer** | Final call to join, copyright, link to IME |

### Membership

| Type | Fee | Who | Includes |
|---|---|---|---|
| Regular member | ¥10,000 / year | Medical educators, clinicians, researchers | IME publishing discount, microcredentials, conferences, workshops and tours at member price |
| Discounted member | ¥5,000 / year | Undergraduate and graduate students; members from low-income countries | Same, **except** the IME publishing discount |

PayPal links:
- Regular: https://www.paypal.com/ncp/payment/5SDZDW5649PTL
- Discounted: https://www.paypal.com/ncp/payment/364U2EXZQQU36

Make sure the amounts set in PayPal match the fees shown on the site.

### Services

- **Custom-tailored workshops**: on site or online, half day to multi-day. Topics: faculty development, PBL and case design, scientific writing, assessment/OSCEs/feedback, curriculum internationalization.
- **Student experience tours**
  - *In Japan*: hospital, medical school and community clinic visits, lectures, cultural program for international students.
  - *Abroad*: intensive courses in medical practice taught in a foreign language.
- **Course languages**: English, Japanese, Spanish, Portuguese, Serbian, Croatian, Bosnian.

### Contact details used on the site

- Address: Berushatou Takamine B2-311, 6-12-1 Higashiyama Motomachi, Chikusa-ku, Nagoya, Aichi 464-0804, Japan
- Email (behind the buttons): branko@med.nagoya-u.ac.jp
- Journal link: https://www.mdpi.com/journal/ime

---

## Editing

Open the files in any text editor (TextEdit in plain-text mode, or a free editor such as Visual Studio Code).

- **Text**: edit `index.html` for English and `ja/index.html` for Japanese. Change both so the two versions stay the same.
- **Prices or PayPal links**: search for `¥10,000`, `¥5,000` or `paypal.com` in both pages.
- **Email address**: search for `branko@med.nagoya-u.ac.jp` in both pages.
- **Colours**: the main colours are at the top of `styles.css`.
- **Photos**: put portrait photos (about 600 × 750 px) in `img/`, named exactly `branko.jpg`, `itzel.jpg`, `yuko.jpg`. Until a photo is there, the site shows initials.

---

## Publishing with GitHub Desktop

The site lives in the GitHub repository on account **branko1976** and is served by GitHub Pages.

### Every update

1. In GitHub Desktop, click **Fetch origin**, then **Pull origin** if it appears, so your Mac copy is current.
2. Edit or replace the files in the repository folder (**Repository → Show in Finder**).
   Keep the `CNAME` file.
3. Back in GitHub Desktop, type a short summary (e.g. `Update membership fees`) and click **Commit to main**.
4. Click **Push origin**.
5. Wait about a minute, then reload https://asime.online (use ⌘ Shift R to skip the browser cache).

### First-time setup (already done, for reference)

1. GitHub Desktop: **File → New Repository**, then copy the site files into the folder.
2. **Commit to main**, then **Publish repository** with "Keep this code private" **unticked**.
3. On github.com: repository **Settings → Pages** → Source **Deploy from a branch**, branch **main**, folder **/ (root)** → **Save**.

---

## Custom domain (asime.online)

Registered at **Namecheap**, nameservers **Namecheap BasicDNS**, **DNSSEC off**.

DNS records (Namecheap → Domain List → Manage → Advanced DNS):

| Type | Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | branko1976.github.io |
| TXT | _github-pages-challenge-branko1976 | (verification code from GitHub) |

On github.com: repository **Settings → Pages** → Custom domain `www.asime.online`, **Enforce HTTPS** ticked.

---

## Troubleshooting

- **Changes not showing**: check the commit appears on github.com, wait a minute, then hard-reload (⌘ Shift R).
- **Push rejected**: click **Fetch origin** → **Pull origin**, then **Push origin** again.
- **"DNS check unsuccessful" on GitHub**: check the records above and that DNSSEC is off. Test at https://dns.google/resolve?name=asime.online&type=A — `"Status": 0` with the four 185.199… addresses means DNS is fine.
- **404 page**: make sure `index.html` is at the top level of the repository and the `CNAME` file is still there.
