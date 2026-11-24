# Ziddi Techies .COM — Complete Brand Management

A standalone static marketing site for the **brand-management division** of Ziddi Techies. It is deliberately separate from `zidditechies.in` (Shopify growth & management division).

## What is in here

| File | Purpose |
| --- | --- |
| `index.html` | Home — proposition, two divisions, problem/solution, services overview, process, CTA |
| `services.html` | All twelve services in four pillars, with deliverables and anchors |
| `approach.html` | Operating model, engagement shapes, FAQ |
| `about.html` | Why the division exists, principles, division comparison |
| `contact.html` | Netlify-powered enquiry form plus direct channels |
| `thanks.html` | Form success page (noindex) |
| `privacy.html`, `terms.html` | Legal pages |
| `404.html`, `robots.txt`, `sitemap.xml` | SEO and error handling |
| `assets/css/styles.css` | Complete visual system (dark, violet/cyan) |
| `assets/js/main.js` | Mobile menu, year, copy-to-clipboard, scroll reveal |
| `favicon.png`, `assets/img/brand-logo.png` | Supplied PNG brand logo |
| `netlify.toml` | Publish directory, security headers, redirects |

No build step, no dependencies, no framework. Plain HTML/CSS/JS.

## Contact details used on the site

- Email: **support@zidditechies.com** (IONOS business mailbox)
- WhatsApp / new business: **+91 85678 75871**
- Client operations: **+91 98884 58818**
- Sister division: **https://zidditechies.in**

## Current deployment

- Source repository: **https://github.com/sukh8397/zidditechies-com**
- Netlify project: **https://app.netlify.com/projects/luxury-pastelito-00698e**
- Netlify site: **https://luxury-pastelito-00698e.netlify.app**
- Custom domains added in Netlify: `zidditechies.com` (primary) and `www.zidditechies.com` (redirect)
- HTTPS is enforced with a Let’s Encrypt certificate for both domains
- Netlify Forms: **brand-enquiry**, with email notification confirmed for **support@zidditechies.com**

The live deploy was published from the same files in this repository using Netlify Drop. The GitHub repository is the source of truth for future updates. The previous project (`melodious-moxie-8d4c15`) is no longer used for this domain.

## Deploy to Netlify

1. Push this folder to a repository (or drag the folder into Netlify Drop).
2. In Netlify: **Add new site → Import an existing project**, select the repo.
3. Build command: leave empty. Publish directory: `.` (already set in `netlify.toml`).
4. Deploy. Confirm the `netlify.app` address loads and the contact form appears under **Forms → brand-enquiry**.

## IONOS DNS records already applied

These records were added after the site was verified on its `netlify.app` address:

| Type | Host | Value |
| --- | --- | --- |
| A | `@` | `75.2.60.5` |
| CNAME | `www` | `luxury-pastelito-00698e.netlify.app` |

Do **not** change MX, SPF, DKIM, DMARC or any other records. The `support@zidditechies.com` mailbox is with IONOS and must stay untouched.

Netlify provisions the Let’s Encrypt certificate automatically after DNS propagation. Verify `https://zidditechies.com` and `https://www.zidditechies.com` once the Netlify HTTPS panel shows a certificate.

## Notes

- The site contains no invented case studies, testimonials or client logos.
- Netlify Forms only works after deployment on Netlify. If deployed elsewhere, replace the form `action` with a `mailto:` link or a form service.
- Fonts load from Google Fonts; system fallbacks are defined in CSS.
