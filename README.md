# CrossFit Jefferson — website

A fully responsive, modern static site for CrossFit Jefferson in Jefferson, GA. No build step, no framework, no dependencies.

## Files

```
site/
├── index.html              Home
├── programs.html           CrossFit, Hyrox, Weightlifting, PT, Nutrition, Teens
├── coaches.html            Story + coach roster (placeholders — drop in real bios)
├── schedule.html           Weekly class grid (sample times — TBD)
├── pricing.html            Membership tiers + add-ons (placeholder $$ — TBD)
├── get-started.html        Free intro form (Formspree-ready)
├── contact.html            Map + hours + general contact form
├── blog.html               Blog index stub (placeholder posts)
└── assets/
    ├── css/styles.css      Single design system, mobile-first
    ├── js/main.js          Mobile nav, sticky header, reveal-on-scroll
    └── img/                Drop hero photos / coach photos here
```

## Preview locally

Any static file server works:

```bash
# Python
cd site && python -m http.server 8765

# Node
npx serve site

# Or just open index.html in a browser
```

## Deploy

It's all static HTML — drag-and-drop the `site/` folder to any host:

- **Netlify** — drag the folder onto netlify.app/drop. Free.
- **Cloudflare Pages** — connect a GitHub repo or upload directly. Free.
- **Vercel** — `vercel deploy` from inside the folder. Free.
- **GitHub Pages** — push to a repo, enable Pages.
- **Existing host** — upload via FTP/SFTP.

## TBD content (drop in when ready)

Search the codebase for `TBD` to find every placeholder. The big ones:

- **Hero photos** — currently a CSS gradient. Replace with real gym photos.
- **Coach bios** — `coaches.html` has 3 placeholder cards.
- **Schedule times** — `schedule.html` has sample slots.
- **Pricing** — `pricing.html` has placeholder amounts.
- **Phone & email** — `contact.html` shows `[Phone TBD]` / `[Email TBD]`.
- **Form endpoint** — search for `YOUR_FORM_ID` in `get-started.html`, `contact.html`, `blog.html`. Replace with your Formspree (or Netlify Forms / other) endpoint.

## Form setup

Three forms ship: Free Intro, Contact, and Newsletter. They're wired for Formspree. Replace `YOUR_FORM_ID` in:

- `get-started.html`
- `contact.html`
- `blog.html` (newsletter)

Or switch to Netlify Forms by adding `data-netlify="true"` and `name="..."` to each `<form>`.

## Brand

- **Colors** — defined as CSS custom properties at the top of `styles.css` (search `:root`). Change `--brand` once and it propagates everywhere.
- **Typography** — Bebas Neue (display) + Inter (body), both from Google Fonts.
- **Logo** — currently a CSS-only "K" mark. Replace with an `<img>` if a real logo exists.

## What this fixes vs. the old site

- ✅ Fully responsive at every width (mobile / tablet / desktop)
- ✅ Mobile nav (hamburger → full-screen panel)
- ✅ Floating Free Intro CTA on mobile
- ✅ Real schedule grid (vs. linking out)
- ✅ Modern card-based pricing with featured tier
- ✅ Get Started form with goal segmentation (better lead data)
- ✅ Map embed on Contact
- ✅ Blog with featured post + category filtering
- ✅ All forms have honeypot anti-spam
- ✅ Schema.org structured data on home (HealthClub)
- ✅ No build step, no JS framework, ~1 file CSS, ~1 file JS
