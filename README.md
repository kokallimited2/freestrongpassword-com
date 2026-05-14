# Free Strong Password

> **Beginner Password Wizard** — 3-step guided password creation in plain English.
> Operated by Kokal Operations Ltd, United Kingdom.

## Deployment

```
freestrongpassword.com → CNAME → kokallimited.github.io/...
```

Push to `main` → GitHub Pages deploys automatically.

---

## ⚠️ SEO Architecture — Individual Blog Post URLs

Each guide is a standalone HTML file with its own indexable URL:

```
/blog/what-makes-a-password-strong-simple-guide.html
/blog/why-you-need-different-password-every-site.html
/blog/best-free-password-managers-beginners-2026.html
/blog/how-to-set-up-two-factor-authentication-simple.html
/blog/what-to-do-if-you-think-youve-been-hacked.html
/blog/common-password-mistakes-to-avoid.html
```

`post.json` contains **metadata only** — no full content.
`blog.html` reads post.json and renders cards that **link to** `/blog/slug.html` directly.
There is **no modal or JavaScript content injection** for blog posts.

---

## File Inventory

| File | Purpose |
|------|---------|
| `index.html` | Homepage + Beginner Password Wizard (SOP-07) |
| `blog.html` | Guide index — reads post.json, links to /blog/*.html |
| `/blog/what-makes-a-password-strong-simple-guide.html` | What Makes a Password Strong? A Simple Guide |
| `/blog/why-you-need-different-password-every-site.html` | Why You Need a Different Password for Every Websit |
| `/blog/best-free-password-managers-beginners-2026.html` | The Best Free Password Managers for Beginners (202 |
| `/blog/how-to-set-up-two-factor-authentication-simple.html` | How to Set Up Two-Factor Authentication — Simple S |
| `/blog/what-to-do-if-you-think-youve-been-hacked.html` | What to Do If You Think You've Been Hacked |
| `/blog/common-password-mistakes-to-avoid.html` | 7 Common Password Mistakes (And How to Fix Them) |
| `about.html` | E-E-A-T author page — Person + Organization schema |
| `contact.html` | Contact form |
| `privacy-policy.html` | UK GDPR privacy policy |
| `affiliate-disclosure.html` | FTC + ASA/CAP compliant disclosure |
| `terms.html` | Terms of use — England & Wales |
| `cookie-policy.html` | Cookie table (key: `fsp-ck`) |
| `404.html` | Custom 404 |
| `post.json` | Blog metadata only — url fields point to /blog/*.html |
| `robots.txt` | GPTBot, ClaudeBot, Googlebot all allowed |
| `llms.txt` | AI citation guidance |
| `sitemap.xml` | All URLs including 6 /blog/ post URLs |

---

## Brand Identity

| Element | Value |
|---------|-------|
| Primary colour | `#10b981` (Emerald) |
| Accent | `#f97316` (Orange) |
| Background | `#fdf8f0` (Warm Cream) |
| Body font | Nunito |
| Border radius | `18px` (rounded, friendly) |
| Cookie key | `fsp-ck` (localStorage) |
| Audience | Non-technical beginners |
| Unique tool | Beginner Password Wizard (3-step) |

---

## SOP Checklist

- [x] 17 core files + 6 individual blog posts
- [x] Each `/blog/*.html` has canonical, og:image, TechArticle, BreadcrumbList, FAQPage schema
- [x] `post.json` metadata-only with `/blog/` url fields, 1 featured post
- [x] `blog.html` links to `/blog/slug.html` — no modal, no `openP()`
- [x] `sitemap.xml` includes all 6 `/blog/` post URLs + about.html
- [x] `about.html` with Person + Organization schema, author bio (Emma Watts)
- [x] `robots.txt` — Googlebot, GPTBot, ClaudeBot, PerplexityBot all allowed
- [x] All affiliate links `rel="nofollow sponsored"`
- [x] Cookie key `fsp-ck` in localStorage
- [x] GitHub Actions: `update-sitemap.yml` + `validate-html.yml`
